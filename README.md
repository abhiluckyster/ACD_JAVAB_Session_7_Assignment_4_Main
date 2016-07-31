# ACD_JAVAB_Session_7_Assignment_4_Main

package exceptionHandling;
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class StringIndexOutOfBoundExceptionClass {
	
	public static void main(String[] args) throws IOException {
			
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		System.out.println("Please enter your string");
		String s = br.readLine();
		System.out.println("String is : "+s);
		int upperCase=0;
		int lowerCase=0;
		int number=0;
		int specialCase=0;
		int whiteSpace=0;
		try{
		for (int i=0; i<=s.length();i++){
			
			char ch = s.charAt(i);
			if(Character.isAlphabetic(ch))
			{
				if(Character.isLowerCase(ch))
					lowerCase++;
				else
					upperCase++;
			}
			else if(Character.isDigit(ch)){
				number++;
			}
			else if(Character.isSpaceChar(ch)){
				whiteSpace++;
			}
			else
				specialCase++;
			}
		}catch(StringIndexOutOfBoundsException  e){
				System.out.println("Exception is : "+e);}
		System.out.println("upperCase "+upperCase);
		System.out.println("lowerCase "+lowerCase);
		System.out.println("number "+number);
		System.out.println("specialCase "+specialCase);
		System.out.println("whiteSpace "+whiteSpace);
  }
 }
