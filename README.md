public class Main {
    public static void main(String[] args) {
        // First part of the program
        int x = 5;
        int y = 3;
        int arr[] = {10, 15, 20, 25, 30};
        int sumOdd = 0; // Initialize sum for odd numbers
        int sumEven = 0; // Initialize sum for even numbers
        int sum = 0;
        float avg;

        // Basic arithmetic operations
        System.out.println("Addition: " + (x + y)); // add
        System.out.println("Subtraction: " + (x - y)); // subtract
        System.out.println("Multiplication: " + (x * y)); // multiply

        // Calculate the sum of all elements in the array
        for (int i = 0; i < arr.length; i++) { 
            sum += arr[i]; // Add each element to sum
        }

        // Calculate the average
        avg = (float) sum / arr.length; // Cast to float for accurate average calculation

        System.out.println("Sum of all elements: " + sum); // Print total sum
        System.out.println("Average: " + avg); // Print average

        // Print odd numbers and their sum
        System.out.println("Odd Numbers:");  
        for (int i = 0; i < arr.length; i++) { 
            if (arr[i] % 2 != 0) {
                sumOdd += arr[i]; // Add the odd number to sumOdd
                System.out.println(arr[i]); 
            }  
        }  
        System.out.println("Sum of Odd Numbers: " + sumOdd); // Print the sum of odd numbers

        // Print even numbers and their sum
        System.out.println("Even Numbers:");  
        for (int i = 0; i < arr.length; i++) {  
            if (arr[i] % 2 == 0) {  
                sumEven += arr[i]; // Add the even number to sumEven
                System.out.println(arr[i]);  
            }  
        }  
        System.out.println("Sum of Even Numbers: " + sumEven); // Print the sum of even numbers

        // Print the total sum of both odd and even numbers
        int totalSum = sumOdd + sumEven;
        System.out.println("Total Sum of Odd and Even Numbers: " + totalSum);

        // Second part of the program
        int[] numbers = {29, 15, 37, 42, 55}; // Your array of numbers
        for (int num : numbers) {
            boolean isPrime = isPrime(num);
            if (isPrime) {
                System.out.println(num + " is a prime number.");
            } else {
                System.out.println(num + " is not a prime number.");
            }
        }
    }

    // Prime checking method
    public static boolean isPrime(int num) {
        if (num <= 1) {
            return false;
        }
        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0) {
                return false;
            }
        }
        return true;
    }
}
