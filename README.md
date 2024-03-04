# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:
install myapp using 'python mnage.py startapp [your app name] ' command 

### STEP 2:
first edit 'settings.py' and then edit 'models.py' and then edit 'admin.py' with the appropriate codes .

### STEP 3:
create a user name and password usingfor your django  'python manage.py createsuperuser'
and then run the program using 'python manage.py runserver [your port number]'
### STEP 4:
login with your username and password in django and select student table and then add 10 students detials.
## STEP 5:
End the Program
## PROGRAM
## code to edit in 'models.py'
```

from django.db import models
from django.contrib import admin


# Create your models here.
class Student (models.Model):
    referencenumber=models.CharField(primary_key=True,max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    number=models.IntegerField()

class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','number')



```
## codes to edit in 'admin.py'
```
from django.contrib import admin
from .models import Student,StudentAdmin


# Register your models here.
admin.site.register(Student,StudentAdmin)


```

## OUTPUT
![adminoutput](https://github.com/Kishorerz/django_orm_app/assets/144451216/b15647e6-b985-463d-b534-7e5895831124)




## RESULT
The student table is created successfully and the program successfully Executed.
