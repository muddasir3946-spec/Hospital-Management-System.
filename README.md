# Hospital-Management-System.
/*
Mini Project: 
Hospital Management System
These variables should be private.
Inheritance:
Person → Doctor
Person → Patient
Person → Nurse
Abstraction: Create an abstract class Person with an abstract method showDetails().
Polymorphism: Each child class implements showDetails() differently.
Encapsulation:
Patient name
Patient ID
Medical record
*/
abstract class person{
    private String name;
    private int age;
    person(String name , int age){
        this.name = name;
        this.age = age;
    }
    public String getName(){
        return name;
    }
    public int getAge(){
        return age;
    }
    abstract void displayInfo();
}
class doctor extends person{
    private int doctorId;
    private String specialization;
    doctor(String name , int age , int doctorId , String specialization){
        super(name,age);
        this.doctorId = doctorId;
        this.specialization = specialization;
    }
    public int getdoctorId(){
        return doctorId;
    }
    public String getSpecialization(){
        return 	specialization;
    }
    void displayInfo(){
        System.out.println("Name: " + getName());
        System.out.println("Age: " + getAge());
        System.out.println("Id: " + doctorId);
        System.out.println("Speaclization: " + 	specialization);
    }
}
class Patient extends person{
    private int patientId;
    private String medicalRecoard;
    Patient(String name , int age , int patientId , String medicalRecoard){
        super(name,age);
        this.patientId = patientId;
        this.medicalRecoard = medicalRecoard;
    }
    public int getPatientId(){
        return patientId;
    }
    public String getMedicalRecoard(){
        return medicalRecoard;
    }
    public void displayInfo(){
        System.out.println("Name: " + getName());
        System.out.println("Age: " + getAge());
        System.out.println("Pateint Id: " + patientId);
        System.out.println("Medical Recoard: " + medicalRecoard);
    }
}
class nurse extends person{
    private int nurseId;
    private String department;
    nurse(String name , int age , int nurseId , String department){
        super(name,age);
        this.nurseId = nurseId;
        this.department = department;
    }
    public int getNurseId(){
        return nurseId;
    }
    public String getDepartment(){
        return department;
    }
    public void displayInfo(){
        System.out.println("Name: " + getName());
        System.out.println("Age: " + getAge());
        System.out.println("Nurse Id: " + nurseId);
        System.out.println("Departemnt: " + department);
    }
}

class Main {
    public static void main(String[] args) {
        doctor d = new doctor("Ahsan",22,1122,"Computer Science");
        Patient p = new Patient("Raza",12,3333,"fever");
        nurse n = new nurse("laiba",19,4444,"OPD");
        d.displayInfo();
        System.out.println();
        p.displayInfo();
        System.out.println();
        n.displayInfo();
        System.out.println();
    }
}
