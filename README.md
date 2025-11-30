public class Person {

    // Attributes (fields)
    private String name;
    private int age;

    // Constructor
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Method to introduce the person
    public void introduce() {
        System.out.println("Hello, my name is " + name + " and I am " + age + " years old.");
    }

    // Main method to create a person object and call introduce()
    public static void main(String[] args) {
        Person p = new Person("Idris", 25);
        p.introduce();
    }
}
public class Student extends Person {

    private String studentId;
    private String course;

    // Constructor
    public Student(String name, int age, String studentId, String course) {
        super(name, age); // calls Person's constructor
        this.studentId = studentId;
        this.course = course;
    }

    // Method specific to Student
    public void study() {
        System.out.println("Student " + studentId + " is studying " + course + ".");
    }

    public static void main(String[] args) {
        Student s = new Student("Idris", 25, "CS101", "Computer Science");
        s.introduce();  // from Person class
        s.study();      // from Student class
    }
}
