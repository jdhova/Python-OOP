

### PYTHON OOP
```

Procedual Programing is the use of functions and the variable is freely moving and can be accessed so this means anyone can update. this alos means its not secured.
Example we may want to make name accessible to everyone but make passwrod hidden, we can do this with OOP

variables = Attributes
Functions =  Methods

class Ceo:
   def __init__(self,vpname,vpdept,vpeducation):
       self.name=vpname
       self.dept=vpdept
       self.education=vpeducation

vp1=Ceo('Jude','Tech','Msc in DS')
vp2=Ceo('Grace','Finance','Msc in Finance')
vp3=Ceo('Jayden','Operations','Msc in Business')

print(vp1.name,vp2.dept,vp3.education)


class Test:
    pi = 3333

    def __init__(self,distance,radius):
        self.distance = distance
        self.radius = radius
        # self.pie = pie

    def peri(self,pie,dist):
        return pie * dist

    def area(self,pie,red):
        return pie * (red * red)

cirProp = Test(20,10)

print(f"cirl is {Test.pi}")
print (cirProp.peri(100,10))
print(cirProp.area(100,20))



```

### OOP CLASSES

```

class Bank:
    def __init__(self,holdername,holderbalance):
        self.name = holdername
        self.balance = holderbalance

    def Deposit(self,amount):
        self.balance =  self.balance + amount
        return (f'Congratulations {self.name} you just Deposited {amount} and your balance is {self.balance}')


    def Withdraw(self,amount):
        if(self.balance > amount):
            self.balance = self.balance - amount
            return (f'Congratulations {self.name} you just withdrawn {amount} and your balance is {self.balance}')
        else:
            return (f' Hi {self.name}  you just  tried withdrawing this {amount} However this is your balance {self.balance}')




Judeacct = Bank('Jude',300)

Grceacct = Bank('Grace',800)


print( Judeacct.Deposit(30))
print( Judeacct.Withdraw(5000))


print( Grceacct.Deposit(5000))
print( Grceacct.Withdraw(34))


def __str__

```

### INHERITANCE in OOP

#### Single Inheritance
```


class Person:
    def __init__(self,occupation):
        self.company = 'CompanyA'
        self.occupation = occupation   ### reusing this attributes from parent

    def city(self):
        return 'I am from Halifax'   ### reusing this methods from parent

    def country(self):
        return 'I am from Canada'



class Person1(Person):
    def __init__(self,name,job):
        super().__init__(job)            ### Super() helps in inheriting the attributes occupation from parent
        self.name = name

    def city(self):
        super().city()
        return 'I am from Toronto'

class Person2(Person):
    def __init__(self,name,job):
        super().__init__(job)
        self.name = name

    def city(self):
        return 'I am from New Brunswick'

    def display(self):
        return(f' My name is {self.name} and '
               f'I am from {self.country()} and i work as a {self.occupation}')


PersonNew = Person1('Jude','Developer')
PersonNew2 = Person2('James','Project Manager')

#
print(f' my name is {PersonNew2.name} and  {PersonNew2.city()}, and my friend is from {PersonNew.city()}')
print(f' I am from {PersonNew2.country()} and my friend is also from {PersonNew.country()}')
print(f' we both work for {PersonNew.company},{PersonNew2.company}')
print(f'He is a  {PersonNew.occupation} and I am {PersonNew2.occupation}')

print(PersonNew2.display())


```

#### Double Multiple Inheritance

```

class Father:
    def __init__(self, surname):
        self.name = surname
        self.citizenship = 'Canadian'

    def tall(self):
        return ('I am tall')


class Mother:
    def __init__(self, mname):
        self.mname = mname

    def goodloking(self):
        return ('I am goodloking')



class Daugter(Father,Mother):
    def __init__(self, name,mname,hobbies):
        Father.__init__(self, name)
        Mother.__init__(self, mname)
        self.hobbies = hobbies

    def cooking(self):
        return ('cooking')

    def display(self):
        return (f'My name is {self.name} and my mothers name is {self.mname} '
                f'{self.goodloking()} like my Mother and '
                f'  {self.tall()} like my father '
                f' I also enjoy {self.cooking()} and {self.hobbies}, and I am {self.citizenship}')

Daugter1 = Daugter('Coker','Adams','coding')

print(Daugter1.display())



```

####  Multiple Level Inheritance (Family Tree)
```


class GrandFather:
    def __init__(self, gname):
        self.gname = gname
        self.Citizenship = 'Canadian'

    def occupation(self):
        return 'founder of company'


class Father(GrandFather):
    def __init__(self, fathersname,gname):
        GrandFather.__init__(self, gname)
        self.fathersname = fathersname
        self.gname = gname

    def father_occupation(self):
        return f'CEO of company'

    def display(self):
        return (f'My former name was {self.fathersname} and my fathers former name was {self.gname}'
                f'I am the {self.father_occupation()} and my father is the {self.occupation()}')
#
class Son(Father):
    def __init__(self, sonsname,gname,fathersname):
        GrandFather.__init__(self, gname)
        Father.__init__(self, fathersname,gname)
        self.sonsname = sonsname

    def son_occupation(self):
        return 'VP of company'

    def display(self):
        return (f'my grand Fathers name is {self.gname} and '
                f' fathers name is {self.fathersname} and'
                f' my name is {self.sonsname}'
                f' my grand Fathers is {self.occupation()} and fathers occupation is {self.father_occupation()}'
                f' and I am from {self.Citizenship} and my job is {self.son_occupation()}')

# #
Son1 = Son('Jude','Coles','Adams')
Father1 = Father('ColesMan','AdamsMan')

print(Son1.display())

print(Father1.display())


```

#### Method Resolution Order, gives an order of inheritance

### ABSTRACTION

#### Abstraction is similar to hiding the details of a function and other methods can over ride from the parent class
#### @abstraction methods must be declared to make methods abstract
#### we must mport ABC from abstractmethods
#### all sub classed must have method of the parent abstract class
#### Abstract Based Clases


#### Access Modifiers __Private _Protected and Public









### QUIZ

1. classes to show Mult level inheritance
2. classes should have hidden class where lower classes abstract methods 
3. classes must have access modifies where methods can be assesed public private and protected



