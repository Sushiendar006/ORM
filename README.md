# Ex02 Django ORM Web Application
## Date:11/03/2024 

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![WhatsApp Image 2024-03-22 at 10 30 36_34419c55](https://github.com/Sushiendar006/ORM/assets/169573954/5fa59c98-944d-4e4e-8ca3-5913866aeb9c)



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
models.py

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

admin.py

from django.contrib import admin
from .models import Book,Display_book

admin.site.register (Book, Display_book)
```

## OUTPUT:
![Screenshot 2024-04-11 211208](https://github.com/Sushiendar006/ORM/assets/169573954/b077b089-b0eb-41d1-81c7-bcf9fa127104)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
