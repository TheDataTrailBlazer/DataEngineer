## Objects as parameters
### Example:
<pre>
class Op
  {
    int a;
    int b;
    Op(int a,int b)
    {
      this.a=a;
      this.b=b;
    }
    boolean equalTo(Op o)
    {
      if(o.a==a &&o.b==b) return true;
      else return false;
    }    
  }
class Main
  {
    public static void main(String args[])
    {
      Op t1=new Op(10,20);
      Op t2=new Op(10,20);
      Op t3=new Op(11,21);
      System.out.println("t1 == t2: " + t1.equalTo(t2));
 System.out.println("t1 == t3: " + t1.equalTo(t3));
     
    }
  }
</pre>
### Result:
t1 == t2: true <br>
t1 == t3: false
