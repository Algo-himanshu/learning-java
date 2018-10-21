# learning-java
best programs for boards and above studies
/*The  names  of  the  teams  participating  in  a  competition  should  be  displayed  on  a banner vertically, 
to accommodate as many teamsas possible in asingle banner.Design a program to accept the names of N teams, 
where 2 < N < 9 and display them in vertical order, side by side with a horizontal tab (i.e. eight spaces). 
Test your program for the following data and some random data**/


import java.util.*;
import java.io.*;
class vertical
{
        static int n;
        int len;
        
        void limit()
        {
            Scanner sc=new Scanner(System.in);
            System.out.println("INPUT NUMBER OF TEAMS");
            int N=sc.nextInt();
            n=N;
        }
        void name()
        {
            Scanner sc=new Scanner(System.in);
            String arr[]=new String[n];
            String s;
            int len=0;
            char ch;
            String st;
            for(int i=0;i<n;i++)
            {
                System.out.print("Team "+(i+1)+": ");
                arr[i]=sc.nextLine();
                s=arr[i];
                System.out.println();
                if(s.length()>len)
                {
                    len=s.length();
                }
            }
            System.out.println("OUTPUT");
            System.out.println();
            for(int k=0;k<len;k++)          //for string characters
            {
                for(int j=0;j<n;j++)   //for arrays
                {
                    st=arr[j];
                    
                    if(st.length()>=(k+1))
                    {
                      ch=st.charAt(k);
                      System.out.print(ch+"        ");
                    }
                    else
                    {
                    System.out.print("         ");
                    }
                }
                System.out.println();
            }
       }
       public static void main(String args[])
       {
            vertical obj=new vertical();
            obj.limit();
            if(n>2&&n<9)
            {
                obj.name();
            }
            else
            {
                System.out.print("Wrong choice");
            }
            
        }
}
