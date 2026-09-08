# homework1


public class Homework1 {
		  public static void main(String []args){
		    int i, j, n;
		    for(i=0; i<10; i++) {
		      for(j=0; j<i; j++) {
		        System.out.print("#");
		      }
		      System.out.println(" ");
		    }
		  
		  for(i=0; i<10; i++) {
		      for(j=0; j<10-i; j++) {
		        System.out.print("#");
		      }
		      System.out.println(" ");
		}
		  
		  for(i=0; i<10; i++) {
		      for(j=0; j<10-i; j++) {
		        System.out.print(" ");
		      }
		      for(n=0; n<i; n++) {
		      System.out.print("#");
		      }
		      System.out.println("");
		    }
		  
		  for(i=0; i<10; i++) {
		      for(j=0; j<i; j++) {
		        System.out.print(" ");
		      }
		      for(n=0; n<10-i; n++) {
		      System.out.print("#");
		      }
		      System.out.println("");
		    }
		  
		 
	}
}
