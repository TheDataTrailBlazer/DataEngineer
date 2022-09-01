# Constructors
## Definition:
A *constructor* initializes an object immediately upon creation.
### Important points:
- It is a tedious task to initialize the variables everytime the object is created. 
- Java allows objects to be automatically initialized with the help of constructors.
- Constructor has the same name as the class where it resides and syntactically similar to methods.
- Constructor is automatically called when objects are created, before *new* operator is completed.
- Constructors has no return type not even *void*.
- Implicit return type of class constructor is class type itself.

### Types of constructors: Default(No arguments) and Parameterized.
## Default Constructors:
Constructors with no arguments.

### Example:
<pre>
class Rectangle
{
   double width;
   double height;
  Rectangle()
  {
    width=10;
    height=20;
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
   Rectangle rec1=new Rectangle();
   
   double vol;
   
    vol=rec1.width * rec1.height; 
   System.out.println("Rectangle 1 area:  "+vol);
   System.out.println("Rectangle 1 perimeter method:  "+rec1.perimeter());
  
  
      }
 }
 </pre>
 ### Result:
 Rectangle 1 area:  200.0 <br>
 Rectangle 1 perimeter method:  60.0
 ## Parameterized Constructors
 - Default constructors are not very useful as they does not initialze the constructors. 
 - **Solution:** use parameterized constructors when we initialize the instance variables while creation of the class. 
 ### Example
 <pre>
 class Rectangle
{
   double width;
   double height;
  Rectangle(double w, double h)
  {
    width=w;
    height=h;
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
 ### Result
Rectangle 1 area:  200.0 <br>
Rectangle 1 perimeter method:  60.0

