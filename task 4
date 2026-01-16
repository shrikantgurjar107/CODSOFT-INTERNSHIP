import java.io.*;
import java.net.*;
import java.util.Scanner;

public class CurrencyConverter {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);
        System.out.print("Base currency: ");
        String base = sc.next().toUpperCase();
        System.out.print("Target currency: ");
        String target = sc.next().toUpperCase();
        System.out.print("Amount: ");
        double amt = sc.nextDouble();

        String u = "https://api.exchangerate.host/convert?from="+base+"&to="+target+"&amount="+amt;
        URL url = new URL(u);
        HttpURLConnection c = (HttpURLConnection) url.openConnection();
        c.setRequestMethod("GET");

        BufferedReader r = new BufferedReader(new InputStreamReader(c.getInputStream()));
        String res="", l;
        while((l=r.readLine())!=null) res+=l;
        r.close();

        int i = res.indexOf("result");
        if(i!=-1){
            int s = res.indexOf(":",i)+1;
            int e = res.indexOf("}",s);
            String val = res.substring(s,e).trim();
            double conv = Double.parseDouble(val);
            System.out.println(amt+" "+base+" = "+conv+" "+target);
        } else {
            System.out.println("Invalid currency or error");
        }
    }
}
