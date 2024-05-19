public class VU2 {
    // Method to calculate total pay for an employee
    public static void calculatePay(double basePay, int hoursWorked) {
        // Check if base pay is less than the minimum wage
        if (basePay < 40000) {
            System.out.println("Error: Base pay cannot be less than UGX40,000 an hour.");
            return;
        }
        
        // Check if hours worked is greater than 60
        if (hoursWorked > 60) {
            System.out.println("Error: An employee cannot work more than 60 hours in a week.");
            return;
        }
        
        // Calculate total pay
        double totalPay;
        if (hoursWorked <= 40) {
            totalPay = hoursWorked * basePay;
        } else {
            // Calculate regular pay for 40 hours
            double regularPay = 40 * basePay;
            // Calculate overtime pay for hours over 40
            double overtimePay = (hoursWorked - 40) * (basePay * 1.5);
            // Total pay is the sum of regular pay and overtime pay
            totalPay = regularPay + overtimePay;
        }
        
        // Print total pay
        System.out.println("Total pay: UGX" + totalPay);
    }
    
    public static void main(String[] args) {
        // Employee A
        System.out.println("Employee A:");
        calculatePay(28000.00, 35);
        
        // Employee B
        System.out.println("\nEmployee B:");
        calculatePay(35000.00, 45);
        
        // Employee C
        System.out.println("\nEmployee C:");
        calculatePay(38000.00, 75);
        
        // Employee D
        System.out.println("\nEmployee D:");
        calculatePay(40000.00, 55);
    }
}
