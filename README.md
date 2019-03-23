# ThreeBrothers

import java.util.Scanner;

public class P25_ThreeBrothers {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        double brat1 = Double.parseDouble(scanner.nextLine());
        double brat2 = Double.parseDouble(scanner.nextLine());
        double brat3 = Double.parseDouble(scanner.nextLine());
        double bashtaFishing = Double.parseDouble(scanner.nextLine());

        double cleaning = 1 / ( 1/ brat1 + 1 / brat2 + 1 / brat3);

        double cleaningWithRest = cleaning + cleaning * 15 / 100.0 ;

        if (bashtaFishing < cleaningWithRest) {
            System.out.printf("Cleaning time: %.2f\n", cleaningWithRest);
            System.out.printf("No, there isn't a surprise - " + "shortage of time -> %f hours.",
                    Math.floor(cleaningWithRest - bashtaFishing));
        } else {
            System.out.printf("Cleaning time: %.2f\n", cleaningWithRest);
            System.out.printf("Yes, there is a surprise - " + "time left -> %.0f hours." ,
                    Math.floor(bashtaFishing - cleaningWithRest));
        }






    }
}
