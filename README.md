Download Link: https://assignmentchef.com/product/solved-jac444-workshop-3
<br>
<strong>Description:</strong>

The following workshop lets you practice basic java coding techniques, creating classes, methods, using arrays, inheritance, polymorphism, Exceptional Handling.




Employee and Payable Case Study:







<h2>The Payable Interface</h2>

An <em>interface</em> declares one or more methods but does not implement the methods. For example, the <strong>Payable interface</strong> should declare the <em>getPaymentAmount</em> method.

<h2>The Invoice and Employee Classes</h2>

Both the <strong>Employee</strong> <strong>class</strong> and <strong>Invoice class</strong> implements Payable interface, which is a promise to implement the <em>getPaymentAmount</em> method. This allows <strong>Employee</strong> objects and <strong>Invoice</strong> objects to be processed polymorphically as Payable objects because they all implement the <em>getPaymentAmount</em> method.

<strong>The Invoice class</strong> is a basic class with

<ul>

 <li><em>instance variables</em> o part – the part number o description – the part description</li>

</ul>

o count – how many o price – cost per item

<ul>

 <li>A <em>constructor</em> that initializes them o public Invoice(String part, String description, int count, double price)</li>

 <li><em>getters</em> and <em>setters</em></li>

 <li>A <em>toString</em> method – returns String representation of Invoice Object.</li>

 <li>An overridden <em>getPaymentAmount</em> method – returns the cost of the invoice</li>

</ul>

<strong>Note</strong>: <em>toString</em> and <em>getPaymentAmount</em> use the get methods rather than directly accessing the variables.

<h2>The Employee class</h2>

<ul>

 <li>Should be an <em>abstract class</em> because it does not implement the <em>getPaymentMethod</em>. You cannot create an object whose class is Employee. For example:</li>

</ul>

Employee employee007 = new Employee(“James”, “Bond”, “007-00-7007”); would cause a runtime error.

<ul>

 <li><em>instance variables.</em></li>

</ul>

o <sub>first</sub> – first name of employee o <sub>last</sub> – last name of employee o <sub>ssn</sub> – SSN of employee

<ul>

 <li><em>getters </em>and <em>setters</em></li>

 <li>A <em>constructor </em>that initialize the variables of the class o Public Employee(String first, String last, String ssn)</li>

</ul>

One might wonder what the constructor is good for. This code will be called by the constructors of the subclasses.

<ul>

 <li>A <em>toString</em> method – returns String representation of Employee Object.</li>

</ul>

<h2>Subclasses of Employee</h2>

Each of the subclasses have the following features:

<ul>

 <li>It extends the Employee class or a subclass of Employee.</li>

 <li>The parameters of its constructor include values to initialize all the instance variables of the class and its superclasses.</li>

 <li>The first line of code in the constructor calls the constructor of the immediate superclass. Note the use of the super keyword. This is good practice in inheritance hierarchies.</li>

 <li>The <em>getPaymentAmount</em> method is implemented, fulfilling the promise made by the Employee class.</li>

 <li>The toString method combines the result of the toString method of the superclass with additional information. Again, note the use of the super keyword.</li>

 <li>The constructor, getPaymentAmount and toString methods use the getters and setters to get and set the instance variables. One reason is that instance variables from the superclasses are private, so there is no other way to access and modify these variables. The other reason is that the setters include code to validate (or at least partially validate) the new values.</li>

</ul>

<h2>CommissionEmployee Class</h2>

<em>Commission employees are paid a percentage of their sales</em>

<ul>

 <li><em>instance variabes</em> o grossSales – gross sales of employee (throw an exception when &lt;= 0.0) o commissionRate – commission rate of employee (throw an exception when rate is not between 0.0 to 1.0)</li>

 <li><em>getters </em>and <em>setters</em> A <em>constructor</em> public CommissionEmployee(String first, String last, String ssn, double sales, double rate)</li>

 <li>A <em>toString </em>method – Overrides <em>toString </em>method in class Employee and returns String representation of CommissionEmployee Object.</li>

</ul>

<h2>HourlyEmployee Class</h2>

<em>Hourly employees are paid by the hour and receive overtime pay (i.e., 1.5 times their hourly salary rate) for all hours worked in excess of 40 hours.</em>

<ul>

 <li><em>instance variabes</em>

  <ul>

   <li>wage – hourly wage of employee (throw an exception when &lt;= 0.0)</li>

   <li>hours – number of hours worked by employee (throw an exception when hours is not between 0.0 to 168.0)</li>

  </ul></li>

 <li><em>getters </em>and <em>setters</em></li>

 <li>A <em>constructor</em></li>

</ul>

public HourlyEmployee(String first, String last, String ssn, double hourlyWage, double hoursWorked)

<ul>

 <li>A <em>toString </em>method – Overrides <em>toString </em>method in class Employee and returns String representation of HourlyEmployee Object.</li>

</ul>

<h2>SalariedEmployee Class</h2>

<em>Salaried employees are paid a fixed weekly salary regardless of the number of hours worked </em>

<ul>

 <li><em>instance variabes</em> o weeklysalary – hourly wage of employee (throw an exception when &lt;= 0.0)</li>

 <li><em>getters </em>and <em>setters</em> A <em>constructor</em> public SalariedEmployee(String first, String last, String ssn, double salary)</li>

 <li>A <em>toString </em>method – Overrides <em>toString </em>method in class Employee and returns String representation of SalariedEmployee Object.</li>

</ul>

<h2>BasePlusCommissionEmployee Class</h2>

