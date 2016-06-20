# Spark


## SparkContext ad sparkConf

Spark script is programed from SparkContext class. The

~~~scala
val conf = new SparkConf()
.setAppName("SomeName")
.setaster("local[4]")

val sc = new SparkContext(conf)
~~~

The code will create a SparkContext Object with 4 threads. The name of App is Somename. And then build a SparkContext object using the simple construction method with Spark

