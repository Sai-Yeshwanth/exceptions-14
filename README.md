import java.lang.reflect.*;  
  
public class Jala {  
	String str;
	public Jala(String str) {         
	      this.str = str;  
	   }
   public static void main(String[] args) {  
   
      Jala  obj = new Jala("Sai");  
      Class class1 = obj.getClass();  
      try {  
         Field Flds = class1.getField(obj.str);  
         System.out.println(" field found: " + Flds.toString());  
      } 
      catch(NoSuchFieldException e) {  
         System.out.println("Errorr "+ e.toString());  
      }  
   }  
}
