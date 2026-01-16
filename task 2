
package task2;
import java.util.Scanner;

public class StudentGradeCalculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("How many subjects? ");
        int sub = sc.nextInt();
        int tot = 0;
        for(int i=0;i<sub;i++){
            System.out.print("Marks for subject "+(i+1)+": ");
            tot += sc.nextInt();
        }
        double avg = tot/(double)sub;
        String grd;
        if(avg>=90) grd="A";
        else if(avg>=80) grd="B";
        else if(avg>=70) grd="C";
        else if(avg>=60) grd="D";
        else grd="F";
        System.out.println("Total: "+tot);
        System.out.println("Average: "+avg);
        System.out.println("Grade: "+grd);
    }
}

