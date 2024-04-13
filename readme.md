# Vinted Brands Dataset
============================

## Overview
--------

This dataset comprises a collection of brand names and their corresponding unique identifiers from the Vinted platform. It is structured in JSON format, offering an essential tool for developers to implement brand-specific functionalities in applications.

## Dataset Structure
-----------------

The dataset is presented in a simple JSON format:

```json
{
  "Brand Name": "Brand ID",
  ...
}
```

### Sample Data

```json
{
  "GUESS": "20",
  "Jordan": "2703",
  "Continental": "52427",
  "Pokémon": "191646",
  "Esprit": "17",
  "Shein": "172724",
  "adidas": "14",
  "Vintage": "573",
  "Reborn": "340261",
  "Catimini": "7835",
  "Funk": "335369",
  "Camaïeu": "26",
  "Disney": "34",
  "Converse": "11445",
  "Xiaomi": "201078",
  "Cecil": "2749",
  "IKEA": "184302",
  "ASOS": "49",
  ...
}
```

## Usage
-----

### Integration with Fuse.js

This dataset can be integrated with `fuse.js` to enable fuzzy searching capabilities, enhancing user interaction by allowing lenient brand name searches. Here's a quick example:

```javascript
const Fuse = require('fuse.js');
const brands = require('./vinted_brands.json');

const fuse = new Fuse(brands, { keys: ["name"], includeScore: true });

// Example search
const result = fuse.search('nike');
console.log(result);
```

