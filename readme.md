# Vinted Brands, Sizes and Groups Dataset

***I will add more brands to the dataset in the future.***

## Overview
-------------

This dataset comprises a collection of brand names, sizes and groups and their corresponding unique identifiers from the Vinted platform. It is structured in JSON format, offering an essential tool for developers to implement brand-specific functionalities in applications.

## Dataset Structure
-----------------

The dataset is presented in a simple JSON format:

```json
{
  "name": "id",
  ...
}
```

### Sample Data

## groups.json

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

## groups.json

```json
{
  "Tailles": 4,
  "Chaussures": 7,
  "Soutiens-gorge": 53,
  "Bagues": 52,
  "Chapeaux adulte": 60,
  "Montres": 62,
  "Gants adulte": 61,
  "Ceintures femme": 64,
  "Chaussettes femme": 72,
  "Tailles hommes": 14,
  ...
}
```

## sizes.json

Each group has unique size identifiers which are listed in the `sizes.json` file. The sizes are grouped by their respective group identifiers.

```json
{
  "72": {
      "S | 35\u201338": 1517,
      "M | 39\u201342": 1518,
      "L | 43\u201346": 1519,
      "Taille unique": 1521
  },
  "14": {
      "XS": 206,
      "S": 207,
      "M": 208,
      "L": 209,
      "XL": 210,
      "XXL": 211,
      "XXXL": 212,
      "4XL": 308,
      "5XL": 309,
      "6XL": 1192,
      "7XL": 1193,
      "8XL": 1194,
      "Universel": 213
  },
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

