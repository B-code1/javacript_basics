# 30 JavaScript Exercises for Students

1. Create a variable to store your name and display it in an alert.
// answer javascript
   let name = "John Doe";
    alert(name);

2. Declare two number variables and show their sum, difference, product, and quotient.
// answer javascript
let num1 = 10;
let num2 = 5;
console.log(num1 + num2);
console.log(num1 - num2);
console.log(num1 * num2);
console.log(num1 / num2);


3. Write a program that converts Celsius to Fahrenheit.
// answer javascript
let celsius = 30;
let fahrenheit = (celsius * 9/5) + 32;
console.log(fahrenheit);


4. Create a program that calculates the area of a rectangle using variables for length and width.
// answer javascript
let length = 10;
let width = 5;
let area = length * width;
console.log(area);


5. Write code that checks if a number is even or odd and displays the result.
// answer javascript
let num = 10;
if (num % 2 === 0) {
    console.log("The number is even.");
    } 
    else {
        console.log("The number is odd.");
        }


6. Create a program that determines if a year entered is a leap year.
// answer javascript
let year = 2020;
if (year % 4 === 0) {
    if (year % 100 === 0) {
        if (year % 400 === 0) {
            console.log(year + " is a leap year.");
            } else {
                console.log(year + " is not a leap year.");
                }
                } else {
                    console.log(year + " is a leap year.");
                    }
                    } else {
                        console.log(year + " is not a leap year.");
                        }
                        

7. Write a function that returns the reverse of a string input.
// answer javascript 
function reverseString(str) {
    return str.split("").reverse().join("");
    }

8. Create a function that counts the number of vowels in a string.
// answer javascript
function countVowels(str) {
    let count = 0;
    for (let i = 0; i < str.length; i++) {
        if (str[i].toLowerCase() === 'a' || str[i].toLowerCase() === ''e' 
        || str[i].toLowerCase() === 'i' || str[i].toLowerCase() === 'o
        || str[i].toLowerCase() === 'u') 
        {
            count++;
            }
            }
            return count;
            }

9. Write a program that finds the largest number in an array of 5 numbers.
// answer javascript
let numbers = [1, 2, 3, 4, 5];
let max = numbers[0];
for (let i = 1; i < numbers.length; i++) {
    if (numbers[i] > max) {
        max = numbers[i];
        }
        }

10. Create a function that checks if a string is a palindrome.
// answer javascript
function isPalindrome(str) {
    str = str.toLowerCase();
    let reversed = str.split("").reverse().join("");
    if (str === reversed) {
        return true;
        } 
        else {
            return false;
            }
            }

11. Write code that calculates the factorial of a number.
// answer javascript
function factorial(n) {
    if (n === 0) {
        return 1;
        }
        else {
            return n * factorial(n - 1);
            }
            }

12. Create a function that generates a random number between two given values.
// answer javascript
function randomNum(min, max) {
    return Math.floor(Math.random() * (max - min + 1)) + min;
    }
    

13. Write a program that converts a number of seconds into hours, minutes, and seconds.
// answer javascript
function convertSeconds(seconds) {
    let hours = Math.floor(seconds / 3600);
    let minutes = Math.floor((seconds % 3600) / 60);
    let seconds = seconds % 60;
    return hours + ":" + minutes + ":" + seconds;
    }

14. Create a program that checks if a number is prime.
// answer javascript
function isPrime(num) {
    if (num <= 1) {
        return false;
        }
        for (let i = 2; i <= Math.sqrt(num); i++) {
            if (num % i === 0) {
                return false;
                }
                }
                return true;
                }

15. Write a function that capitalizes the first letter of each word in a sentence.
// answer javascript
function capitalizeWords(sentence) {
    return sentence.split(" ").map(word => word.charAt(0).toUpperCase() + word.slice(
        1).toLowerCase()).join(" ");
        }


16. Create a program that calculates the sum of all numbers from 1 to n.
// answer javascript
function sumNumbers(n) {
    let sum = 0;
    for (let i = 1; i <= n; i++) {
        sum += i;
        }
        return sum;
        }


17. Write code that finds the average of numbers in an array.
// answer javascript
function averageNumbers(arr) {
    let sum = 0;
    for (let num of arr) {
        sum += num;
        }
        return sum / arr.length;
        }

18. Create a function that removes duplicate values from an array.
// answer javascript
function removeDuplicates(arr) {
    return [...new Set(arr)];
    }

19. Write a program that counts down from 10 to 1, then displays "Blast off!".
// answer javascript
function countdown() {
    for (let i = 10; i >= 1; i--) {
        console.log(i);
        }
        console.log("Blast off!");
        }

