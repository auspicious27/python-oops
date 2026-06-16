# Module 12: Object-Oriented Programming - Complete Separate Notes

Language style: Simple English with Hinglish explanation.

Document format:

1. Theory Explanation
2. Example Code
3. Output
4. Line-by-Line Explanation
5. Mini Project with detailed explanation

---

# Module 12: Object-Oriented Programming

## Topics Covered

- Classes & Objects
- Constructors
- Inheritance
- Encapsulation
- Mini Project
- Project 6: Bank Account System

---

## Learning Outcomes

Is module ke end tak learner ye confidently explain kar paayega:

| Skill | Learner Kya Samjhega |
|---|---|
| Class | Class ko blueprint/design ke form mein samjhega |
| Object | Object ko class se bana actual item samjhega |
| Attribute | Object ke data ko attribute bolte hain |
| Method | Object ke action/function ko method bolte hain |
| Constructor | Object create hote hi data initialize kaise hota hai |
| Inheritance | Child class parent class ke features kaise use karti hai |
| Encapsulation | Sensitive data ko direct access se kaise protect karte hain |
| Project | Bank account system mein OOP concepts kaise combine hote hain |

---

## OOP Ko Samajhne Ka Simple Formula

```text
Class = Design / Blueprint
Object = Actual thing made from that blueprint
Attribute = Object ka data
Method = Object ka kaam
```

Real-world comparison:

| Example | Class | Object | Attribute | Method |
|---|---|---|---|---|
| Student system | `Student` | Aman ka student record | name, course | show details |
| Bank system | `BankAccount` | Aman ka bank account | holder, balance | deposit, withdraw |
| Shopping app | `Product` | Laptop product | name, price | show product |
| Employee app | `Employee` | Sara employee record | name, salary | show salary |

Teaching tip:

Jab learner confused ho, unhe bolo:

```text
Class ek form ka blank format hai.
Object us form ka filled copy hai.
self ka matlab hai "yeh wala current object".
```

---

## Basic OOP Syntax Breakdown

```python
class ClassName:
    def __init__(self, value):
        self.attribute = value

    def method_name(self):
        print(self.attribute)

object_name = ClassName("data")
object_name.method_name()
```

| Syntax Part | Meaning |
|---|---|
| `class ClassName:` | New class/blueprint create karta hai |
| `def __init__(...)` | Constructor method, object create hote hi run hota hai |
| `self` | Current object ko represent karta hai |
| `self.attribute` | Object ke andar saved data |
| `def method_name(self):` | Class ke andar action/function |
| `object_name = ClassName("data")` | Class se object create karna |
| `object_name.method_name()` | Object ke method ko call karna |

Important indentation rule:

```text
Class ke andar method 4 spaces indent hota hai.
Method ke andar code 8 spaces indent hota hai.
```

---

## Integrated Learning Path - OOP Concepts Ko Ek Saath Kaise Samjhein

OOP ko alag-alag topics ki tarah ratna difficult lag sakta hai. Isliye ise ek story ke through samjho.

Story:

Hum ek coaching institute ka software bana rahe hain. Hume students, teachers, accounts aur payments manage karne hain. Agar hum normal variables aur functions se sab kuch likhenge, code messy ho sakta hai. OOP help karta hai real-world cheezon ko code mein clean structure dene mein.

Learning path:

| Step | Concept | Kyu Zaroori Hai |
|---|---|---|
| 1 | Class | Blueprint banane ke liye |
| 2 | Object | Actual data/entity banane ke liye |
| 3 | Constructor | Object create hote hi initial data set karne ke liye |
| 4 | Methods | Object ke actions define karne ke liye |
| 5 | Encapsulation | Sensitive data protect karne ke liye |
| 6 | Inheritance | Common code reuse karne ke liye |
| 7 | Project | Sab concepts ko real app mein combine karne ke liye |

Simple integrated example:

```python
class Student:
    def __init__(self, name, course):
        self.name = name
        self.course = course

    def show_details(self):
        print(f"{self.name} is learning {self.course}")

student1 = Student("Aman", "Python")
student1.show_details()
```

Is small code mein:

| OOP Concept | Code mein Kahan Hai |
|---|---|
| Class | `class Student:` |
| Object | `student1` |
| Constructor | `__init__` |
| Attribute | `self.name`, `self.course` |
| Method | `show_details` |
| `self` | Current object ko refer karta hai |

Line-by-line explanation:

