# this Keyword
- If the local variables in the class and the parameters for the formal parameters for the method are same then local variables *hides* the instance variables.
-  this can be used inside any method to refer to the *current* object. 
### Example without this Keyword:
<pre>
class Rectangle
{
   double width;
   double height;
  Rectangle(double width, double height)
  {
    width=width;
    height=width;
  }
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
   Rectangle rec1=new Rectangle(10,20);
   
   double vol;
   
    vol=rec1.width * rec1.height; 
   System.out.println("Rectangle 1 area:  "+vol);
   System.out.println("Rectangle 1 perimeter method:  "+rec1.perimeter());
  
  
      }
 }
</pre> 
### Result:
Rectangle 1 area:  0.0 <br>
Rectangle 1 perimeter method:  0.0
### Example with this keyword
<pre>
class Rectangle
{
   double width;
   double height;
  Rectangle(double width, double height)
  {
    this.width=width;
    this.height=width;
  }
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
   Rectangle rec1=new Rectangle(10,20);
   
   double vol;
   
    vol=rec1.width * rec1.height; 
   System.out.println("Rectangle 1 area:  "+vol);
   System.out.println("Rectangle 1 perimeter method:  "+rec1.perimeter());
  
  
      }
 }
</pre>
### Result:
Rectangle 1 area:  100.0 <br>
Rectangle 1 perimeter method:  40.0

## Garbage Collection
- When we create an object with *new* then the dynamic allocation of memory occurs.
- In C++ you have to use keyword *delete* to manually deallocate the memory.
- But in Java; it deallocated automatically. The technique is called **Garbage Collection**.
- When no references to an object exist, that object is assumed to be no longer needed, and the memory 
occupied by the object can be reclaimed. 
## Finalize() method
- Sometimes an object will need to perform some action when it is destroyed. For example, 
if an object is holding some non-Java resource such as a file handle or character font, then 
you might want to make sure these resources are freed before an object is destroyed. To 
handle such situations, Java provides a mechanism called finalization.
- finalize( ) is only called just prior to garbage collection.
### Syntax:
<pre>
protected void finalize( )
{
// finalization code here
}
</pre>
