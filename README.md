INHERITENCE:-

package dog1;


public class Dog1 {

    int size=30;
    
    void size(){
    
        System.out.println("20");
    }
    void brak(){
    
        System.out.println("ruff");
    }
}
public class cat extends Dog1{


}

     public static void main(String[] args) {
     
       cat c = new cat();
       
       c.size();
    }
    
    2.ENCAPSULATION:-
    
    package encapsulation;

public class EncapSulation {

    private int rollno;
    
    private String name;
    
    private int age;
    
    //start getter methods
    
    public int getrollno(){
    
    return rollno;
    
}
    public String getname(){
    
        return name;
        
    }
    public int getage(){
    
        return age;
    }
    //start satter methods
    
    public void setrollno(int value){
    
        rollno=value;
        
    }
    public void setname(String value){
    
        name=value;
    }
    public void setage(int value){
    
        age=value;
    }
   
    public class EncapTest {
    

    public static void main(String[] args) {
    
      encapsulation e = new encapsulation();
      
      e.setrollno(01);
      
      e.setname("rabia");
      
      e.setage(20);
      
      System.out.println("rollno" +e.getrollno);
      
      System.out.println("name" +e.getname);
      
      System.out.println("age" +e.getage);
      
    }
}

3.POLYMORPHISM:-

public class Employee

{
   private String name;
   
   private String address;
   
   private int number;
   
   public Employee(String name, String address, int number)
   
   {
      System.out.println("Constructing an Employee");
      
      this.name = name;
      
      this.address = address;
      
      this.number = number;
      
   }
   public void mailCheck()
   
   {
      System.out.println("Mailing a check to " + this.name
       + " " + this.address);
       
   }
   public String toString()
   
   {
      return name + " " + address + " " + number;
      
   }
   public String getName()
   
   {
      return name;
      
   }
   
   public String getAddress()
   
   {
      return address;
      
       }
       
   public void setAddress(String newAddress)
   
   {
      address = newAddress;
      
   }
   
   public int getNumber()
   
   {
     return number;
     
   }
}
   //NEW FILE
   
   public class Salary extends Employee
   
{
   private double salary; //Annual salary
   
   public Salary(String name, String address, int number, double
      salary)
      
   {
       super(name, address, number);
       
       setSalary(salary);
       
   }
   
   public void mailCheck()
   
   {
       System.out.println("Within mailCheck of Salary class ");
       
       System.out.println("Mailing check to " + getName()
       + " with salary " + salary);
   }
   
   public double getSalary()
   
   {
       return salary; 
       
    }
    
   public void setSalary(double newSalary)
   
   {
       if(newSalary >= 0.0)
       
       {
          salary = newSalary;
          
       }
   }
   public double computePay()
   
   {
      System.out.println("Computing salary pay for " + getName());
      
      return salary/52;
      
   }
   
}
//NEW FILE

public class VirtualDemo

{
   public static void main(String [] args)
   
   {
      Salary s = new Salary("Mohd Mohtashim", "Ambehta, UP", 3, 3600.00);
      
      Employee e = new Salary("John Adams", "Boston, MA", 2, 2400.00);
      
      System.out.println("Call mailCheck using Salary reference --");
      
      s.mailCheck();
      
      System.out.println("\n Call mailCheck using Employee reference--");
      
      e.mailCheck();
      
    }
    
}

4.ABSTRACT:-

public class Main{

	public static void main(String args[]){
	
        TwoWheeler test = new Honda();
        
        test.run();
    }
    
}
abstract  class TwoWheeler {

    public abstract void run();
    
}
class Honda extends TwoWheeler{

	public void run(){
	
		System.out.println("Running..");
		
	}
	
}
    
    