| Line | Code | Explanation |
|---|---|---|
| 1 | `class Student:` | Student ka blueprint create hota hai. Har student object isi design se banega. |
| 2 | `def __init__(self, name, course):` | Constructor define hota hai. Jab object create hoga, name aur course set honge. |
| 3 | `self.name = name` | Current object ke andar name save hota hai. |
| 4 | `self.course = course` | Current object ke andar course save hota hai. |
| 6 | `def show_details(self):` | Student details show karne ka method define hota hai. |
| 7 | `print(f"{self.name} is learning {self.course}")` | Saved attributes use karke readable message print hota hai. |
| 9 | `student1 = Student("Aman", "Python")` | Student object create hota hai. Constructor automatically run hota hai. |
| 10 | `student1.show_details()` | Object ka method call hota hai. |

Output:

```text
Aman is learning Python
```

Teaching line:

```text
Class se object banta hai, constructor object ka data set karta hai, method object ka kaam perform karta hai.
```

---

## 1. Object-Oriented Programming Kya Hai?

### Theory Explanation

Object-Oriented Programming, short form OOP, ek programming style hai jisme hum real-world things ko `class` aur `object` ke form mein represent karte hain.

Simple English:

OOP is a way of writing code by grouping data and related actions together.

Hinglish:

OOP mein hum data aur us data par hone wale actions ko ek saath organize karte hain. Jaise student ke paas name, roll number, course hota hai, aur student details show karne ka action bhi hota hai. Yeh sab ek class ke andar rakha ja sakta hai.

Real-world story:

Socho ek school admission form ka blank format hai. Us blank form mein fields hoti hain: name, age, course. Yeh blank format class jaisa hai. Jab Aman ka form fill hota hai, woh ek object ban jaata hai. Jab Sara ka form fill hota hai, woh doosra object ban jaata hai.

| Real World | OOP Meaning |
|---|---|
| Blank admission form | Class |
| Aman ka filled form | Object |
| Name, age, course | Attributes |
| Details display karna | Method |

Why OOP useful hai:

- Code organized hota hai.
- Real-world problems ko easily model kar sakte hain.
- Same blueprint se multiple objects bana sakte hain.
- Large projects manage karna easy hota hai.
- Data aur related functions ek jagah rehte hain.

---

## 2. Classes & Objects

### Theory Explanation

Class ek blueprint hoti hai. Object us blueprint se bana actual item hota hai.

Example:

`Student` class ek blueprint hai. `student1` object ek actual student hai.

Class ke andar do main cheezein hoti hain:

| Part | Meaning |
|---|---|
| Attributes | Object ka data, jaise name, course |
| Methods | Object ke actions, jaise show details |

Syntax:

```python
class ClassName:
    def method_name(self):
        code
```

Important:

`self` current object ko refer karta hai. Matlab jis object se method call ho raha hai, `self` usi object ko represent karega.

### Example Code

```python
class Student:
    def show_message(self):
        print("I am a student.")

student1 = Student()
student1.show_message()
```

### Output

```text
I am a student.
```

### Line-by-Line Explanation

| Line | Code | Detailed Explanation |
|---|---|---|
| 1 | `class Student:` | `Student` naam ki class create hoti hai. Class ek blueprint hoti hai. Colon `:` ke baad class ka block start hota hai. |
| 2 | `def show_message(self):` | Class ke andar method define hota hai. Method class ke andar function jaisa hota hai. `self` current object ko represent karta hai. |
| 3 | `print("I am a student.")` | Jab method call hoga, yeh message screen par print hoga. Yeh line method ke andar hai kyunki indentation hai. |
| 5 | `student1 = Student()` | `Student` class ka object create hota hai. Is object ka naam `student1` hai. |
| 6 | `student1.show_message()` | `student1` object ka `show_message()` method call hota hai. Isse line 3 execute hoti hai. |

### Technical Flow

```text
Python class read karta hai -> object create hota hai -> method call hota hai -> print line execute hoti hai
```

Step-by-step:

| Step | What Happens |
|---|---|
| 1 | Python `Student` class ko memory mein store karta hai |
| 2 | `student1 = Student()` se object create hota hai |
| 3 | `student1.show_message()` method call karta hai |
| 4 | Python automatically `student1` ko `self` ke form mein method ko deta hai |
| 5 | Method ke andar `print()` execute hota hai |

### Common Mistakes

| Mistake | Why Wrong |
|---|---|
| `class student:` | Class name usually capital letter se start karna best practice hai |
| `def show_message():` | Method ke andar `self` missing hai |
| `student1.show_message` | Parentheses missing, method call nahi hoga |

### Extra Example - Product Class

### Theory Explanation

E-commerce app mein product ka name aur price store karna hota hai. Har product ke liye same structure hota hai, isliye class useful hai.

### Example Code

```python
class Product:
    def show_product(self):
        print("Product: Laptop")
        print("Price: 55000")

product1 = Product()
product1.show_product()
```

### Output

```text
Product: Laptop
Price: 55000
```

### Line-by-Line Explanation

