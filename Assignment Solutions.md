# Code

``` 1.

import java.util.*;
public class Main {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int flag=0;
        int n = sc.nextInt();
        int[] arr = new int[n];
        for(int i=0;i<n;i++){
            arr[i]=sc.nextInt();
        }
        int x = sc.nextInt();
        for(int i=0;i<n;i++){
            if(arr[i]==x){
                System.out.println(x+" found at location "+(i+1));
                flag=1;
                break;
            }
        }
        if(flag==0){
            System.out.println(x+" is not found");
        }
    }
}


-----------------

import java.util.*;
import java.text.*;
public class Main{
    static void printCurrency(Locale locale,double x){
        NumberFormat form = NumberFormat.getCurrencyInstance(locale);
        String curr = form.format(x);
        System.out.println("Formatted in dollars "+curr);
    }
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        double n = sc.nextDouble();
        System.out.println("Without fraction part "+Math.round(n));
        System.out.printf("Formatted to give precision %.2f",(float)n);
        System.out.println();
        System.out.println("Appended zeroes to right "+String.format("%.6f",n));
        DecimalFormat df = new DecimalFormat("00000.##");
        System.out.println("Formatting numeric part "+df.format(n));
        printCurrency(Locale.US,n);
    }
}

-----------------------------
2.
import java.util.*;
public class Main {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        String str1 = sc.next();
        String newstr = str;
        int n1 = str1.length();
        for(int i=0;i<n1;i++){
            str=str.replace(str1.charAt(i),'x');
        }
        System.out.println(newstr);
        for(int i=0;i<str.length();i++){
            if(str.charAt(i)=='x')
            continue;
            else
            System.out.print(str.charAt(i));
        }
    }
}

---------------------------------
import java.util.*;
public class Main {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        for(int i=0;i<n;i++){
            for(int j=0;j<n;j++){
                if(i!=j){
                    System.out.print(0);
                }
                else
                System.out.print(1);
            }
            System.out.println();
        }
    }
}
------------------------------------
3.


import java.util.*;
import java.sql.*;
public class Main {
    public static void main(String[] args) throws Exception{
        Scanner sc = new Scanner(System.in);
        //Class.forName("")
        String str = sc.next();
        str="'"+str+"'";
        //System.out.println(str);
        final String url = "jdbc:mysql://localhost/ri_db";
        final String username = "test";
        final String password ="test123";
        try(Connection connection = DriverManager.getConnection(url, username, password);
        Statement statement = connection.createStatement();){
                String sql = "DELETE FROM book WHERE name ="+str;
                statement.executeUpdate(sql);
                ResultSet rs = statement.executeQuery("SELECT Id, name, author FROM book;");
                while(rs.next()){
                    System.out.print(rs.getString(1));
                    System.out.print(rs.getString(2));
                    System.out.print(rs.getString(3));
                    System.out.println();
                }
        }catch(SQLException e){
            e.printStackTrace();
        }
            }
            
        
    
}

-------------------------------------

import java.util.*;
public class Main {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        System.out.println("cube of "+n+" is "+(n*n*n));
    }
}

--------------------------------------

4.

public class Main {
    public static void main(String[] args){
        int[] arr = new int[]{1,2};
        int n =0;
        try{
            //System
            n=arr[3];
        }
        catch(Exception e){
            System.out.println(e);
        }
    }
}
------------------------------------

import java.util.*;
public class Main {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        switch(n){
            case 1:
                System.out.print("The entered month is in the Winter");
                break;
            case 10:
                System.out.print("The entered month is in the Winter");
                break;
            case 11:
                System.out.print("The entered month is in the Winter");
                break;
            case 12:
                System.out.print("The entered month is in the Winter");
                break;
            case 2:
                System.out.print("The entered month is in the Summer");
                break;
            case 3:
                System.out.print("The entered month is in the Summer");
                break;
            case 4:
                System.out.print("The entered month is in the Summer");
                break;
            case 5:
                System.out.print("The entered month is in the Summer");
                break;
            case 6:
                System.out.print("The entered month is in the Spring");
                break;
            case 7:
                System.out.print("The entered month is in the Spring");
                break;
            case 8:
                System.out.print("The entered month is in the Spring");
                break;
            case 9:
                System.out.print("The entered month is in the Spring");
                break;
            default:
                System.out.print("The entered month is in the Bogus Month");
                break;
                
            
            
        }
    }
}

-------------------------------------------------------
8.

import java.util.*;
public class Main {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[][] mat1 = new int[n][n];
        int[][] mat2 = new int[n][n];
        int[][] mat = new int[n][n];
        for(int i=0;i<n;i++){
            for(int j=0;j<n;j++){
                mat1[i][j]=sc.nextInt();
            }
        }
        for(int i=0;i<n;i++){
            for(int j=0;j<n;j++){
                mat2[i][j]=sc.nextInt();
            }
        }
        for(int i=0;i<n;i++){
            for(int j=0;j<n;j++){
                mat[i][j]=0;
                for(int k=0;k<n;k++){
                    mat[i][j] += mat1[i][k]*mat2[k][j];
                }
                System.out.println(mat[i][j]+" ");
            }
            System.out.println();
        }
        
    }
}

__________________________________________________________

class Vehicle {
    String str;
    public void move(String str){
        System.out.println(str);
    }
}
class MotorBike extends Vehicle {
    String str;
    public void move(String str){
        System.out.println(str);
    }
}

______________________________--------------------------------

9.

import java.util.*;
public class Main {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        List<Integer> list = new ArrayList<>();
        for(int i=0;i<n;i++){
            list.add(sc.nextInt());
        }
        System.out.println(list);
    }
}
----------------------------------------------------

import java.sql.*;
import java.util.*;
public class Main {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String str = sc.next();
        str="'"+str+"'";
        String url = "jdbc:mysql://localhost/ri_db";
        String user = "test";
        String pass = "test123";
        try(Connection connection = DriverManager.getConnection(url,user,pass)){
            try(Statement statement = connection.createStatement();){
                String sql = "SELECT id,name FROM student WHERE dept="+str+";";
                ResultSet rs = statement.executeQuery(sql);
                while(rs.next()){
                    System.out.println(rs.getString(1)+" "+rs.getString(2));
                }
                
            }
        }
        catch(SQLException e){
            System.out.print(e);
        }
    }
}

--------------------------------------------------------
10.

import java.util.*;
public class Main {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        for(int i=n;i>0;i--){
            for(int j=i;j>0;j--){
                System.out.print("*"+" ");
            }
            System.out.println();
        }
    }
}

___________________________________________________


import java.util.*;
public class Main {
    public static void main(String[] args){
        List<Integer> list = new ArrayList<>();
        list.add(1);
        list.add(2);
        list.add(3);
        System.out.println("Size of the collection "+list.size());
        int n = list.size();
        System.out.println("Is the arrayList empty: "+ (n>0 ? false:true));
    }
}
_______________________________________________________
```
