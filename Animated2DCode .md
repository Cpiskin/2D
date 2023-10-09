# The code to do the animations

public class Animated2DCode {

    public static void main(String[] args) throws InterruptedException {
        int frameCount = 10;
        int animationDelay = 100; // Delay between frames in milliseconds

        for (int frame = 1; frame <= frameCount; frame++) {
            clearScreen(); // Clears the console for a clean animation
            System.out.println("Frame " + frame);
            int row = 1;

            // Loop for rows
            while (row <= 5) {
                int col = 1;

                // Loop for columns
                while (col <= 10) {
                    if (row == 1 || row == 5 || col == 1 || col == 10) {
                        System.out.print(" * "); // Print '*' for borders
                    } else {
                        System.out.print("   "); // Print spaces for inner area
                    }
                    col++;
                }

                System.out.println(); // Move to the next line
                row++;
            }

            Thread.sleep(animationDelay); // Adds a delay between frames
        }
    }

    // Function to clear the console screen
    public static void clearScreen() {
        System.out.print("\033[H\033[2J");
        System.out.flush();
    }
}