| Line | Code | Detailed Explanation |
|---|---|---|
| 1 | `class Product:` | Product class create hoti hai. Yeh product ka blueprint hai. |
| 2 | `def show_product(self):` | Product details show karne ke liye method define hota hai. |
| 3 | `print("Product: Laptop")` | Product name print hota hai. |
| 4 | `print("Price: 55000")` | Product price print hota hai. |
| 6 | `product1 = Product()` | Product class ka object create hota hai. |
| 7 | `product1.show_product()` | Object ka method call hota hai aur details print hoti hain. |

---

## 3. Constructors

### Theory Explanation

Constructor ek special method hota hai jo object create hote hi automatically run hota hai. Python mein constructor ka naam `__init__` hota hai.

Constructor ka use initial data set karne ke liye hota hai.

Example:

Jab student object create ho, tabhi uska name aur course set ho jaaye.

Syntax:

```python
def __init__(self, parameter1, parameter2):
    self.parameter1 = parameter1
    self.parameter2 = parameter2
```

Important terms:

| Term | Meaning |
|---|---|
| `__init__` | Constructor method |
| `self` | Current object |
| Parameter | Object create karte time di gayi value receive karta hai |
| Attribute | Object ke andar saved data |

### Example Code

```python
class Student:
    def __init__(self, name, course):
        self.name = name
        self.course = course

    def show_details(self):
        print(f"Name: {self.name}")
        print(f"Course: {self.course}")

student1 = Student("Aman", "Python")
student1.show_details()
```

### Output

```text
Name: Aman
Course: Python
```

### Line-by-Line Explanation

| Line | Code | Detailed Explanation |
|---|---|---|
| 1 | `class Student:` | Student class define hoti hai. Yeh student object banane ka blueprint hai. |
| 2 | `def __init__(self, name, course):` | Constructor define hota hai. Object create hote hi automatically run hota hai. `name` aur `course` values receive karta hai. |
| 3 | `self.name = name` | Received `name` value current object ke andar save hoti hai. Ab object ke paas apna name attribute hai. |
| 4 | `self.course = course` | Received `course` value current object ke andar save hoti hai. |
| 6 | `def show_details(self):` | Student details display karne ke liye method define hota hai. |
| 7 | `print(f"Name: {self.name}")` | Current object ka saved name print hota hai. |
| 8 | `print(f"Course: {self.course}")` | Current object ka saved course print hota hai. |
| 10 | `student1 = Student("Aman", "Python")` | Object create hota hai. `"Aman"` name parameter mein jaata hai, `"Python"` course parameter mein jaata hai. |
| 11 | `student1.show_details()` | Object ka method call hota hai aur saved details print hoti hain. |

### Constructor Technical Flow

```text
Student("Aman", "Python") call hota hai
-> Python object create karta hai
-> __init__ automatically run hota hai
-> self.name and self.course set hote hain
-> object student1 variable mein store hota hai
```

Dry run:

| Expression | Value |
|---|---|
| `name` | `"Aman"` |
| `course` | `"Python"` |
| `self.name` | `"Aman"` |
| `self.course` | `"Python"` |

### Common Mistakes

| Mistake | Problem |
|---|---|
| `def init(self):` | Wrong constructor name. Correct is `__init__` |
| `self.name = "Aman"` hard-code karna | Har object ka name same ho jayega |
| `Student()` without arguments | Constructor ko `name` aur `course` chahiye, error aayega |

### Extra Example - Employee Constructor

### Theory Explanation

Company mein employee ka name aur salary object create karte time set kar sakte hain. Constructor is kaam ke liye best hai.

### Example Code

```python
class Employee:
    def __init__(self, name, salary):
        self.name = name
        self.salary = salary

    def show_salary(self):
        print(f"{self.name} salary is {self.salary}")

employee1 = Employee("Sara", 30000)
employee1.show_salary()
```

### Output

```text
Sara salary is 30000
```

### Line-by-Line Explanation

| Line | Code | Detailed Explanation |
|---|---|---|
| 1 | `class Employee:` | Employee blueprint create hota hai. |
| 2 | `def __init__(self, name, salary):` | Constructor employee ka name aur salary receive karta hai. |
| 3 | `self.name = name` | Employee name object mein save hota hai. |
| 4 | `self.salary = salary` | Employee salary object mein save hoti hai. |
| 6 | `def show_salary(self):` | Salary display karne ka method. |
| 7 | `print(f"{self.name} salary is {self.salary}")` | Employee ka name aur salary print hoti hai. |
| 9 | `employee1 = Employee("Sara", 30000)` | Employee object create hota hai aur constructor run hota hai. |
| 10 | `employee1.show_salary()` | Salary show method call hota hai. |

---

## 4. Inheritance

