public class UniversitySystem {
public static void main(String[] args) {
}

private Course_Node Course_head; //head of the course linked list
private Course_Node Course_Tail; //tail of the course linked list
private Student_Node Student_head;
private Student_Node Student_Tail;

public UniversitySystem() {
    Course_head = null;
    Course_Tail = null;
    Student_head = null;
    Student_Tail = null;
  } 

  //Student class
  class Student_Node{  
    private int size;
    private int IDStudnt;
    private Student_Node next;
    public Student_Node(){
    }
    public Student_Node(int IDStudnt){
    this.IDStudnt=IDStudnt;
    this.next=null;
    }
    public Student_Node(int IDStudnt,Student_Node next){
    this.IDStudnt=IDStudnt;
    this.next=next;
    }
  }
  
  //Course class
  class Course_Node{
    private int size;
    private int IDCourse;
    private String NameCourse;
    Course_Node next;
    public Course_Node(){
    }
    public Course_Node(int IDCourse,String NameCourse){
      this.IDCourse=IDCourse;
      this.NameCourse=NameCourse;
    }
    public Course_Node(int IDCourse,String NameCourse,Course_Node next){
      this.IDCourse=IDCourse;
      this.NameCourse=NameCourse;
      this.next=next;
    }
  }

  //PrintCourseNode method
  public void PrintCourseNode(){
    Course_Node tmp=Course_head;
    while (tmp != null) {
      System.out.print("ID course: "+tmp.IDCourse + ", Name of course is: "+ tmp.NameCourse + " -> ");
      tmp= tmp.next;
    }
    System.out.println("null");
  } 

  //PrintStudent method
     public void PrintStudent(){
      Student_Node tmp=Student_head;
      while (tmp != null) {
        System.out.print("ID stusdent: "+tmp.IDStudnt + " -> ");
        tmp= tmp.next;
      }
       System.out.println("null");
      } 

      //methods 
      public void addCourseToHead() { }
      public void addCouseToTail() { }
      public int deleteCourseFromHead()   { return 0;} 
      public int deleteCourseFromTail()   { return 0;}
      public void addStudentToHead() { }
      public void addStudentToTail() { }
      public int deleteStudentFromHead()   { return 0;}
      public int deleteStudentFromTail()   { return 0;}
      public int deleteNode() {return 0;}

}
