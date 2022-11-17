<img width="959" alt="Screenshot 1" src="https://user-images.githubusercontent.com/118383947/202334610-fb1ba3a2-8f47-4e8f-8391-12a5639a91df.png">
<img width="957" alt="Screenshot 2" src="https://user-images.githubusercontent.com/118383947/202334630-4d412509-6def-4f3a-a2c9-3649034d2020.png">

# project_java
import java.time.LocalTime;
import java.util.Random;
import java.util.Scanner;
import java.util.concurrent.TimeUnit;

public class wpm {
	
	static String[] words = {"accident", "development", "exaggerate","knowlageble","fascinate", "necessary","impossible",
		"determinate","civilization","demonstrat", "envirornment","rehabiliate","utalization","describe","ingredient","guarantee",
		"hideous","lethargic","homogeneous","phenomenon","comprehend","application"};
	
    public static void main(String[] args) throws InterruptedException{
    	
	System.out.println("3");
	TimeUnit.SECONDS.sleep(1);
	
	System.out.println("2");
	TimeUnit.SECONDS.sleep(1);
	
	System.out.println("1");
	TimeUnit.SECONDS.sleep(1);
	
	Random rand = new Random();
	for(int i=0; i<15; i++) {
		System.out.print(words[rand.nextInt(14)] +" ");
		}
	System.out.println();
	
	double start = LocalTime.now().toNanoOfDay();
	
	Scanner scan = new Scanner(System.in);
		String typedWord =scan.nextLine();
		
	double end = LocalTime.now().toNanoOfDay();
	double elapsedTime = end - start;
	double seconds = elapsedTime / 1000000000.0;
	int numChars = typedWord.length();
	
	int wpm = (int)((((double) numChars / 5) / seconds) * 60);
	
	System.out.println("Your wpm is " + wpm + "!");
	
	}
		
	
}