### Theory Explanation

Inheritance ka matlab hai ek class doosri class ke features use kar sakti hai.

Parent class common properties/methods rakhti hai. Child class parent ke features inherit karti hai aur apne extra features add kar sakti hai.

Real-world example:

Person ek parent concept hai. Student bhi person hai. Teacher bhi person hai. Dono mein name common ho sakta hai, lekin student ke paas course hoga aur teacher ke paas subject hoga.

| OOP Term | Meaning |
|---|---|
| Parent class | Jis class se features inherit hote hain |
| Child class | Jo class features inherit karti hai |
| Inheritance | Parent ke features child mein use hona |

### Example Code

```python
class Person:
    def show_person(self):
        print("I am a person.")

class Student(Person):
    def show_student(self):
        print("I am a student.")

s1 = Student()
s1.show_person()
s1.show_student()
```

### Output

```text
I am a person.
I am a student.
```

### Line-by-Line Explanation

| Line | Code | Detailed Explanation |
|---|---|---|
| 1 | `class Person:` | Parent class create hoti hai. Isme common behavior rakha gaya hai. |
| 2 | `def show_person(self):` | Parent class ka method define hota hai. |
| 3 | `print("I am a person.")` | Parent method ka message print hota hai. |
| 5 | `class Student(Person):` | Student child class hai. Parentheses mein `Person` likhne ka matlab Student class Person se inherit kar rahi hai. |
| 6 | `def show_student(self):` | Student class ka apna method define hota hai. |
| 7 | `print("I am a student.")` | Student method ka message print hota hai. |
| 9 | `s1 = Student()` | Student class ka object create hota hai. |
| 10 | `s1.show_person()` | Parent class ka method child object se call ho raha hai. |
| 11 | `s1.show_student()` | Child class ka own method call ho raha hai. |

### Extra Example - Teacher Inheritance

### Theory Explanation

Teacher bhi ek person hai. Teacher class Person class se name functionality inherit kar sakti hai.

### Example Code

```python
class Person:
    def __init__(self, name):
        self.name = name

    def show_name(self):
        print("Name:", self.name)

class Teacher(Person):
    def __init__(self, name, subject):
        super().__init__(name)
        self.subject = subject

    def show_subject(self):
        print("Subject:", self.subject)

teacher1 = Teacher("Mr. Khan", "Python")
teacher1.show_name()
teacher1.show_subject()
```

### Output

```text
Name: Mr. Khan
Subject: Python
```

### Line-by-Line Explanation

| Line | Code | Detailed Explanation |
|---|---|---|
| 1 | `class Person:` | Parent class define hoti hai. |
| 2 | `def __init__(self, name):` | Parent constructor name receive karta hai. |
| 3 | `self.name = name` | Name parent object structure mein save hota hai. |
| 5 | `def show_name(self):` | Name show karne ka parent method. |
| 6 | `print("Name:", self.name)` | Saved name print hota hai. |
| 8 | `class Teacher(Person):` | Teacher class Person se inherit kar rahi hai. |
| 9 | `def __init__(self, name, subject):` | Teacher constructor name aur subject receive karta hai. |
| 10 | `super().__init__(name)` | Parent class ka constructor call hota hai taaki name set ho sake. |
| 11 | `self.subject = subject` | Teacher-specific subject save hota hai. |
| 13 | `def show_subject(self):` | Subject show karne ka method. |
| 14 | `print("Subject:", self.subject)` | Subject print hota hai. |
| 16 | `teacher1 = Teacher("Mr. Khan", "Python")` | Teacher object create hota hai. |
| 17 | `teacher1.show_name()` | Parent method call hota hai. |
| 18 | `teacher1.show_subject()` | Child method call hota hai. |

### Inheritance Technical Flow

```text
Teacher object create hota hai
-> Teacher constructor run hota hai
-> super().__init__(name) parent constructor ko call karta hai
-> parent name set karta hai
-> child subject set karta hai
```

Why `super()` useful hai:

`super()` parent class ke methods/constructor ko call karne ke liye use hota hai. Isse parent ka code repeat nahi karna padta.

### Common Mistakes

| Mistake | Problem |
|---|---|
| `class Teacher:` | Parent class inherit nahi hui |
| `super().__init__()` without name | Parent constructor ko required value nahi milegi |
| Parent aur child mein same logic copy karna | Code duplication hota hai |

---

## 5. Encapsulation

### Theory Explanation

Encapsulation ka matlab hai data ko class ke andar protect karna aur controlled access dena.

Simple English:

Encapsulation means hiding internal data and allowing access through methods.

Hinglish:

Encapsulation mein hum sensitive data ko direct access se bachate hain. Jaise bank balance ko direct change karna allowed nahi hona chahiye. Balance deposit aur withdraw methods ke through hi change hona chahiye.