20. Create a function that determines if a string contains only numbers.
// answer javascript
function containsOnlyNumbers(str) {
    return /^\d+$/.test(str);
    }


21. Write code that finds the second smallest number in an array.
// answer javascript
function secondSmallest(arr) {
    arr.sort((a, b) => a - b);
    return arr[1];
    }



22. Create a program that displays the multiplication table for a given number.
// answer javascript
function multiplicationTable(num) {
    for (let i = 1; i <= 10; i++) {
        console.log(`${num} x ${i} = ${num * i}`);
        }
        }


23. Write a function that validates if a password meets specific criteria (at least 8 characters, one uppercase, one lowercase, one number).
// answer javascript
function validatePassword(password) {
    if (password.length < 8) {
        return false;
        }
        if (!/[A-Z]/.test(password)) {
            return false;
            }
            if (!/[a-z]/.test(password)) {
                return false;
                }
                if (!/\d/.test(password)) {
                    return false;
                    }
                    return true;
                    }


24. Create code that simulates a simple calculator with basic operations.
// answer javascript
function calculator() {
    let num1 = parseFloat(prompt("Enter first number: "));
    let operator = prompt("Enter operator (+, -, *, /): ");
    let num2 = parseFloat(prompt("Enter second number: "));

    if (operator === "+") {
        console.log(num1 + " + " + num2 + " = " + (num1 + num2));
    } else if (operator === "-") {
        console.log(num1 + " - " + num2 + " = " + (num1 - num2));
    } else if (operator === "*") {
        console.log(num1 + " * " + num2 + " = " + (num1 * num2));
    } else if (operator === "/") {
        if (num2 !== 0) {
            console.log(num1 + " / " + num2 + " = " + (num1 / num2));
        } else {
            console.log("Error: Division by zero is not allowed.");
        }
    } else {
        console.log("Error: Invalid operator.");
    }
}


25. Write a program that finds all factors of a given number.
// answer javascript
function findFactors(num) {
    let factors = [];
    for (let i = 1; i <= num; i++) {
        if (num % i === 0) {
            factors.push(i);
        }
    }
    return factors;
}



26. Create a function that checks if two strings are anagrams.
// answer javascript
function areAnagrams(str1, str2) {
    str1 = str1.toLowerCase().replace(/\s/g, '');
    str2 = str2.toLowerCase().replace(/\s/g, '');
    return str1.split('').sort().join('') === str2.split('').sort().join('');
}

27. Write a program that generates the Fibonacci sequence up to n terms.
// answer javascript
function fibonacci(n) {
    let fibSequence = [0, 1];
    while (fibSequence.length < n) {
        fibSequence.push(fibSequence[fibSequence.length - 1] + fibSequence[fibSequence.length - 2]);
    }
    return fibSequence;
}

28. Create code that sorts an array of numbers without using the built-in sort method.
// answer javascript
function sortArray(arr) {
    for (let i = 0; i < arr.length; i++) {
        for (let j = i + 1; j < arr.length; j++) {
            if (arr[i] > arr[j]) {
                let temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }
        }
    }
    return arr;
}


29. Write a function that counts how many times a specific element appears in an array.
// answer javascript
function countElement(arr, element) {
    let count = 0;
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] === element) {
            count++;
        }
    }
    return count;
}



30. Create a shopping cart program where users can add items, remove items, and calculate the total price.
// answer javascript
class ShoppingCart {
    constructor() {
        this.items = [];
    }

    addItem(name, price, quantity) {
        let item = {
            name: name,
            price: price,
            quantity: quantity
        };
        this.items.push(item);
    }

    removeItem(name) {
        for (let i = 0; i < this.items.length; i++) {
            if (this.items[i].name === name) {
                this.items.splice(i, 1);
                break;
            }
        }
    }

    calculateTotal() {
        let total = 0;
        for (let i = 0; i < this.items.length; i++) {
            total += this.items[i].price * this.items[i].quantity;
        }
        return total;
    }

    displayCart() {
        console.log("Shopping Cart:");
        for (let i = 0; i < this.items.length; i++) {
            console.log(`${this.items[i].name} x ${this.items[i].quantity} = $${this.items[i].price * this.items[i].quantity}`);
        }
        console.log(`Total: $${this.calculateTotal()}`);
    }
}
let cart = new ShoppingCart();
cart.addItem("Apple", 1.00, 2);
cart.addItem("Banana", 0.50, 3);
cart.displayCart();
cart.removeItem("Apple");
cart.displayCart();
