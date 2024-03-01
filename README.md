# MidTerm

Program no# 01

class Student {
String name;
String id;
List<String> courses;
Student(this.name, this.id, this.courses);
void addCourse(String course) {
courses.add(course);
print("Added course: $course");
}
void dropCourse(String course) {
if (courses.contains(course)) {
courses.remove(course);
print("Dropped course: $course");
} else {
print("Course not found.");
}
}
void displayCourses() {
print("Courses for ${name} (ID: ${id}):");
for (var course in courses) {
print("- $course");
}
print("");
}
}
void main() {
var student1 = Student("Mubeen", "0320320", ["Math", "Science"]);
var student2 = Student("Moiz", "0320230", ["History", "English"]);
student1.addCourse("Physics");
student1.displayCourses();
student1.dropCourse("Math");
student1.displayCourses();
}

Program no# 02


class BankAccount {
int accountNumber;
double balance;
String accountType;
double interestRate;
BankAccount(this.accountNumber, this.balance, this.accountType, this.interestRate);
void deposit(double amount) {
balance += amount;
print("Deposited \${amount}. New balance: \${balance}");
}
void withdraw(double amount) {
if (amount <= balance) {
balance -= amount;
print("Withdrew \${amount}. New balance: \${balance}");
} else {
print("Insufficient funds!");
}
}
void addInterest() {
double interest = balance * (interestRate / 100);
balance += interest;
print("Added interest. New balance: \${balance}");
}
void display() {
print("Account Number: $accountNumber");
print("Balance: \${balance}");
print("Account Type: $accountType");
print("Interest Rate: $interestRate%");
print("");
}
}
void main() {
BankAccount account1 = BankAccount(123456, 1000.0, "Savings", 5.0);
BankAccount account2 = BankAccount(987654, 5000.0, "Checking", 3.0);
account1.deposit(500);
account1.withdraw(200);
account1.addInterest();
account1.display();
account2.deposit(1000);
account2.withdraw(6000);
account2.addInterest();
account2.display();
}