Python mein double underscore `__` use karke variable ko private-like banaya ja sakta hai.

Example:

```python
self.__balance = balance
```

Iska matlab balance ko direct access karna avoid karna chahiye.

### Example Code

```python
class Account:
    def __init__(self, balance):
        self.__balance = balance

    def show_balance(self):
        print("Balance:", self.__balance)

account1 = Account(5000)
account1.show_balance()
```

### Output

```text
Balance: 5000
```

### Line-by-Line Explanation

| Line | Code | Detailed Explanation |
|---|---|---|
| 1 | `class Account:` | Account class create hoti hai. |
| 2 | `def __init__(self, balance):` | Constructor initial balance receive karta hai. |
| 3 | `self.__balance = balance` | Balance private-like attribute mein save hota hai. Double underscore direct access ko discourage karta hai. |
| 5 | `def show_balance(self):` | Balance show karne ke liye method define hota hai. |
| 6 | `print("Balance:", self.__balance)` | Class ke andar private-like balance access karke print hota hai. |
| 8 | `account1 = Account(5000)` | Account object create hota hai with initial balance 5000. |
| 9 | `account1.show_balance()` | Controlled method ke through balance show hota hai. |

### Extra Example - Controlled Update

### Theory Explanation

Encapsulation ka benefit yeh hai ki hum invalid data ko stop kar sakte hain. Example: balance negative amount se update nahi hona chahiye.

### Example Code

```python
class Wallet:
    def __init__(self):
        self.__money = 0

    def add_money(self, amount):
        if amount > 0:
            self.__money += amount
            print("Money added.")
        else:
            print("Invalid amount.")

    def show_money(self):
        print("Money:", self.__money)

wallet1 = Wallet()
wallet1.add_money(100)
wallet1.show_money()
```

### Output

```text
Money added.
Money: 100
```

### Line-by-Line Explanation

| Line | Code | Detailed Explanation |
|---|---|---|
| 1 | `class Wallet:` | Wallet class create hoti hai. |
| 2 | `def __init__(self):` | Constructor no input leta hai aur default money set karta hai. |
| 3 | `self.__money = 0` | Money private-like attribute mein 0 se initialize hoti hai. |
| 5 | `def add_money(self, amount):` | Money add karne ka controlled method. |
| 6 | `if amount > 0:` | Sirf positive amount allow hai. |
| 7 | `self.__money += amount` | Valid amount private money mein add hota hai. |
| 8 | `print("Money added.")` | Success message print hota hai. |
| 9 | `else:` | Agar amount invalid hai toh else chalega. |
| 10 | `print("Invalid amount.")` | Invalid amount message print hota hai. |
| 12 | `def show_money(self):` | Money display karne ka method. |
| 13 | `print("Money:", self.__money)` | Current money print hoti hai. |
| 15 | `wallet1 = Wallet()` | Wallet object create hota hai. |
| 16 | `wallet1.add_money(100)` | 100 add karne ka method call hota hai. |
| 17 | `wallet1.show_money()` | Final money show hoti hai. |

### Encapsulation Technical Flow

```text
Private-like data class ke andar store hota hai
-> Outside code direct data change nahi karta
-> Method validation karta hai
-> Valid data hone par value update hoti hai
```

Why direct balance change risky hai:

```python
account.balance = -5000
```

Agar balance public ho aur koi directly negative value set kar de, toh system wrong ho jayega. Isliye sensitive data ko method ke through update karna better hai.

### Common Mistakes

| Mistake | Problem |
|---|---|
| Balance public rakhna | Koi bhi direct change kar sakta hai |
| Validation na lagana | Negative amount bhi add ho sakta hai |
| Private data access karne ki koshish | Encapsulation ka purpose break hota hai |

---

## 6. Mini Project - Project 6: Bank Account System

### Project Theory Explanation

Bank Account System OOP ka practical project hai. Is project mein bank account ko class ke form mein design karte hain. Har account object ke paas account holder ka naam aur balance hota hai.

Project features:

- Account creation
- Deposit amount
- Withdraw amount
- Check balance
- Balance ko encapsulation ke through protect karna

Real-world explanation:

Bank mein user directly balance variable change nahi kar sakta. User deposit karega ya withdraw karega. System rules check karega, phir balance update hoga. Isi idea ko Python class mein implement karte hain.

### Project Code

