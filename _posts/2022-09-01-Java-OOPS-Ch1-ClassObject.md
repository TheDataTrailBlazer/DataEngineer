# OOPS
## Class 
Class are the bluprint of the object.
#### Syntax:
<pre>
class <i>classname {
    type variable1;
    type variable2;
    type variable3; ...
    type function1(parameter-list){
    
        //body of the function1
    
    }
    type function2(parameter-list){
    
        //body of the function2
    
    </i>
}
</pre>
### Example for class creation
<pre>
class Rectangle
{
   double width;
   double height;
   
}
</pre>

## Object
Object is the instance of the class.

### Example for the object creation
Rectangle rec = new Rectangle();
### new operator
- Dynamically allocates memory for the object. The memory is allocated at the runtime. Any number of objects can be created. If memory is not sufficient then the new will rise runtime exception.

## Important Definitions:
- The data or varialbes declared in the class are called as the *instance variables.*
- Code is written in *function or method.*
- Instance variables and methods together are called *members* of a class.
- Class is a logic construct and the object is physical reality.



#### Example with 2 objects for a class.
<pre>
class Rectangle
{
   double width;
   double height;
 }
 class Main
 {
 public static void main(String args[])
 {
   Rectangle rec1=new Rectangle();
   Rectangle rec2=new Rectangle();
   double vol;
   rec1.width=12;
   rec1.height=10;
    vol=rec1.width * rec1.height; 
   System.out.println("Rectangle 1 area:  "+vol);
   rec2.width=2;
   rec2.height=11;
    vol=rec2.width * rec2.height; 
   System.out.println("Rectangle 2 area:  "+vol);
   
 }
 }
 </pre>
 ### Result: 
Rectangle 1 area:  120.0 <br>
Rectangle 2 area:  22.0

## Assigning object reference variables
<pre>
Rectangle rec1=new Rectangle();
rec1=rec2;
</pre>

- Both rec1 and rec2 will be pointing to the same object. Assignment operator will not allocate new memory. 
## Methods or functions
### Systax:
<pre>
type name(parameter-list){
//body of method
</pre>
- *type* is the type of the data returned by method. If nothing to be returned then the type should be *void*.
- If the method is returning any value then the function should end with <br>
   return *value*;
   
### Example adding methods to Rectangle
<pre>
class Rectangle
{
   double width;
   double height;
  double perimeter()
  {
    double p= 2*(width+height);
    return p;
  }
 }
 class Main
 {
 public static void main(String args[])
 {
   Rectangle rec1=new Rectangle();
   Rectangle rec2=new Rectangle();
   double vol;
   rec1.width=12;
   rec1.height=10;
    vol=rec1.width * rec1.height; 
   System.out.println("Rectangle 1 area:  "+vol);
   System.out.println("Rectangle 1 perimeter method:  "+rec1.perimeter());
   
   rec2.width=2;
   rec2.height=11;
    vol=rec2.width * rec2.height; 
   System.out.println("Rectangle 2 area:  "+vol);
   System.out.println("Rectangle 2 perimeter method:  "+rec2.perimeter());
     
 }
 }
</pre>
### Result:
Rectangle 1 area:  120.0 <br>
Rectangle 1 perimeter method:  44.0 <br>
Rectangle 2 area:  22.0 <br>
Rectangle 2 perimeter method:  26.0 <br>
## Method that takes parameters
<pre>
class Square
{
   double width;
   double area(double w)
  {
     width=w;
    double p= width*width;
    return p;
  }
 }
 class Main
 {
 public static void main(String args[])
 {
   Square s1=new Square();
     System.out.println("Square are: "+s1.area(10.0));
      
 }
 }
 </pre>
 ### Result
 Square are: 100.0

