## Welcome to learn Google Earth Engine

Google Earth Engine(GEE) combines a multi-petabyte catalog of satellite imagery and geospatial datasets with planetary-scale analysis capabilities and makes it available for scientists, researchers, and developers to detect changes, map trends, and quantify differences on the Earth's surface

The Google Earth Engine is free registered account and all data have been stored in clouds, therefore you don't need a space of your marchine to store and spatial data. 
### How to use code in GEE

Code as a very powerful which can be runned in GEE, for example you just copy the code below and past it in ``New script`` window in GEE and ``run`` then you will see the result in the map below the script
```
var dataset = ee.ImageCollection('LANDSAT/LE07/C01/T1_32DAY_EVI')
                  .filterDate('2020-01-01', '2020-12-31');
var colorized = dataset.select('EVI');
var colorizedVis = {
  min: 0.0,
  max: 1.0,
  palette: [
    'FFFFFF', 'CE7E45', 'DF923D', 'F1B555', 'FCD163', '99B718', '74A901',
    '66A000', '529400', '3E8601', '207401', '056201', '004C00', '023B01',
    '012E01', '011D01', '011301'
  ],
};
Map.setCenter(105.089791088926,12.534845667599683, 6);
Map.addLayer(colorized, colorizedVis, 'Colorized');
```

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Yavnet2021/.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
