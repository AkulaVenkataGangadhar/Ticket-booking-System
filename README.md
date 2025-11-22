
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class TicketBookingSystem {
    static Scanner sc = new Scanner(System.in);
    static boolean[] seats = new boolean[40];
    static String[] seatType = {"Regular", "Sleeper", "AC"};
    static int[] seatPrice = {450, 700, 1000};

    public static void main(String[] args) {
        int choice;
        do {
            System.out.println("\n=================================");
            System.out.println("     TICKET BOOKING SYSTEM  ");
            System.out.println("=================================");
            System.out.println("1. View Seats");
            System.out.println("2. Book Ticket");
            System.out.println("3. Cancel Ticket");
            System.out.println("4. Exit");
            System.out.print("Enter your choice: ");

            choice = getIntInput();

            switch (choice) {
                case 1 -> viewSeats();
                case 2 -> bookTicket();
                case 3 -> cancelTicket();
                case 4 -> System.out.println("Thank you for using Ticket Booking System!");
                default -> System.out.println("Invalid choice! Try again.");
            }
        } while (choice != 4);
    }

    static void viewSeats() {
        System.out.println("\nSeat Availability:");
        for (int i = 0; i < seats.length; i++) {
            System.out.println("Seat " + (i + 1) + ": " + (seats[i] ? "BOOKED" : "AVAILABLE"));
        }
    }

    static void bookTicket() {
        try {
            System.out.print("Enter seat number (1-40) to book: ");
            int seatNo = getIntInput();

            if (seatNo < 1 || seatNo > 40)
                throw new IllegalArgumentException("Invalid seat number! Choose between 1–40.");

            if (seats[seatNo - 1]) {
                System.out.println("Seat already booked!");
                return;
            }

            System.out.println("\nChoose Seat Type:");
            for (int i = 0; i < seatType.length; i++) {
                System.out.println((i + 1) + ". " + seatType[i] + " - ₹" + seatPrice[i]);
            }
            System.out.print("Enter seat type (1-3): ");
            int typeChoice = getIntInput();

            if (typeChoice < 1 || typeChoice > seatType.length)
                throw new IllegalArgumentException("Invalid seat type selection!");

            int price = seatPrice[typeChoice - 1];
            String type = seatType[typeChoice - 1];
            seats[seatNo - 1] = true;

            System.out.println("\nSeat " + seatNo + " (" + type + ") booked successfully!");
            System.out.println("Total price: ₹" + price);

            saveBookingToFile(seatNo, type, price);

        } catch (Exception e) {
            System.out.println("Error: " + e.getMessage());
        }
    }

    static void cancelTicket() {
        try {
            System.out.print("\nEnter seat number (1-40) to cancel: ");
            int seatNo = getIntInput();

            if (seatNo < 1 || seatNo > 40) {
                System.out.println("Invalid seat number!");
                return;
            }

            if (!seats[seatNo - 1]) {
                System.out.println("Seat is not booked yet!");
                return;
            }

            // Apply ₹100 cancellation fee
            System.out.println("Cancelling booking for seat " + seatNo + "...");
            System.out.println("Cancellation successful! ₹100 will be deducted as a cancellation charge.");
            System.out.println("Refund Amount: ₹" + calculateRefund(seatNo));

            seats[seatNo - 1] = false;
            saveCancellationToFile(seatNo);

        } catch (Exception e) {
            System.out.println("Error: " + e.getMessage());
        }
    }

    static int calculateRefund(int seatNo) {
        // Assume refund based on seat type
        int typeIndex = (seatNo - 1) % seatType.length; // simple assumption
        int originalPrice = seatPrice[typeIndex];
        int refundAmount = Math.max(0, originalPrice - 100);
        return refundAmount;
    }

    static void saveBookingToFile(int seatNo, String type, int price) {
        try (FileWriter fw = new FileWriter("bookings.txt", true)) {
            fw.write("Seat " + seatNo + " (" + type + ") booked. Price: ₹" + price + "\n");
        } catch (IOException e) {
            System.out.println("Error saving booking: " + e.getMessage());
        }
    }

    static void saveCancellationToFile(int seatNo) {
        try (FileWriter fw = new FileWriter("bookings.txt", true)) {
            fw.write("Seat " + seatNo + " booking cancelled. ₹100 cancellation charge applied.\n");
        } catch (IOException e) {
            System.out.println("Error saving cancellation: " + e.getMessage());
        }
    }

    static int getIntInput() {
        while (true) {
            try {
                return Integer.parseInt(sc.nextLine());
            } catch (NumberFormatException e) {
                System.out.print("Invalid input! Enter a valid number: ");
            }
        }
    }
}
