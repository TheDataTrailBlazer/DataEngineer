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

## Object
Object is the instance of the class.
#### Definitions:
- The data or varialbes declared in the class are called as the *instance variables.*
- Code is written in *function or method.*
- Instance variables and methods together are called *members* of a class.

### Example for class creation
<pre>
class Rectangle
{
   double width;
   double height;
   
}
</pre>
### Example for the object creation
Rectangle rec = new Rectangle();

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
 ### Result: 
Rectangle 1 area:  120.0
Rectangle 2 area:  22.0

