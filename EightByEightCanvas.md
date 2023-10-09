# Creating a 8 by 8 canvas

import javax.swing.*;
import java.awt.*;

public class EightByEightCanvas extends JPanel {

    @Override
    protected void paintComponent(Graphics g) {
        super.paintComponent(g);

        // Calculate the width and height of each cell
        int cellWidth = getWidth() / 8;
        int cellHeight = getHeight() / 8;

        // Loop through rows
        for (int row = 0; row < 8; row++) {
            // Loop through columns
            for (int col = 0; col < 8; col++) {
                // Calculate the position of the cell
                int x = col * cellWidth;
                int y = row * cellHeight;

                // Draw a rectangle for each cell
                g.drawRect(x, y, cellWidth, cellHeight);
            }
        }
    }

    public static void main(String[] args) {
        JFrame frame = new JFrame();
        EightByEightCanvas canvas = new EightByEightCanvas();

        frame.add(canvas);
        frame.setSize(400, 400);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setVisible(true);
    }
}