```python
class BankAccount:
    def __init__(self, account_holder, balance):
        self.account_holder = account_holder
        self.__balance = balance

    def deposit(self, amount):
        if amount <= 0:
            print("Deposit amount must be positive.")
            return

        self.__balance += amount
        print("Amount deposited successfully.")

    def withdraw(self, amount):
        if amount <= 0:
            print("Withdrawal amount must be positive.")
            return

        if amount <= self.__balance:
            self.__balance -= amount
            print("Withdrawal successful.")
        else:
            print("Insufficient balance.")

    def check_balance(self):
        print(f"{self.account_holder}, your balance is {self.__balance}")

account = BankAccount("Aman", 5000)
account.deposit(2000)
account.withdraw(1000)
account.check_balance()
```

### Output

```text
Amount deposited successfully.
Withdrawal successful.
Aman, your balance is 6000
```

### How to Save and Run

Save file as:

```text
bank_account_system.py
```

Run command:

```bash
python bank_account_system.py
```

Windows alternative:

```bash
py bank_account_system.py
```

### Full Line-by-Line Explanation

| Line | Code | Detailed Explanation |
|---|---|---|
| 1 | `class BankAccount:` | Bank account ka blueprint create hota hai. Is class se account objects banenge. |
| 2 | `def __init__(self, account_holder, balance):` | Constructor define hota hai. Account object create hote hi holder name aur opening balance set karega. |
| 3 | `self.account_holder = account_holder` | Account holder ka naam object ke andar save hota hai. |
| 4 | `self.__balance = balance` | Balance private-like attribute mein save hota hai. Direct outside access avoid hota hai. |
| 6 | `def deposit(self, amount):` | Deposit method define hota hai. Yeh amount receive karega. |
| 7 | `if amount <= 0:` | Check hota hai ki deposit amount zero ya negative toh nahi. |
| 8 | `print("Deposit amount must be positive.")` | Invalid deposit ke liye message print hota hai. |
| 9 | `return` | Function yahin stop ho jaata hai, balance update nahi hota. |
| 11 | `self.__balance += amount` | Valid amount current balance mein add hota hai. |
| 12 | `print("Amount deposited successfully.")` | Deposit success message print hota hai. |
| 14 | `def withdraw(self, amount):` | Withdraw method define hota hai. |
| 15 | `if amount <= 0:` | Withdrawal amount positive hona chahiye. |
| 16 | `print("Withdrawal amount must be positive.")` | Invalid withdrawal amount message. |
| 17 | `return` | Invalid amount hone par method stop hota hai. |
| 19 | `if amount <= self.__balance:` | Check hota hai account mein enough balance hai ya nahi. |
| 20 | `self.__balance -= amount` | Valid withdrawal hone par amount balance se minus hota hai. |
| 21 | `print("Withdrawal successful.")` | Withdrawal success message. |
| 22 | `else:` | Agar amount balance se zyada hai toh else chalega. |
| 23 | `print("Insufficient balance.")` | Balance kam hone par message print hota hai. |
| 25 | `def check_balance(self):` | Balance check karne ka method define hota hai. |
| 26 | `print(f"{self.account_holder}, your balance is {self.__balance}")` | Account holder ka naam aur current balance print hota hai. |
| 28 | `account = BankAccount("Aman", 5000)` | BankAccount class ka object create hota hai. Holder Aman hai aur opening balance 5000 hai. |
| 29 | `account.deposit(2000)` | Account mein 2000 deposit hota hai. Balance 5000 se 7000 ho jaata hai. |
| 30 | `account.withdraw(1000)` | Account se 1000 withdraw hota hai. Balance 7000 se 6000 ho jaata hai. |
| 31 | `account.check_balance()` | Final balance print hota hai. |

### Project Flow

```text
Create account -> Deposit amount -> Withdraw amount -> Check final balance
```

### Project Dry Run

Starting line:

```python
account = BankAccount("Aman", 5000)
```

| Step | Action | Balance |
|---|---|---|
| 1 | Account create hota hai | 5000 |
| 2 | `deposit(2000)` call hota hai | 7000 |
| 3 | `withdraw(1000)` call hota hai | 6000 |
| 4 | `check_balance()` call hota hai | 6000 print hota hai |

### Method-Wise Explanation

#### `__init__` Method

```python
def __init__(self, account_holder, balance):
    self.account_holder = account_holder
    self.__balance = balance
```

| Line | Explanation |
|---|---|
| `def __init__(self, account_holder, balance):` | Account create hote hi holder name aur balance receive karta hai |
| `self.account_holder = account_holder` | Holder name object ke andar store hota hai |
| `self.__balance = balance` | Balance private-like form mein store hota hai |

#### `deposit` Method

```python
def deposit(self, amount):
    if amount <= 0:
        print("Deposit amount must be positive.")
        return

    self.__balance += amount
    print("Amount deposited successfully.")
```

