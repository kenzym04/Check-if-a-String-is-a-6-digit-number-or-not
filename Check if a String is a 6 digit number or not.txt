import java.util.regex.Pattern;
/**
 * Java program to demonstrate use of Regular Expression to check
 * if a String is a 6 digit number or not.
 */
public class RegularExpressionExample {
 
    public static void main(String args[]) {
     
        // Regular expression in Java to check if String is number or not
        Pattern pattern = Pattern.compile(".*[^0-9].*");
       //Pattern pattern = Pattern.compile(".*\\D.*");
       String [] inputs = {"123", "-123" , "123.12", "abcd123"};
     
       for(String input: inputs){
           System.out.println( "does " + input + " is number : "
                                + !pattern.matcher(input).matches());
       }
     
       // Regular expression in java to check if String is 6 digit number or not
       String [] numbers = {"123", "1234" , "123.12", "abcd123", "123456"};
       Pattern digitPattern = Pattern.compile("\\d{6}");       
       //Pattern digitPattern = Pattern.compile("\\d\\d\\d\\d\\d\\d");
       

       for(String number: numbers){
           System.out.println( "does " + number + " is 6 digit number : "
                               + digitPattern.matcher(number).matches());
       }
    }
 
}