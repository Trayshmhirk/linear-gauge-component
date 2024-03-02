# Linear Gauge

## Overview

The Linear gauge is a web component designed to visually represent drug concentration levels within a given range. It features a linear gauge that displays different categories of drug concentration, such as "good", "mid", and "bad", along with pointers indicating specific concentration levels. The dashboard is built with HTML, CSS, and JavaScript, aiming to provide a clear and interactive visualization tool for drug concentration analysis.

## Features

-  **Dynamic Range Visualization**: Easily display drug concentration ranges with customizable colors for different categories.
-  **Pointer Indication**: Indicate specific drug concentration levels with customizable pointers.
-  **Tooltip Information**: Display detailed information about the concentration level on hover, including normal range and category.
-  **Responsive Design**: Ensures the dashboard looks great on all devices.

## Screenshot

![](/linear-gauge-component/img/linear%20gauge%20image.png)

## Installation

To use the Linear Gauge component in your project, simply copy the HTML, CSS, and JavaScript code provided in this repository into your project files. There are no external dependencies required.

## Usage

1. **Include the Component in Your HTML**: Add the `<div id="app" class="App"></div>` element to your HTML file where you want the dashboard to appear.

2. **Initialize the Linear Gauge**: Call the `DrugComponent` function and assign its return value to the `innerHTML` of the `app` div.

3. **Customize the Linear gauge**: Modify the `drugs` array in the `DrugComponent` function to include your specific drug concentration ranges and pointers.

## Examples

The `DrugComponent` function accepts an array of `drugs`, each with its own `ranges` and `pointers`. Here's an example of how to define a drug with its ranges and pointers:

```Javascript
   const drugs = [
      {
         ranges: [
            { start: 0, end: 40, category: "bad" },
            { start: 40, end: 95, category: "mid" },
            { start: 95, end: 500, category: "good" },
            { start: 500, end: 650, category: "mid" },
            { start: 650, end: 800, category: "bad" },
         ],
         pointers: [
            {
               value: 350,
               color: "#948c92",
               rangeType: "Neutral",
               rangeTypeColor: "orange",
            },
            {
               value: 500,
               color: "#3b61bb",
               rangeType: "Healthy",
               rangeTypeColor: "#4cdfbb",
            },
            {
               value: 750,
               color: "",
               rangeType: "UNHEALTHY",
               rangeTypeColor: "red",
            },
         ],
      },
   ];
```

## Contributing

Contributions are welcome! If you find a bug, want to suggest a new feature, or have any other inquiries, please open an issue. For contributions, please follow these steps:

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -am 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a Pull Request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
