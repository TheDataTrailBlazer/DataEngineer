## Overloading methods
- Methods can have the same names within the same class but should have different parameter declaration.
- Method overloading is one of the ways that Java supports polymorphism.
### Example
<pre>
class Op
  {
    int a;
    int b;
    
    int operation(int a)
    {
      int square=a*a;
      return square;
    }
    int operation(int a,int b)
    {
      int add=a+b;
      return add;
    }    
  }
class Main
  {
    public static void main(String args[])
    {
      Op o=new Op();
      System.out.println("Sqaure value: "+o.operation(10));
       System.out.println("Addition value: "+o.operation(10,20));
    }
  }
</pre>
### Result:
Sqaure value: 100 <br>
Addition value: 30
## Overloading Constructors
- If the required variables are not initalized properly then overloading the constructor will handle the improper initialization.
## Example:
<pre>
class Op
  {
    int a;
    int b;
    Op()
    {
      a=-1;
      b=-1;
    }
       Op(int a)
    {
      this.a=a;
      b=a;
    }
           Op(int a,int b)
    {
      this.a=a;
      this.b=b;
    }
    int multiply()
    {
      int mul=a*b;
      return mul;
    }    
  }
class Main
  {
    public static void main(String args[])
    {
      Op o1=new Op();
      Op o2=new Op(10);
      Op o3=new Op(10,20);
      System.out.println("No values provided: "+o1.multiply());
       System.out.println("One values provided: "+o2.multiply());
      System.out.println("Both values provided: "+o3.multiply());
    }
  }
</pre>
### Result:
<pre>
No values provided: 1
One values provided: 100
Both values provided: 200
</pre>
