
-----------------------------------------------------------------ENGLISH------------------------------------------------------------------------

In this question,we have a text file full of ZEROs and ONEs. So firstly,I wrote a Java code to convert ZEROs and ONEs into 0s and 1s. 

import java.io.*; import java.util.Scanner;

public class Oku {

 public static void main(String[] args) {

        {
         try
             {
             File file = new File("/home/compleng/Desktop/CTF/AlexCTF/crypto1/zero_one");
             BufferedReader reader = new BufferedReader(new FileReader(file));
             String line = "", oldtext = "";
             while((line = reader.readLine()) != null)
                 {
                 oldtext += line + "\r\n";
             }
             reader.close();

             String replacedtext  = oldtext.replaceAll("ZERO", "0");
             replacedtext = replacedtext.replaceAll("ONE", "1" );


             FileWriter writer = new FileWriter("/home/compleng/Desktop/CTF/AlexCTF/crypto1/output.txt");
             writer.write(replacedtext);


             writer.close();

         }
         catch (IOException ioe)
             {
             ioe.printStackTrace();
         }
     }

 }
}

And I printed results into output.txt file.

![output](https://cloud.githubusercontent.com/assets/17202745/22864979/f5b19190-f16b-11e6-9c40-2f2b1abf84be.png)


And then I converted these binary numbers to text from www.binarytranslator.com/ site .
I got a base64 code.

Li0gLi0uLiAuIC0uLi0gLS4tLiAtIC4uLS4gLSAuLi4uIC4tLS0tIC4uLi4uIC0tLSAuLS0tLSAuLi4gLS0tIC4uLi4uIC4uLSAuLS0uIC4uLi0tIC4tLiAtLS0gLi4uLi4gLiAtLi0uIC4tLiAuLi4tLSAtIC0tLSAtIC0uLi0gLQ== 
I decoded this base64 from www.base64decode.org site .

.- .-.. . -..- -.-. - ..-. - .... .---- ..... --- .---- ... --- ..... ..- .--. ...-- .-. --- ..... . -.-. .-. ...-- - --- - -..- - 
I got this Morse code.Then I converted this Morse code from  http://morsecode.scphillips.com/translator.html site.

The result was ALEXCTFTH15O1SO5UP3RO5ECR3TOTXT .I tried ALEXCTF{TH15O1SO5UP3RO5ECR3TOTXT} as flag but it wasn't.So I replaced O's with _'s.

And the flag was ALEXCTF{TH15_1S_5UP3R_5ECR3T_TXT}






-----------------------------------------------------------------TURKISH------------------------------------------------------------------------

Bu soruda bize içi ZERO ve ONE'larla dolu bir dosya veriliyor. Ben de öncelikle verilen ZERO ve ONE'ları 0 ve 1'lere çevirmek için aşağıdaki Java kodunu yazdım.

import java.io.*; import java.util.Scanner;

public class Oku {

 public static void main(String[] args) {

        {
         try
             {
             File file = new File("/home/compleng/Desktop/CTF/AlexCTF/crypto1/zero_one");
             BufferedReader reader = new BufferedReader(new FileReader(file));
             String line = "", oldtext = "";
             while((line = reader.readLine()) != null)
                 {
                 oldtext += line + "\r\n";
             }
             reader.close();

             String replacedtext  = oldtext.replaceAll("ZERO", "0");
             replacedtext = replacedtext.replaceAll("ONE", "1" );


             FileWriter writer = new FileWriter("/home/compleng/Desktop/CTF/AlexCTF/crypto1/output.txt");
             writer.write(replacedtext);


             writer.close();

         }
         catch (IOException ioe)
             {
             ioe.printStackTrace();
         }
     }

 }
}

Sonuçları da output.txt dosyasına bastırdım.

![output](https://cloud.githubusercontent.com/assets/17202745/22866044/83745c9c-f180-11e6-8b02-5a2843f17b85.png)


Daha sonra çıkan binary sayıları www.binarytranslator.com/ sitesinden text'e çevirdim.

Li0gLi0uLiAuIC0uLi0gLS4tLiAtIC4uLS4gLSAuLi4uIC4tLS0tIC4uLi4uIC0tLSAuLS0tLSAuLi4gLS0tIC4uLi4uIC4uLSAuLS0uIC4uLi0tIC4tLiAtLS0gLi4uLi4gLiAtLi0uIC4tLiAuLi4tLSAtIC0tLSAtIC0uLi0gLQ== şeklinde bir base64 text çıktı.Bu base64'ü de www.base64decode.org sitesinden decode ettim.

.- .-.. . -..- -.-. - ..-. - .... .---- ..... --- .---- ... --- ..... ..- .--. ...-- .-. --- ..... . -.-. .-. ...-- - --- - -..- - şeklinde Morse kodu çıktı.Daha sonra bu Morse kodu http://morsecode.scphillips.com/translator.html sitesinden çevirdiğimde

ALEXCTFTH15O1SO5UP3RO5ECR3TOTXT gibi bir text çıktı.Bunu ALEXCTF{TH15O1SO5UP3RO5ECR3TOTXT} diye denedim ancak flag bu değildi.Daha sonra O'ları _ ile değiştirerek girdim.

Ve flag ALEXCTF{TH15_1S_5UP3R_5ECR3T_TXT} olarak çıktı.