| Line | Explanation |
|---|---|
| `def deposit(self, amount):` | Deposit action ka method hai |
| `if amount <= 0:` | Invalid amount check karta hai |
| `print(...)` | Invalid input par message show karta hai |
| `return` | Method yahin stop hota hai |
| `self.__balance += amount` | Valid amount balance mein add hota hai |
| `print(...)` | Success message show hota hai |

#### `withdraw` Method

```python
def withdraw(self, amount):
    if amount <= 0:
        print("Withdrawal amount must be positive.")
        return

    if amount <= self.__balance:
        self.__balance -= amount
        print("Withdrawal successful.")
    else:
        print("Insufficient balance.")
```

| Line | Explanation |
|---|---|
| `def withdraw(self, amount):` | Withdrawal action ka method hai |
| `if amount <= 0:` | Zero/negative amount reject karta hai |
| `return` | Invalid case mein method stop hota hai |
| `if amount <= self.__balance:` | Check karta hai account mein enough balance hai ya nahi |
| `self.__balance -= amount` | Amount balance se minus hota hai |
| `else:` | Agar balance enough nahi hai toh else run hota hai |
| `print("Insufficient balance.")` | User ko balance kam hone ka message milta hai |

#### `check_balance` Method

```python
def check_balance(self):
    print(f"{self.account_holder}, your balance is {self.__balance}")
```

| Line | Explanation |
|---|---|
| `def check_balance(self):` | Balance check karne ka method hai |
| `print(f"...")` | Holder name aur current balance formatted message mein print hota hai |

### Test Cases

| Test | Code | Expected Result |
|---|---|---|
| Valid deposit | `account.deposit(2000)` | Balance increase hoga |
| Invalid deposit | `account.deposit(-100)` | Error message |
| Valid withdrawal | `account.withdraw(1000)` | Balance decrease hoga |
| More than balance | `account.withdraw(99999)` | Insufficient balance |
| Balance check | `account.check_balance()` | Current balance print |

### Concepts Used in Project

| Concept | Where Used |
|---|---|
| Class | `BankAccount` |
| Object | `account` |
| Constructor | `__init__` |
| Attribute | `account_holder`, `__balance` |
| Method | `deposit`, `withdraw`, `check_balance` |
| Encapsulation | `__balance` |
| Condition | Deposit and withdrawal validation |

---

## OOP Concepts Integrated in One Flow

Ab dekho kaise saare OOP concepts ek project mein naturally connect hote hain.

### Step 1 - Class and Object

Theory:

Pehle hum bank account ka blueprint banate hain. Abhi isme sirf account holder ka naam show karenge.

Code:

```python
class BankAccount:
    def show_account(self):
        print("This is a bank account.")

account1 = BankAccount()
account1.show_account()
```

Output:

```text
This is a bank account.
```

Line-by-line explanation:

| Line | Code | Explanation |
|---|---|---|
| 1 | `class BankAccount:` | Bank account ka blueprint create hota hai. |
| 2 | `def show_account(self):` | Account information show karne ka method define hota hai. |
| 3 | `print("This is a bank account.")` | Method call hone par message print hota hai. |
| 5 | `account1 = BankAccount()` | BankAccount class ka object create hota hai. |
| 6 | `account1.show_account()` | Object ka method call hota hai. |

### Step 2 - Constructor Add Karna

Theory:

Ab account create hote hi account holder ka naam aur opening balance set karenge. Iske liye constructor use hota hai.

Code:

```python
class BankAccount:
    def __init__(self, account_holder, balance):
        self.account_holder = account_holder
        self.balance = balance

    def show_account(self):
        print(f"{self.account_holder} has balance {self.balance}")

account1 = BankAccount("Aman", 5000)
account1.show_account()
```

Output:

```text
Aman has balance 5000
```

Line-by-line explanation:

| Line | Code | Explanation |
|---|---|---|
| 1 | `class BankAccount:` | Bank account blueprint define hota hai. |
| 2 | `def __init__(self, account_holder, balance):` | Constructor account holder aur balance receive karta hai. |
| 3 | `self.account_holder = account_holder` | Holder name object mein save hota hai. |
| 4 | `self.balance = balance` | Balance object mein save hota hai. |
| 6 | `def show_account(self):` | Account details show karne ka method. |
| 7 | `print(f"{self.account_holder} has balance {self.balance}")` | Object ke attributes print hote hain. |
| 9 | `account1 = BankAccount("Aman", 5000)` | Object create hota hai aur constructor run hota hai. |
| 10 | `account1.show_account()` | Account details print hoti hain. |

### Step 3 - Methods Add Karna

Theory:

Account ke actions deposit aur withdraw hote hain. Yeh actions methods ke form mein class ke andar likhenge.

Code:

```python
class BankAccount:
    def __init__(self, balance):
        self.balance = balance

    def deposit(self, amount):
        self.balance += amount

    def show_balance(self):
        print("Balance:", self.balance)

account1 = BankAccount(5000)
account1.deposit(2000)
account1.show_balance()
```

