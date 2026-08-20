# CSP P4 Checkpoint Week 1 Sprint 1 — Bitcoin Portfolio Analyzer

## Project Idea

For this checkpoint, I created a **Bitcoin Portfolio Analyzer** that calculates the value of a Bitcoin portfolio and compares the current Bitcoin price to a list of previous prices.

The goal is to practice translating the same algorithm between **College Board pseudocode, Python, and JavaScript** while keeping the Bitcoin theme consistent.

## Question

> How can a program use Bitcoin ownership and historical price data to calculate a portfolio's value and determine how the current Bitcoin price compares to previous prices?

The program uses sample values that can be changed before running each code cell.

---

# College Board Pseudocode

This version uses College Board pseudocode to represent the main algorithm.

```text
bitcoinOwned ← 0.5
currentPrice ← 70000

previousPrices ← [62000, 65000, 68000, 70000]

PROCEDURE GET_AVERAGE(prices)
{
    total ← 0

    FOR EACH price IN prices
    {
        total ← total + price
    }

    average ← total / LENGTH(prices)

    RETURN(average)
}

portfolioValue ← bitcoinOwned * currentPrice
averagePrice ← GET_AVERAGE(previousPrices)

DISPLAY("Bitcoin owned: " + bitcoinOwned)
DISPLAY("Current Bitcoin price: $" + currentPrice)
DISPLAY("Portfolio value: $" + portfolioValue)
DISPLAY("Average previous price: $" + averagePrice)

IF (currentPrice > averagePrice)
{
    DISPLAY("The current Bitcoin price is above the historical average.")
}
ELSE
{
    DISPLAY("The current Bitcoin price is at or below the historical average.")
}
```

### What the pseudocode does

1. Stores the amount of Bitcoin owned.
2. Stores the current Bitcoin price.
3. Uses a list to hold previous Bitcoin prices.
4. Loops through the list to calculate the total.
5. Uses a procedure to calculate and return the average price.
6. Calculates the value of the Bitcoin portfolio.
7. Uses selection to compare the current price with the historical average.
8. Displays the results.

---

# CPT Work from CB Pseudocode to Python

The College Board pseudocode can be translated into Python while keeping the same algorithm.

```python
# Values that can be changed before running
bitcoin_owned = 0.5
current_price = 70000

# Previous Bitcoin prices
previous_prices = [62000, 65000, 68000, 70000]


def get_average(prices):
    total = 0

    for price in prices:
        total += price

    average = total / len(prices)

    return average


portfolio_value = bitcoin_owned * current_price
average_price = get_average(previous_prices)

print("Bitcoin owned:", bitcoin_owned)
print("Current Bitcoin price: $", current_price)
print("Portfolio value: $", round(portfolio_value, 2))
print("Average previous price: $", round(average_price, 2))

if current_price > average_price:
    print("The current Bitcoin price is above the historical average.")
else:
    print("The current Bitcoin price is at or below the historical average.")
```

### CB Pseudocode → Python

| College Board | Python |
|---|---|
| `←` | `=` |
| `DISPLAY()` | `print()` |
| `PROCEDURE` | `def` |
| `RETURN()` | `return` |
| `LENGTH(prices)` | `len(prices)` |
| `FOR EACH` | `for...in` |
| `IF / ELSE` | `if / else` |

---

# CPT Work from CB Pseudocode to JavaScript

The same algorithm can also be translated into JavaScript while keeping the same logic.

```javascript
// Values that can be changed before running
const bitcoinOwned = 0.5;
const currentPrice = 70000;

// Previous Bitcoin prices
const previousPrices = [62000, 65000, 68000, 70000];

function getAverage(prices) {
    let total = 0;

    for (const price of prices) {
        total += price;
    }

    const average = total / prices.length;

    return average;
}

const portfolioValue = bitcoinOwned * currentPrice;
const averagePrice = getAverage(previousPrices);

console.log("Bitcoin owned: " + bitcoinOwned);
console.log("Current Bitcoin price: $" + currentPrice);
console.log("Portfolio value: $" + portfolioValue.toFixed(2));
console.log("Average previous price: $" + averagePrice.toFixed(2));

if (currentPrice > averagePrice) {
    console.log("The current Bitcoin price is above the historical average.");
} else {
    console.log("The current Bitcoin price is at or below the historical average.");
}
```

### CB Pseudocode → JavaScript

| College Board | JavaScript |
|---|---|
| `←` | `const` or `let` |
| `DISPLAY()` | `console.log()` |
| `PROCEDURE` | `function` |
| `RETURN()` | `return` |
| `LENGTH(prices)` | `prices.length` |
| `FOR EACH` | `for...of` |
| `IF / ELSE` | `if / else` |

---

# Theme Check on Python and JavaScript Examples

Both programs follow the same **Bitcoin Portfolio Analyzer** theme.

The Python and JavaScript programs both:

- Store the amount of Bitcoin owned
- Store a current Bitcoin price
- Keep previous Bitcoin prices in a list
- Loop through historical prices
- Calculate an average price
- Calculate the portfolio value
- Compare the current price to the historical average
- Display the results

This keeps the examples connected instead of using unrelated examples for each programming concept.

---

# CPT Concepts

| Concept | Bitcoin Portfolio Analyzer |
|---|---|
| Input/Data | `bitcoinOwned` and `currentPrice` |
| Output | Portfolio value and price comparison |
| List | `previousPrices` |
| Procedure | `GET_AVERAGE` / `get_average` / `getAverage` |
| Parameter | `prices` |
| Return Value | Average Bitcoin price |
| Sequencing | Calculate average → calculate portfolio → compare → display |
| Selection | Current price is compared to average price |
| Iteration | Loop processes every historical Bitcoin price |
| Boolean Expression | `currentPrice > averagePrice` |

---

# Example Result

With:

```text
Bitcoin owned = 0.5
Current price = $70,000
Previous prices = [$62,000, $65,000, $68,000, $70,000]
```

The average previous price is:

```text
$66,250
```

The portfolio value is:

```text
$35,000
```

Therefore, the program reports:

```text
The current Bitcoin price is above the historical average.
```

---

## References

- [Intro to Python](https://pages.opencodingsociety.com/python/intro)
- [Intro to JavaScript](https://pages.opencodingsociety.com/javascript/intro/csp/)
- [Create Performance Task Concepts](https://pages.opencodingsociety.com/csp/cpt-concepts)