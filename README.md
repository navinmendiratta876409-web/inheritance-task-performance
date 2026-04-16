# inheritance-task-performance
class Employee:
    def __init__(self,name,base_salary):
        self.name = name
        self.base_salary = base_salary
        
    def work(self):
        print(f"{self.name} kaam kr raha hai ")
        
class Manager(Employee):
    def __init__(self,name,base_salary,bonus):
        super().__init__(name,base_salary)
        
        self.bonus = bonus
    
    def show_total_salary(self):
        print(f"{self.base_salary + self.bonus} ")
        
class Developer(Employee):
    def __init__(self,name,base_salary,language):
        super().__init__(name,base_salary)
        self.language = language
    def code(self):
        print(f"{self.name} {self.language} me coding kr raha hai")
        
manager = Manager("Rahul",100000,25000)
developer = Developer("Navin",150000,"Python",)
manager.work()
developer.work()
manager.show_total_salary()
developer.code()

