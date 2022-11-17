<img width="960" alt="Screenshot 2022-11-17 070856" src="https://user-images.githubusercontent.com/118383947/202333126-02a6d8ea-3dde-4ac2-8ac1-80096d1cd040.png">
<img width="960" alt="Screenshot 2022-11-17 070926" src="https://user-images.githubusercontent.com/118383947/202333153-ea6b8f61-ded2-40c8-9c26-809d997d93f3.png">
# project_java
import java.time.LocalTime;
import java.util.Random;
import java.util.Scanner;
import java.util.concurrent.TimeUnit;

public class wpm {
	
	static String[] words = {"car","night","walk","music","things","sleep","food","fun"};
	
    public static void main(String[] args) throws InterruptedException{
    	
	System.out.println("3");
	TimeUnit.SECONDS.sleep(1);
	
	System.out.println("2");
	TimeUnit.SECONDS.sleep(1);
	
	System.out.println("1");
	TimeUnit.SECONDS.sleep(1);
	
	Random rand = new Random();
	for(int i=0; i<8; i++) {
		System.out.print(words[rand.nextInt(7)] +" ");
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
