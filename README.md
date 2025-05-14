# Ex02 Django ORM Web Application
## Date: 

## AIM
To develop a Django application to store and retrieve data from a Movies Database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM



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
admin.py
```
from django.contrib import admin
from .models import book,bookadmin
admin.site.register(book,bookadmin)
```
models.py
```
from django.db import models
from django.contrib import admin
class book(models.Model):
    Book_name=models.CharField(max_length=100)
    Author=models.CharField(max_length=100)
    Co_author=models.CharField(max_length=100)
    Book_code=models.IntegerField()
    Publisher=models.CharField(max_length=100)
    MRP=models.IntegerField()
class bookadmin(admin.ModelAdmin):
    list_display=("Book_name","Author","Co_author","Book_code","Publisher","MRP")
```
urls.pr
```
from django.contrib import admin
from django.urls import path

urlpatterns = [
    path('admin/', admin.site.urls),
]
```

## OUTPUT
![image](https://github.com/user-attachments/assets/cbed9d91-d199-43ce-be22-cb3a84e05d9b)
![image](https://github.com/user-attachments/assets/cd2b9199-b4c3-444e-8c3a-dce5e4a275a4)
![image](https://github.com/user-attachments/assets/6e1a7168-1cf7-4c8b-a5d9-c2b7611b160e)

Include the screenshot of your admin page.
## RESULT
Thus the program for creating movies database using ORM hass been executed successfully
