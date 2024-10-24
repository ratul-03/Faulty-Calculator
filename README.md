# Faulty Calculator

This project is a basic web-based calculator that introduces intentional errors to provide incorrect results with a 10% probability.

## Features

- Prompts the user to input two numbers and a mathematical operation.
- Calculates and displays the result.
- Intentionally provides a faulty result 10% of the time by switching the operation.

## Requirements

- Modern web browser (Chrome, Firefox, Safari, etc.)

## Installation

1. Clone this repository or download the `index.html` file.
2. Open the `index.html` file in your web browser.

## Usage

1. Open the `index.html` file in your web browser.
2. Enter the first number when prompted.
3. Enter the second number when prompted.
4. Enter the operation (`+`, `-`, `*`, `/`) when prompted.
5. The result will be displayed. There is a 10% chance that the result will be intentionally faulty by changing the operation.

## Code Explanation

The main script `index.html` includes:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Excersise 10</title>
</head>
<body>
    <script>
        let random = Math.random();
        let prompt1 = prompt("Enter first number");
        let prompt2 = prompt("Enter second number");
        let prompt3 = prompt("Enter the operation");

        let obj1 = {
            "+": "-",
            "*": "+",
            "/": "*",
            "-": "/"
        }

        if (random > 0.1) {
            alert(`The result is ${eval(`${prompt1} ${prompt3} ${prompt2}`)}`);
            console.log(`The result is ${eval(`${prompt1} ${prompt3} ${prompt2}`)}`);
        } else {
            prompt3 = obj1[prompt3];
            alert(`The result is ${eval(`${prompt1} ${prompt3} ${prompt2}`)}`);
            console.log(`The result is ${eval(`${prompt1} ${prompt3} ${prompt2}`)}`);
        }
    </script>
</body>
</html>
```
## Contributing
Feel free to fork this repository and contribute by submitting a pull request. Any improvements or new features are welcome!

## License
This project is licensed under the MIT License.
