# Ex02 Django ORM Web Application
## Date: 07/03/2024
## Name : H Vishinu 
## Reg.No : 212223220124
## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here
![ER diagram](https://github.com/VisHinu24/ORM/assets/144244396/0ec12a42-7709-4c28-811d-4c38b52072cc)

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
```
Models.py

from django.db import models
from django.contrib import admin

# Create your models here.
class Book(models.Model):
    book_id = models.IntegerField(primary_key=True)
    book_name = models.CharField(max_length=100)
    Author= models.CharField(max_length=50)
    Date= models.DateField()
    price = models.IntegerField()

class Display_book(admin.ModelAdmin):
    list_display = ('book_id','book_name','Author','Date','price')


Admin.py

from django.contrib import admin
from .models import Book,Display_book
# Register your models here.

admin.site.register (Book, Display_book)
```
## OUTPUT
![alt text](<Screenshot 2024-03-15 143800.png>)
![alt text](<Screenshot 2024-03-15 144146.png>)

## RESULT
Thus the program for creating a database using ORM hass been executed successfully
