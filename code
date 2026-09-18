package library;

import library.service.LibraryService;
import library.storage.DataManager;
import library.util.InputValidator;

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        DataManager dataManager = new DataManager("data");
        LibraryService library = new LibraryService(dataManager);
        InputValidator input = new InputValidator(scanner);

        library.loadData();

        System.out.println("==============================================");
        System.out.println("      LIBRARY MANAGEMENT SYSTEM");
        System.out.println("==============================================");
        System.out.println("Data folder: " + dataManager.getDataDirectory());

        boolean running = true;
        while (running) {
            printMainMenu();
            int choice = input.readInt("Enter choice: ", 1, 10);

            switch (choice) {
                case 1 -> library.addBook(input);
                case 2 -> library.viewBooks();
                case 3 -> library.searchBook(input);
                case 4 -> library.addStudent(input);
                case 5 -> library.viewStudents();
                case 6 -> library.issueBook(input);
                case 7 -> library.returnBook(input);
                case 8 -> library.viewBorrowingHistory(input);
                case 9 -> library.reports();
                case 10 -> {
                    library.saveData();
                    System.out.println("Data saved. Goodbye!");
                    running = false;
                }
            }
        }
        scanner.close();
    }

    private static void printMainMenu() {
        System.out.println("\n--------------- MAIN MENU ----------------");
        System.out.println("1. Add Book");
        System.out.println("2. View All Books");
        System.out.println("3. Search Book / Check Status");
        System.out.println("4. Register Student");
        System.out.println("5. View All Students");
        System.out.println("6. Issue Book");
        System.out.println("7. Return Book");
        System.out.println("8. Borrowing History");
        System.out.println("9. Reports & Fine Summary");
        System.out.println("10. Save & Exit");
        System.out.println("------------------------------------------");
    }
}
