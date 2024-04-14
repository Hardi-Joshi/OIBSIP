# Number Guessing Game
@OasisInfobyte Java Development Internship
```java
import java.util.Random;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        Random random = new Random();
        int count = 0;
        int game = 0;
        int score = 0;
        
        while (1 == 1) {
            game++;
            System.out.print("Guess The Number: ");
            int correct = random.nextInt(100) + 1;
            int a = 1;
            
            while (a < 6) {
                int number = in.nextInt();
                
                if (number > correct) {
                    System.out.println("Nopes! Go lower");
                } else if (number < correct) {
                    System.out.println("Nopes! Go higher");
                }
                
                if (number == correct) {
                    System.out.println("Yayy! You got it Correct!");
                    count++;
                    
                    switch (a) {
                        case 1:
                            score += 5;
                            break;
                        case 2:
                            score += 4;
                            break;
                        case 3:
                            score += 3;
                            break;
                        case 4:
                            score += 2;
                            break;
                        default:
                            score++;
                    }
                    
                    break;
                }
                a++;
            }
            
            System.out.println("Number was: " + correct);
            System.out.println("Play again?\n1->yes or 2->no or 3->view your score");
            int i = in.nextInt();
            
            if (i == 2) {
                System.exit(0);
            } else if (i == 3) {
                System.out.println("You won " + count + " out of " + game + " games.\nScore = " + score);
                System.exit(0);
            }
        }
    }
}
```

