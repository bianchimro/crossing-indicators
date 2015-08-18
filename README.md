# crossing-indicators

## Cross correlations matrix

## Data structure
Data must consist of a serie of indicators related to the same "entities" (i.e. geographic or political territories). Indicators are grouped into categories for operating grouped selections. Categorization of indicators is not strictly required and in case of no categorization provided, all indicators will be assigned to the same category.

### Data processing

A cross correlation matrix between the various series of indicators is calculated as the Spearman's rank correlation coefficient between each possible couple of normalized serie of data. (http://en.wikipedia.org/wiki/Spearman's_rank_correlation_coefficient)

For computing the correlation coefficient for each couple of indicators only the entities having a score for both series must be taken in account.

### Pre processing

In order to simplify access and visualization to data, the dataset is represented in various formats, for easily accessing informations by lookups. This may lead to a redundancy in data representation, in favour of better performance in rendering the visualization.

* by-entity view
* by-indicator view
* cross correlation matrix

### Visualization

The cross correlation matrix is visualized, with color of cells representing correlation value between indicators in x and y axis.

By selecting a cell a scatterplot is visualized with the two correlated indicators on x and y axis.

Representing the whole square matrix lets us plot all combinations of scatterplots (obtained by inverting x and y axis).

## Joining more data

### Geographic data

* Latitude
* Longitude
* Altitude
* Distance from somewhere

### Other data series
Any other data series related to the observed entities can be joined in


## Dynamic ranking
Another desired feature is dynamic ranking of entities, that can be accomplished by:

* Filtering out categories of indicators or single indicators
* Weighting categories and/or indicators
