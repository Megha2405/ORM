# Ex02 Django ORM Web Application
## Date: 05/02/2026

## AIM
To develop a Django application to manage an online food delivery platform like Zomato/Swiggy using Object Relational Mapping (ORM).

## ENTITY RELATIONSHIP DIAGRAM

![alt text](<Screenshot 2026-02-04 235914.png>)

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
admin.py

from django.contrib import admin
from .models import Employee

class EmployeeAdmin(admin.ModelAdmin):
    list_display = (
        'OrderID',
        'UserID',
        'OrderDate',
        'ItemName',
        'OrderQty',
        'UnitPrice',
        'TotalAmount',
        'DeliveryAddress'
    )

admin.site.register(Employee, EmployeeAdmin)

models.py

from django.db import models

class Employee(models.Model):
    OrderID = models.IntegerField(primary_key=True)
    UserID = models.CharField(max_length=100)
    OrderDate = models.DateField()
    ItemName = models.CharField(max_length=100)
    OrderQty = models.IntegerField()
    UnitPrice = models.FloatField()
    TotalAmount = models.FloatField()
    DeliveryAddress = models.CharField(max_length=255)

    def __str__(self):
        return str(self.OrderID)

```



## OUTPUT

![alt text](<Screenshot 2026-02-04 233433.png>)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
