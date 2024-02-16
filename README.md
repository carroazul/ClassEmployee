// Employee implements program //
package disagn;
class Employee {
    //attributes of Employee class
    private String firstName;
    private String lastName;
    private int employeeID;
    private double salary;


    public Employee() { //default constructor
        firstName = null;
        lastName = null;
        employeeID = 0;
        salary = 0.0;

    }

    public void setFirstName(String fname) { //set and get methods for all attributes
        firstName = fname;
    }

    public String getFirstname() {
        return firstName;
    }

    public String getLastName() {
        return lastName;
    }
    public void setLastName(String lname) {
        lastName = lname;
    }

    public double getEmployeeID() {
        return employeeID;
    }

    public void setEmployeeID(int empId) {
        employeeID = empId;

    }

    public double getSalary() {
        return salary;
    }

    public void setSalary(double s) {
        salary = s;
    }

    public void EmployeeSummary() { //display all assign of Employee
        System.out.println("Employee Name: " + firstName + " " + lastName + " Employee Id :" + employeeID + " salary: " + salary);
    }
}

class Manager extends Employee {
    private String department;


    public Manager() { //default constructor
        super();                           //calling superior base class default constructor
        department = null;
    }

    public String getDepartment() {
        return department;
    }

    public void setDepartment(String dept) { //set and get methods for department
        department = dept;
    }

    public void EmployeeSummary() {
        super.EmployeeSummary();     //calling super class method with same name
        System.out.println(STR."Department : \{department}");
    }
}

class TestEmployee {
    public static void main(String[] args) {
        Manager mgr = new Manager();
        mgr.setFirstName("Carlos J");        //all set methods of super class are available to derived class
        mgr.setLastName("Delgado");
        mgr.setEmployeeID(42158);
        mgr.setSalary(6.0E04);
        mgr.setDepartment("Accounts department");
        mgr.EmployeeSummary();
    }
}
