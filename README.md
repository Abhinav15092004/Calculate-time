# Calculate-time
import java.util.Scanner;

class TimeCalculator {
    private double distance;
    private double speed;

    public TimeCalculator(double distance, double speed) {
        this.distance = distance;
        this.speed = speed;
    }

    public double calculateTime() {
        return distance / speed;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the distance traveled (in units): ");
        double distance = scanner.nextDouble();

        System.out.print("Enter the speed (in units per hour): ");
        double speed = scanner.nextDouble();

        TimeCalculator calculator = new TimeCalculator(distance, speed);

        double time = calculator.calculateTime();

        System.out.println("Time taken = " + time + " hours");

        scanner.close();
    }
}
