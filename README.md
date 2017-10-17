# INFX-499

import java.io.*;

import java.util.*;

import java.text.DateFormat;

import java.util.Date;

import java.text.SimpleDateFormat;




class medicine 
{
    public static void main (String[] args) 
{

    Scanner s = new Scanner(System.in);

    System.out.println("Enter medicine:");

    String medicine = s.nextLine();

    System.out.println("Enter Tmax (in hours):");

    int tmax = s.nextInt();

    System.out.println("Enter half time (in hours):");

    int half = s.nextInt();

    System.out.println("Do you want to enter time of dose: ");

    char n = s.next().charAt(0);

    int time=0;

    int amount;

    DateFormat time2 = new SimpleDateFormat("HH:mm:ss");

    Date date = new Date();

    if(n=='y')

{

        System.out.println("Enter amount of medicine (in mg):");

        amount = s.nextInt();

        System.out.println("Enter time of dosage:");

        time = s.nextInt();

}

    else

{

       System.out.println("Enter amount of medicine (in mg):");

       amount = s.nextInt();

       //System.out.println(sdf.format(date));

      //time2 = time2.format(date);  

}

    System.out.println("");

    System.out.println("The medicine details are: ");

    System.out.print("Medicine:");

    System.out.println(medicine);

    System.out.print("Time of dosage:");
    

    if(n=='y')

        System.out.println(time);
        

    else

        System.out.println(time2.format(date));

        System.out.print("Full dosage time: ");

        System.out.println(time + tmax*100);

        System.out.print("Half concentration time:");

        System.out.println(time + tmax*100 + half*100);

}

}

