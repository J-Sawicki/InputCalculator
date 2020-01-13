//# InputCalculator
//A simple program that shows sum and average of user inputted numbers.

import java.util.Scanner;

public class InputCalculator {
    public static void inputThenPrintSumAndAverage (){
        Scanner scanner = new Scanner(System.in);
        long sum = 0;
        int count = 0;
        double average;
        while (true){
            if (!scanner.hasNextInt()){
                break;
            }
            int number = scanner.nextInt();
            scanner.nextLine();
            sum += number;
            count ++;
        }
        average = ((double)(sum)/count);
        System.out.println("SUM = " + sum + " AVG = " + Math.round(average));
        scanner.close();
    }
}
