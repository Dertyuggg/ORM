# Ex01 Django ORM Web Application
## Date: 3/02/2026

## AIM
To develop a Django Application to store and retrieve data from an Online Food Delivery Database platform like Zomato or Swiggy using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM



## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Detect changes and create migration files that describe how to modify the database schema

### STEP 5:
Execute the migration files and update the database schema to match your Django models

### STEP 6:
Create a superuser with full access rights to all models and data through the admin interface.

### STEP 7:
Apply the migration files of the created app to the database

### STEP 8:
Execute Django admin using localhost and create details for 10 entries

## PROGRAM
```
models.py
from django.db import models
from django.contrib import admin
class customerDB(models.Model):
    customer_id = models.CharField(primary_key=True,max_length=10)
    name = models.CharField(max_length=100)
    email = models.EmailField()
    phone_number = models.CharField(max_length=15)
    address = models.CharField(max_length=100)
    time = models.DateTimeField()
    costomer_rating = models.CharField(max_length=10)
    charges = models.IntegerField()
    
class customerAdmin(admin.ModelAdmin):
    list_display = ('customer_id', 'name', 'email', 'phone_number', 'address', 'time', 'costomer_rating', 'charges')

admin.py
from django.contrib import admin
from .models import customerDB, customerAdmin
admin.site.register(customerDB, customerAdmin)
```

## OUTPUT

<img width="1920" height="1080" alt="Screenshot (14)" src="https://github.com/user-attachments/assets/e3bb3f98-c7a2-44f6-a20e-2c845e50d4a5" />




## RESULT
Thus the program for creating E-commerce website database using ORM hass been executed successfully
