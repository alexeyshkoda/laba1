/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package algoritm_laba1;

/**
 *
 * @author user
 */
import java.util.Scanner;

public class Algoritm_laba1 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        
        Scanner in=new Scanner(System.in);
        double[] array;
        System.out.println("Put n");
        int n=in.nextInt();
        array=new double [n];
        
        double sum=0;
        
        for(int i=0;i<n;i++)
            {   
            
            array[i]=(-50)+Math.random()*100;
            
                        }
        long startTime = System.nanoTime();
        
        for(int i=0;i<n;i++)
                        {      
            
            
            if (0>array[i])
                sum+=array[i];
                        }
        
            long timeSpent = System.nanoTime()-startTime;
            
        System.out.println("The generated array:");
            
        for(int i=0;i<n;i++)
            {
                System.out.print(String.format("%.2f",array[i])+" ");
                
            }
        System.out.println("\n Sum of negative Elements="+String.format("%.2f",sum));
        double timeSpentMs =(double)timeSpent/1000000.0;
         System.out.println("Running time "+timeSpent+" nanoseconds");
        System.out.println("Running time "+String.format("%.10f",timeSpentMs)+" milliseconds");
                                           }
}