<em>Base-salaried commission employees receive a base salary plus a percentage of their sales. </em><em>For the current pay period, the company has decided to reward salaried-commission employees by adding 10% to their base salaries </em>

<ul>

 <li><em>instance variabes</em> o baseSalary – base salary of employee (throw an exception when &lt;= 0.0)</li>

 <li><em>getters </em>and <em>setters</em></li>

 <li>A <em>constructor</em></li>

</ul>

public BasePlusCommissionEmployee(String first, String last, String ssn, double sales, double rate, double salary)

A <em>toString </em>method – Overrides <em>toString </em>method in class Employee and returns String representation of BasePlusCommissionEmployee Object.

<strong>Testing (main method): </strong>

The PayrollSystemTest Main Method:

<ul>

 <li>The <u>main method</u> for <em>java</em> should uses the <strong>Employee class</strong> and its subclasses.</li>

 <li>It should first creates four objects, one for each subclass of Employee.</li>

</ul>

<strong>Note</strong>: the constructors have different numbers of parameters.

For example, a BasePlusCommissionEmployee object will need information for six instance variables (one in BasePlusCommissionEmployee class and five in superclasses). Also, the BasePlusCommissionEmployee constructor needs some way to initialize the private variables from the superclasses.

Sample of an object creation

SalariedEmployee salariedEmployee = <strong>new </strong>SalariedEmployee(“John”, “Smith”,”111-11-1111″, 800.00);

<ul>

 <li>Then the next group of statements should prints information about each object individually. For this to work, use <em>toString </em>method from each subclass and needs a getPaymentAmount method.</li>

</ul>

Sample

System.out.println( “Employees processed individually:
” );

System.out.printf( “%s
%s: $%,.2f

”, salariedEmployee, “earned”, salariedEmployee.getPaymentAmount() );

<strong>Note: </strong>Learn about <a href="https://docs.oracle.com/javase/tutorial/java/data/numberformat.html">Formatting with printf()</a>

<ul>

 <li>The next group of statements (creation of array through the first for loop) should prints information about each object polymorphically.</li>

 <li>The objects are stored in an Employee array. o The for loop will depend on the same toString and getPaymentAmount methods as the previous group of statements.</li>

 <li>An if statement inside the for loop should illustrates how to write code specific to one of the Employee subclasses. (Hint: use instanceof)</li>

 <li>The if condition tests whether currentEmployee belongs to the subclass. o The first statement inside the if casts the Employee object to the subclass.</li>

 <li>This is needed because setBaseSalary and getBaseSalary are methods in the BasePlusCommissionEmployee class, but of Employee or other subclasses of Employee.</li>

 <li>The last for loop illustrates how to find out the specific class for each object. (Hint: use getClass())</li>

</ul>










<strong><em>Continue to next page… </em></strong>

Workshop Header




/**********************************************

<strong>Workshop #  </strong>

<strong>Course:</strong><em>&lt;subject type&gt; – Semester </em>

<strong>Last Name:</strong><em>&lt;student last name&gt; </em>

<strong>First Name:</strong><em>&lt;student first name&gt; </em>

<strong>ID:</strong><em>&lt;student ID&gt; </em>

<strong>Section:</strong><em>&lt;section name&gt; </em>

<em>This assignment represents my own work in accordance with Seneca Academic Policy. </em>

<em>Signature </em>

<strong>Date:</strong><em>&lt;submission date&gt; </em>

**********************************************/




<strong> </strong>

Code Submission Criteria:

Please note that you should have:

<ul>

 <li>Appropriate indentation.</li>

 <li>Proper file structure</li>

 <li>Follow java naming convention</li>

 <li>Document all the classes properly</li>

 <li>Do Not have any debug/ useless code and/ or files in the assignment</li>

 <li>Do not have everything in the <em>main method</em>.</li>

 <li>Have a separate TestClass with the main method in it.</li>

 <li>Check your inputs if the user is not entering garbage inputs.</li>

 <li>Use exceptional handling or other methods to let the user know if the inputs are incorrect.</li>

</ul>




Deliverables and Important Notes:




<strong>All these deliverables are supposed to be uploaded on the blackboard once done. </strong>

<strong> </strong>

<ul>

 <li>You are supposed to create video/ record voice/ detailed document of your running solution. <strong>(50%)</strong>  o Screen Video captured file should state your last name and id, like</li>

</ul>

Ali_123456.mp4 (or whatever the extension of the file is) o Record voice clip should also include a separate word file with the screen shots of your program’s output, state your last name and id, like Ali_123456.mp3 (or whatever the extension of the file is)

o Detailed document should include screen shots of your output, have your name and id on the top of the file and save the file with your last name and id, like Ali_123456.docx (or whatever the extension of the file is)

<ul>

 <li>A word/ text file which will reflect on learning of your concepts in this workshop. Also include the instructions on how to run your code.                           <strong>(30%)</strong>

  <ul>

   <li>Should state your Full name and Id on the top of the file and save the file with your last name and id, like Ali_123456.txt</li>

  </ul></li>

 <li>Submission of working code.                                                                      <strong>(20%)</strong>

  <ul>

   <li>Make sure your follow the “<strong>Code Submission Criteria”</strong> mentioned above.</li>

   <li>You should zip your whole working project to a file named after your Last Name followed by the first 3 digits of your student ID. For example, zip.</li>

  </ul></li>

 <li>Your marks will be deducted according to what is missing from the above-mentioned submission details.</li>

 <li>Late submissions would result in additional 10% penalties for each day or part of it.</li>

 <li>Remember that you are encouraged to talk to each other, to the instructor, or to anyone else about any of the assignments, but the final solution may not be copied from any source.</li>

</ul>


