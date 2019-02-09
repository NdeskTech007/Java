# Java
package labwork;

import java.io.BufferedReader; import java.io.File; import java.io.FileNotFoundException; import java.io.FileReader; import java.io.IOException;

public class Labwork {

public static void main(String[] args) throws FileNotFoundException, IOException {
    File file = new File("C:\\Users\\Nazmul\\Desktop\\default.txt");
    BufferedReader br = new BufferedReader(new FileReader(file));
    String x;

    System.out.print("Keywords : ");
    while ((x = br.readLine()) != null) {
        String[] y = x.split("[, ;()]");
        int z = x.split(", ;()").length;
        for (int j = 0; j < z; j++) {
            if ("int".equals(y[j]) || "float".equals(y[j]) || "char".equals(y[j]) || "if".equals(y[j]) || "else".equals(y[j])) {
                System.out.print(y[j] + ",");
            }
        }
    }

    File file1 = new File("C:\\Users\\Nazmul\Desktop\\default.txt");
    BufferedReader br1 = new BufferedReader(new FileReader(file1));
    String x1;

    System.out.print("\n" + "Identifires : ");
    while ((x1 = br1.readLine()) != null) {

        String[] y1 = x1.split("[ ]");
        int z1 = x1.split(" ").length;

        for (int j1 = 1; j1 < z1 - 1; j1++) {

            String x11 = ",";
            if ("int".equals(y1[0]) || "float".equals(y1[0]) || "char".equals(y1[0]) || "long".equals(y1[0]) || "double".equals(y1[0])) {
                x11 += y1[j1];
            }
            String[] y11 = x11.split("[,]");
            int z11 = x11.split(",").length;

            for (int j11 = 1; j11 < z11; j11++) {
                System.out.print(y11[j11] + ",");

            }
        }
    }
    
    
    
    File file2 = new File("C:\\Users\\Nazmul\\Desktop\\default.txt");
    BufferedReader br2 = new BufferedReader(new FileReader(file2));
    String x2;

    System.out.print("\n" + "Math Operations : ");
    while ((x2 = br2.readLine()) != null) {
        char ch[]=x2.toCharArray(),ch1[] = null;

        for(int i=0;i<ch.length;i++){
            if(ch[i]=='+'||ch[i]=='-'||ch[i]=='*'||ch[i]=='/'||ch[i]=='='){
                //ch1[j++]=ch[i];
                System.out.print(ch[i]+",");
            }
        }
    }
}
}
