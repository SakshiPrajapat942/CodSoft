import java.util.Scanner;

public class StudentGradeCalculator {

    public static String calculateGrade(double averagePercentage) {
        if (averagePercentage >= 90) {
            return "A+";
        } else if (averagePercentage >= 80) {
            return "A";
        } else if (averagePercentage >= 70) {
            return "B";
        } else if (averagePercentage >= 60) {
            return "C";
        } else if (averagePercentage >= 50) {
            return "D";
        } else {
            return "F";
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("STUDENT GRADE CALCULATOR");

        // Input the number of subjects
        System.out.print("Enter the number of subjects: ");
        int subjects = scanner.nextInt();
        double[] marks = new double[subjects];

        // Input marks for each subject
        for (int i = 0; i < subjects; i++) {
            while (true) {
                System.out.print("Enter marks obtained in subject " + (i + 1) + " (out of 100): ");
                double mark = scanner.nextDouble();
                if (mark >= 0 && mark <= 100) {
                    marks[i] = mark;
                    break;
                } else {
                    System.out.println("Please enter a valid mark (0 to 100).");
                }
            }
        }

        // Calculate total marks and average percentage
        double totalMarks = 0;
        for (double mark : marks) {
            totalMarks += mark;
        }
        double averagePercentage = totalMarks / subjects;

        // Grade calculation
        String grade = calculateGrade(averagePercentage);

        // Display results
        System.out.println("\nResults:");
        System.out.printf("Total Marks: %.2f out of %.2f%n", totalMarks, subjects * 100);
        System.out.printf("Average Percentage: %.2f%%%n", averagePercentage);
        System.out.println("Grade: " + grade);

        scanner.close();
    }
}
