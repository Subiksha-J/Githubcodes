# Inheritance
class Village(object):
    def __init__(self, name,pop):
        self.name = name
        self.pop=pop
    def display(self):
        print(self.name)
    def dispop(self):
        print("Total population",self.pop)
    def design(self):
        print("There is no school here")
class School(Village):
    def __init__(self,name,num,pop,schl):
        Village.__init__(self,name,pop)
        self.num = num
        self.schl=schl
    def design(self):
        print("The village has {} schools".format(self.num))
        print("The number of students in schools are ",self.schl)
vil= School("Tisaiyanvillai",2,1000,400)
vil.display()
vil.dispop()
vil.design()
vil1=Village("Idaichivillai",500)
vil1.display()
vil1.dispop()
vil1.design()
