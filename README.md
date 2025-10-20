# jfreechart

A 2D chart library for Java applications (JavaFX, Swing or server-side).

## Key Features & Benefits

*   **Versatile Charting:** Supports a wide variety of chart types, including bar charts, pie charts, line charts, scatter plots, time series charts, and more.
*   **Java Compatibility:** Works seamlessly with Java applications, whether built with JavaFX, Swing, or used in server-side environments.
*   **Customization:** Offers extensive customization options for chart appearance, data representation, and interactive features.
*   **Easy Integration:** Simple API for integrating charts into your Java projects.
*   **Data Handling:** Designed for handling various data formats efficiently.
*   **Open Source:** Licensed under the LGPL, making it suitable for both commercial and non-commercial projects.

## Prerequisites & Dependencies

*   **Java Development Kit (JDK):** Version 8 or later is recommended.
*   **Maven:** For build management and dependency resolution (optional, but recommended).

## Installation & Setup Instructions

### Using Maven (Recommended)

1.  Add the jfreechart dependency to your `pom.xml` file:

    ```xml
    <dependency>
        <groupId>org.jfree</groupId>
        <artifactId>jfreechart</artifactId>
        <version>1.5.4</version> <!-- Replace with the latest version -->
    </dependency>
    ```

2.  Maven will automatically download and manage the jfreechart library and its dependencies.

### Manual Installation

1.  Download the jfreechart JAR file from a trusted source (e.g., Maven Central).
2.  Add the JAR file to your project's classpath.

## Usage Examples & API Documentation

Here's a simple example of creating a basic bar chart using jfreechart:

```java
import org.jfree.chart.ChartFactory;
import org.jfree.chart.ChartPanel;
import org.jfree.chart.JFreeChart;
import org.jfree.data.category.DefaultCategoryDataset;

import javax.swing.JFrame;
import javax.swing.SwingUtilities;

public class BarChartExample extends JFrame {

    public BarChartExample(String title) {
        super(title);
        // Create dataset
        DefaultCategoryDataset dataset = new DefaultCategoryDataset();
        dataset.addValue(20, "Sales", "January");
        dataset.addValue(15, "Sales", "February");
        dataset.addValue(25, "Sales", "March");

        // Create chart
        JFreeChart chart = ChartFactory.createBarChart(
                "Monthly Sales", // Chart title
                "Month", // Category axis label
                "Sales", // Value axis label
                dataset);

        // Create Panel
        ChartPanel panel = new ChartPanel(chart);
        setContentPane(panel);
    }

    public static void main(String[] args) {
        SwingUtilities.invokeLater(() -> {
            BarChartExample example = new BarChartExample("Bar Chart Example");
            example.setSize(800, 600);
            example.setLocationRelativeTo(null);
            example.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
            example.setVisible(true);
        });
    }
}
```

For more detailed API documentation, refer to the official jfreechart documentation: [JFreeChart Documentation](https://www.jfree.org/jfreechart/) (Replace with actual documentation link if available)

## Configuration Options

jfreechart offers a multitude of configuration options, allowing you to customize every aspect of your charts.  These options can be set using the API when creating and modifying chart objects. Examples include:

*   **Chart Titles:** Set the main title, subtitle, and font properties.
*   **Axis Labels:** Customize axis labels, ranges, and tick marks.
*   **Colors & Styles:** Adjust colors, fonts, line styles, and fill patterns for chart elements.
*   **Legend:** Configure the legend's position, appearance, and item labels.
*   **Tooltips:** Add interactive tooltips to data points.
*   **Data Rendering:** Control how data is visualized (e.g., bar styles, line smoothing).

## Contributing Guidelines

We welcome contributions to jfreechart! If you'd like to contribute, please follow these guidelines:

1.  **Fork the repository** on GitHub.
2.  **Create a new branch** for your feature or bug fix.
3.  **Write clear, concise code** with appropriate comments.
4.  **Test your changes** thoroughly.
5.  **Submit a pull request** to the main repository.

Please ensure your pull request includes:

*   A clear description of the changes.
*   Relevant test cases.
*   Adherence to the project's coding style.

## License Information

This project is licensed under the GNU Lesser General Public License v2.1.  See the `licence-LGPL.txt` file for more details.

## Acknowledgments

*   This project uses GitHub Actions for continuous integration.
