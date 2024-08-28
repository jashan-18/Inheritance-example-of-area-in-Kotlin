# Inheritance-example-of-area-in-Kotlin
We find area of various shapes circle , rectangle and square with the use of  inheritance in Kotlin Here is the code 

Create a class rectangle with primary constr.  A and B both of double inside it create two function one is area and other is print the area */


 open class rectangle(val a : Double , val b : Double ) {
     open fun area() : Double {
         return a*b
     }
      
     open fun display() {
         println("Area of rectangle of side $a and $b is ${area()}")
     }
 }
 
 class circle(val x : Double ) : rectangle(x , x ) {
     override fun area() : Double {
         return 3.14*x*x
     }
     
     override fun display() {
         println("Area of Circle with radius $x is ${area()}")
     }
 }
 
 class square(val r : Double ) : rectangle(r , r) {
    override fun area() : Double {
         return r*r
     }
     override fun display() {
         println("Area of square of side $r is ${area()}")
     }
 }
 
 fun main() {
     val c  = rectangle(22.22 , 44.44 )
     c.display()
     
     val q  = circle(3.22)
     q.display()
     
     val h = square(44.22)
     h.display()
 }
