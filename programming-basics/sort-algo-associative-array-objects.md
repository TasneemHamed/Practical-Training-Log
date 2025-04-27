# Sort Algo-Associative Array, Objects

**Sorting Algorithms:** Starting with sorting algorithms, you were introduced to two primary types: Bubble Sort and Merge Sort. _**Bubble Sort**_ is like the first step in organizing a messy room. It's simple; you compare two adjacent elements and swap them if they're out of order. It's as if you're sorting books on a shelf one by one, making sure each one is in its correct place before moving on. However, it’s not the fastest way to sort a large collection – it's time-consuming as you might go over the same books multiple times.

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption><p><em><strong>Bubble Sort</strong></em></p></figcaption></figure>





_**Merge Sort**_, on the other hand, is your strategy for bigger challenges. It's like dividing your books into smaller piles, organizing each pile, and then combining them back into one big, sorted pile. This method is systematic and efficient, particularly when you're dealing with a large number of books. It’s the algorithm you'd turn to for speed and efficiency as it consistently performs well, no matter the size of the data.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption><p><em><strong>Merge Sort</strong></em></p></figcaption></figure>

**Associative Arrays: Your Data Organization Tool** Think of associative arrays as your personal filing system. In JavaScript, you often use associative arrays to store data in a way that you can look up using a key, much like checking a dictionary for a definition. These are particularly handy when you need to retrieve information quickly and without hassle, like finding a contact in your phone by their name.

**Objects: Modeling the Real World** When it comes to objects, imagine them as your digital assistants. They hold information and can perform tasks. You were shown how to structure objects and use them to model real-world scenarios in code. Just like a filing cabinet, an object can hold various types of data and functions that work on that data.

**Object Cloning: Keeping the Original Safe** One fascinating topic was object cloning. It's like taking a photocopy of an important document – you work on the copy so that the original remains unchanged. This is a concept you'll find invaluable when you want to avoid unintended side effects in your code.

_One of the important job interview questions:_&#x48;ow to clone an object..

<figure><img src="../.gitbook/assets/Screen Shot 2024-04-26 at 2.52.30 AM.png" alt=""><figcaption><p>How to clone an object</p></figcaption></figure>

In summary, these topics aim to equip you with the tools to organize, manage, and utilize data effectively, helping you create JavaScript code that's not only functional but also elegant and efficient. Understanding these concepts allows you to write code that's robust and adaptable to a variety of data-related challenges you'll encounter.



<figure><img src="../.gitbook/assets/Screen Shot 2024-04-26 at 3.05.42 AM.png" alt=""><figcaption><p>HW</p></figcaption></figure>



```javascript
class Account {
    constructor(owner, balance) {
        this.owner = owner;
        this.balance = balance;
    }
    suspend() {
        console.log(`Account of ${this.owner} is suspended!`);
    }

    deposit(sum) {
        this.balance += sum;
        console.log(`Deposited $${sum} to ${this.owner}'s account.`);
    }

    withdraw(sum) {
        if (this.balance >= sum) {
            this.balance -= sum;
            console.log(`Withdrew $${sum} from ${this.owner}'s account.`);
        } else {
            console.log(`Not enough balance to withdraw $${sum} from ${this.owner}'s account.`);
        }
    }
}

var daveAccount = new Account("israa", 5000.0);
var peterAccount = new Account("jumana", 1825.50);
var nazAccount = new Account("lina", 25.0);

var tasneemAccount = JSON.parse(JSON.stringify(nazAccount));
tasneemAccount.owner = 'Tasneem';

var totalBalance = daveAccount.balance + peterAccount.balance + nazAccount.balance + tasneemAccount.balance;

console.log(`Tasneem's cloned account balance is: $${tasneemAccount.balance}`);
console.log(`The sum of balances for the 4 accounts is: $${totalBalance}`);

```

