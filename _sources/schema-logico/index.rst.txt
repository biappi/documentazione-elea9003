Schema Logico
=============

.. raw:: html

    <style>
    .leaflet-container {
        background:rgba(255,0,0,0.0);
    }

    #image2d {
        background:rgba(255,0,0,0.0);
        width: 100%;
        height: 800px;
        padding: 0;
        margin: 0;
    }
    </style>

    <div id="image2d"></div>
    <link rel="stylesheet" type="text/css" href="../_static/leaflet.css" />
    <script type="text/javascript" src="../_static/leaflet.js"></script>
    <script type="text/javascript">

        const ImageLayer = L.TileLayer.extend({
            initialize: function (url, options) {
                var options = L.setOptions(this, options);
                this._url = url;
                var southWest = map.unproject([0, options.height], 5);
                var northEast = map.unproject([options.width, 0], 5);
                options.bounds = new L.LatLngBounds(southWest, northEast);	
            },

            _toQuad: function (x, y, z) {
                var quadkey = 't';
                for ( var i = z; i >= 0; --i) {
                    var bitmask = 1 << i;
                    var digit = 0;

                    if ((x & bitmask) !== 0) { digit |= 1; }
                    if ((y & bitmask) !== 0) { digit |= 2; }

                    quadkey += "qrts"[digit];
                }

                return quadkey;
            },

            getTileUrl: function(tilePoint) {
                var quad = this._toQuad(tilePoint.x, tilePoint.y, tilePoint.z)
                return this._url + quad + '.jpg';
            },

        });

        var map = L.map('image2d').setView(new L.LatLng(0,0), 0);
        var dzLayer = new ImageLayer('../_static/schema-logico/', { 
            width: 8192, 
            height: 8192,
            tileSize: 256,
            maxZoom: 5,
            noWrap: true,
        }).addTo(map);

    </script>

