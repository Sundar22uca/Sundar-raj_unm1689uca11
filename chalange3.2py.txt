class Student:

  def __init__(self, name, roll_number, cgpa):
    self.name = name
    self.roll_number = roll_number
    self.cgpa = cgpa

  def __str__(self):
    return f"{self.name}, Roll Number: {self.roll_number}, CGPA: {self.cgpa}"


def sort_students(student_list):
  sorted_students = sorted(student_list, key=lambda x: x.cgpa, reverse=True)
  return sorted_students


# Example usage:
student1 = Student("Alice", "A101", 3.8)
student2 = Student("Bob", "B102", 3.6)
student3 = Student("Charlie", "C103", 4.0)
student4 = Student("David", "D104", 3.9)

students = [student1, student2, student3, student4]

sorted_students = sort_students(students)

print("Sorted Students:")
for student in sorted_students:
  print(student)
