 $\mathcal{O}(n)$ or **Linear Time** is perhaps the most intuitive and common Big O complexity you'll encounter. It describes algorithms where the time required grows directly and proportionally with the size of the input.

***

### Real-World $\mathcal{O}(n)$ Example: Checking Every Item in Your Grocery Cart 🛒

Imagine you are a cashier at a grocery store, and you need to **scan every single item** in a customer's shopping cart.

| Characteristic | Mapping to Big O |
| :--- | :--- |
| **Items in the Cart** | Represents the input size, $n$. |
| **Scanning Each Item** | Represents the time complexity, $\mathcal{O}(n)$. |

#### The Process:

1.  **Start:** The customer places their cart, which contains $n$ items, on the conveyor belt.
2.  **Scan First Item:** You pick up the first item, scan its barcode, and place it in a bag. This takes a fixed amount of time (e.g., 2 seconds).
3.  **Scan Second Item:** You pick up the second item, scan it, and bag it. Another 2 seconds.
4.  **Repeat:** You continue this process for every single item in the cart.

#### Why it is Linear

The total time it takes you to process the customer's order is directly proportional to the number of items in their cart.

* If there are **10 items**, it takes you roughly $10 \times 2 = 20$ seconds.
* If there are **20 items**, it takes you roughly $20 \times 2 = 40$ seconds.
* If you **double** the number of items in the cart, you **double** the amount of time it will take to scan them all.

In Big O terms, the relationship is linear. The number of operations (scans) increases exactly at the same rate as the number of items ($n$). This is a straightforward $\mathcal{O}(n)$ operation because you have to perform a constant amount of work for each piece of the input.

In programming, this often translates to a single loop that iterates through every element of a list, array, or similar data structure once.
