package task5;
import java.io.*;
import java.util.ArrayList;
import java.util.Scanner;

class Student {
    String name;
    int rollNum;
    String grade;

    Student(String n, int r, String g){
        name = n;
        rollNum = r;
        grade = g;
    }
}
public class StudentManagementSystem {
    static ArrayList<Student> stList = new ArrayList<>();
    static String fileName = "students.txt";

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        loadStudents();

        boolean run = true;
        while(run){
            System.out.println("1.Add 2.Remove 3.Search 4.Display 5.Exit");
            System.out.print("Choice: ");
            int c = sc.nextInt();
            sc.nextLine();

            if(c==1){
                System.out.print("Name: ");
                String n = sc.nextLine();
                System.out.print("Roll: ");
                int r = sc.nextInt();
                sc.nextLine();
                System.out.print("Grade: ");
                String g = sc.nextLine();
                stList.add(new Student(n,r,g));
                saveStudents();
                System.out.println("Added");
            } else if(c==2){
                System.out.print("Roll to remove: ");
                int r = sc.nextInt();
                sc.nextLine();
                for(int i=0;i<stList.size();i++){
                    if(stList.get(i).rollNum==r){
                        stList.remove(i);
                        System.out.println("Removed");
                        saveStudents();
                        break;
                    }
                }
            } else if(c==3){
                System.out.print("Roll to search: ");
                int r = sc.nextInt();
                sc.nextLine();
                for(Student s: stList){
                    if(s.rollNum==r){
                        System.out.println("Name:"+s.name+" Roll:"+s.rollNum+" Grade:"+s.grade);
                    }
                }
            } else if(c==4){
                for(Student s: stList){
                    System.out.println(s.rollNum+" "+s.name+" "+s.grade);
                }
            } else if(c==5){
                run=false;
                System.out.println("Bye");
            } else{
                System.out.println("Invalid");
            }
        }
    }

    static void saveStudents(){
        try{
            PrintWriter pw = new PrintWriter(new FileWriter(fileName));
            for(Student s: stList){
                pw.println(s.rollNum+","+s.name+","+s.grade);
            }
            pw.close();
        } catch(Exception e){
            System.out.println("Save error");
        }
    }

    static void loadStudents(){
        try{
            BufferedReader br = new BufferedReader(new FileReader(fileName));
            String line;
            while((line=br.readLine())!=null){
                String[] parts = line.split(",");
                stList.add(new Student(parts[1],Integer.parseInt(parts[0]),parts[2]));
            }
            br.close();
        } catch(Exception e){}
    }
}
