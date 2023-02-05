# 36.

<img width="886" alt="Screen Shot 2023-02-05 at 12 44 47" src="https://user-images.githubusercontent.com/111941990/216800402-ff423e36-2cb2-4af3-a533-69545ea8678d.png">


## Code
```.py
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def get_name(self) -> str:
        return self.name

    def get_age(self):
        return self.age


class Student(Person):
    def __init__(self, name, age, grade):
        super().__init__(name, age)
        self.grade = grade

    def get_grade(self):
        return self.grade


class Classroom:
    def __init__(self):
        self.students = []

    def add_student(self, student):
        self.students.append(student)

    def remove_student(self, student):
        if student not in self.students:
            raise ValueError
        else:
            self.students.remove(student)

    def get_average_score(self):
        if len(self.students) == 0:
            raise ValueError
        total = 0
        for student in self.students:
            total += student.get_grade()
        average = total / len(self.students)
        return average

```

## UML
<img width="596" alt="Screen Shot 2023-02-05 at 17 20 14" src="https://user-images.githubusercontent.com/111941990/216808788-7a2854ed-6c3f-48df-8911-77a01c7b694a.png">
