# react-leaflet-measure

[![travis build](https://img.shields.io/travis/mhasbie/react-leaflet-measure.svg?style=plastic)](https://travis-ci.org/mhasbie/react-leaflet-measure)
[![version](https://img.shields.io/npm/v/react-leaflet-measure.svg?style=plastic)](http://npm.im/react-leaflet-measure)
[![MIT License](https://img.shields.io/npm/l/react-leaflet-measure.svg?style=plastic)](http://opensource.org/licenses/MIT)
[![dependencies](https://img.shields.io/david/mhasbie/react-leaflet-measure.svg?style=plastic)](https://david-dm.org/mhasbie/react-leaflet-measure)
[![peer dependencies](https://img.shields.io/david/peer/mhasbie/react-leaflet-measure.svg?style=plastic)](https://david-dm.org/mhasbie/react-leaflet-measure?type=peer)
[![downloads](https://img.shields.io/npm/dt/react-leaflet-measure.svg?style=plastic)](http://npm-stat.com/charts.html?package=react-leaflet-measure&from=2018-01-01)
[![issues](https://img.shields.io/github/issues/mhasbie/react-leaflet-measure.svg?style=plastic)](https://github.com/mhasbie/react-leaflet-measure/issues)

React wrapper of [leaflet-measure](https://github.com/ljagis/leaflet-measure)
for [react-leaflet](https://github.com/PaulLeCam/react-leaflet).

Coordinate, linear, and area measure control for [Leaflet](http://leafletjs.com) maps. Extends [L.Control](http://leafletjs.com/reference.html#control).

*Tested with Leaflet 1.0.3 and React-Leaflet 1.3.1*

[![Demo](http://ljagis.github.io/leaflet-measure/assets/leaflet-measure.png)](http://ljagis.github.io/leaflet-measure)

[Demo JSFiddle](https://jsfiddle.net/m_hasbie/sb20zL8w/)

## Installation

### Install via NPM

```bash
npm install react-leaflet-measure --save
```

Include leaflet-measure.css stylesheet to your project.

```html
<link rel="stylesheet" href="leaflet-measure.css">
```

## Usage example

```javascript
import { Map, TileLayer } from 'react-leaflet';
import MeasureControl from 'react-leaflet-measure';

const measureOptions = {
  position: 'topright',
  primaryLengthUnit: 'meters',
  secondaryLengthUnit: 'kilometers',
  primaryAreaUnit: 'sqmeters',
  secondaryAreaUnit: 'acres',
  activeColor: '#db4a29',
  completedColor: '#9b2d14'
};
		
<Map center={[101.483459, 2.938926]} zoom={12}>
  <TileLayer
    url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
    attribution='&copy; <a href="http://osm.org/copyright">OpenStreetMap</a> contributors'
  />

  <MeasureControl {...measureOptions} />
</Map>
```

### Control options

Any props passed to MeasureControl are passed down to leaflet-measure.

Refer [leaflet-measure control options](https://github.com/ljagis/leaflet-measure#control-options).


# Credits
Credits goes to all the [contributors](https://github.com/ljagis/leaflet-measure/graphs/contributors) for the original work.


# License

MIT License