Output:

```text
Balance: 7000
```

Line-by-line explanation:

| Line | Code | Explanation |
|---|---|---|
| 1 | `class BankAccount:` | Bank account class create hoti hai. |
| 2 | `def __init__(self, balance):` | Constructor initial balance receive karta hai. |
| 3 | `self.balance = balance` | Balance object mein save hota hai. |
| 5 | `def deposit(self, amount):` | Deposit method amount receive karta hai. |
| 6 | `self.balance += amount` | Amount balance mein add hota hai. |
| 8 | `def show_balance(self):` | Balance display method define hota hai. |
| 9 | `print("Balance:", self.balance)` | Current balance print hota hai. |
| 11 | `account1 = BankAccount(5000)` | Object initial balance 5000 ke saath create hota hai. |
| 12 | `account1.deposit(2000)` | 2000 deposit hota hai. |
| 13 | `account1.show_balance()` | Updated balance print hota hai. |

### Step 4 - Encapsulation Add Karna

Theory:

Balance sensitive data hai. Isko direct access se protect karna chahiye. Isliye `__balance` use karenge.

Code:

```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount

    def show_balance(self):
        print("Balance:", self.__balance)

account1 = BankAccount(5000)
account1.deposit(2000)
account1.show_balance()
```

Output:

```text
Balance: 7000
```

Line-by-line explanation:

| Line | Code | Explanation |
|---|---|---|
| 1 | `class BankAccount:` | Bank account class create hoti hai. |
| 2 | `def __init__(self, balance):` | Constructor balance receive karta hai. |
| 3 | `self.__balance = balance` | Balance private-like attribute mein save hota hai. |
| 5 | `def deposit(self, amount):` | Deposit method amount receive karta hai. |
| 6 | `if amount > 0:` | Sirf positive amount allow hai. |
| 7 | `self.__balance += amount` | Valid amount balance mein add hota hai. |
| 9 | `def show_balance(self):` | Balance show karne ka method. |
| 10 | `print("Balance:", self.__balance)` | Private-like balance class ke andar access hota hai. |
| 12 | `account1 = BankAccount(5000)` | Account object create hota hai. |
| 13 | `account1.deposit(2000)` | Deposit method call hota hai. |
| 14 | `account1.show_balance()` | Updated balance print hota hai. |

### Step 5 - Inheritance Add Karna

Theory:

Agar hum SavingsAccount aur CurrentAccount banana chahein, dono BankAccount se common features inherit kar sakte hain.

Code:

```python
class BankAccount:
    def __init__(self, account_holder):
        self.account_holder = account_holder

    def show_holder(self):
        print("Account holder:", self.account_holder)

class SavingsAccount(BankAccount):
    def show_account_type(self):
        print("Account type: Savings")

account1 = SavingsAccount("Aman")
account1.show_holder()
account1.show_account_type()
```

Output:

```text
Account holder: Aman
Account type: Savings
```

Line-by-line explanation:

| Line | Code | Explanation |
|---|---|---|
| 1 | `class BankAccount:` | Parent class create hoti hai. |
| 2 | `def __init__(self, account_holder):` | Parent constructor holder name receive karta hai. |
| 3 | `self.account_holder = account_holder` | Holder name object mein save hota hai. |
| 5 | `def show_holder(self):` | Holder name show karne ka method. |
| 6 | `print("Account holder:", self.account_holder)` | Holder name print hota hai. |
| 8 | `class SavingsAccount(BankAccount):` | SavingsAccount child class hai jo BankAccount se inherit kar rahi hai. |
| 9 | `def show_account_type(self):` | Child class ka own method. |
| 10 | `print("Account type: Savings")` | Account type print hota hai. |
| 12 | `account1 = SavingsAccount("Aman")` | Child class ka object create hota hai. Parent constructor run hota hai. |
| 13 | `account1.show_holder()` | Parent method child object se call hota hai. |
| 14 | `account1.show_account_type()` | Child method call hota hai. |

Final teaching point:

```text
Class design deta hai.
Object actual account banata hai.
Constructor account ka starting data set karta hai.
Methods account ke actions perform karte hain.
Encapsulation balance ko protect karta hai.
Inheritance common account features reuse karta hai.
```

---

## Final Summary

| Topic | Key Point |
|---|---|
| Classes & Objects | Class blueprint hai, object actual item hai |
| Constructors | Object create hote hi initial data set karte hain |
| Inheritance | Child class parent class ke features use karti hai |
| Encapsulation | Data ko protected and controlled access deta hai |
| Bank Account Project | OOP concepts ko real-world banking logic mein use karta hai |

Happy Coding.
