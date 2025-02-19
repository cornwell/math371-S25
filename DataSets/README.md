## Data sets found in this folder

---

### Auto Data
The gas mileage, number of cylinders, weight, and other information for 392 vehicles. This data was taken from the StatLib library maintained at Carnegie Melon University, and was also used in the book _An Introduction to Statistical Learning_.

Consists of 392 observations on 9 variables.
* `mpg`: miles per gallon
* `cylinders`: Number of cylinders between 4 and 8
* `displacement`: Engine displacement in cubic inches
* `horsepower`: Engine horsepower
* `weight`: Vehicle weight in lbs.
* `acceleration`: Seconds to accelerate from 0 to 60 mph
* `year`: Model year (modulo 100)
* `origin`: Origin of car (1 = American; 2 = European; 3 = Japanese)
* `name`: Vehicle name

#### Notes 
The original data set had 397 observations. Of these, 5 were missing values in the `horsepower` column and are removed.

```python
auto = pd.read_csv('./DataSets/Auto.csv')
auto[['mpg','cylinders','displacement','horsepower']].describe()
```

|       | mpg | cylinders | displacement | horsepower |
| ---   | --- | ---       | ---          | ---        |
| count |392.000000|392.000000|	392.000000|	392.000000|
|mean   |23.445918 |5.471939  |	194.411990|	104.469388|
|std    |7.805007  |1.705783  |	104.644004|	38.491160 |
|min	|9.000000  |3.000000  |68.000000  |46.000000  |
|25%	|17.000000 |4.000000  |105.000000 |75.000000  |
|50%	|22.750000 |4.000000  |151.000000 |93.500000  |
|75%	|29.000000 |8.000000  |275.750000 |126.000000 |
|max	|46.600000 |8.000000  |455.000000 |230.000000 |