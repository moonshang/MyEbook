# trait
Similar to **interfaces** in Java, traits are used to define object types by specifying the signature of the supported methods. Like in Java 8, Scala allows traits to be partially implemented; i.e. it is possible to define default implementations for some methods. In contrast to classes, traits may not have constructor parameters. Here is an example:

```scala
trait Similarity {
  def isSimilar(x: Any): Boolean
  def isNotSimilar(x: Any): Boolean = !isSimilar(x)
}

```



#class
Classes in Scala are static templates that can be instantiated into many objects at runtime. Here is a class definition which defines a class Point:

```scala
class Point(xc: Int, yc: Int) {
  var x: Int = xc
  var y: Int = yc
  def move(dx: Int, dy: Int) {
    x = x + dx
    y = y + dy
  }
  override def toString(): String = "(" + x + ", " + y + ")";
}
```