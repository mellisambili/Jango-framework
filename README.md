# Prompt-Powered Kickstart: A Beginner's Toolkit for Django Food Ordering System

## 1. Title & Objective

### Title:
Prompt-Powered Kickstart: A Beginner's Toolkit for Django Food Ordering System

### Objective:
This toolkit documents the journey of learning backend development using the Django framework. It showcases a structured learning progression, starting from basic web setup to building a functional food ordering web application.

The goal is to provide a clear and replicable guide for a beginner to:
- Set up a Django development environment
- Build a basic web application
- Develop a food ordering system with core features
- Understand backend concepts like models, views, and authentication
- Leverage generative AI to accelerate learning and debugging

### Why Django?
Django was chosen because it is beginner-friendly, secure, and designed for rapid development. It comes with built-in tools like authentication, database handling, and an admin panel, making it ideal for building real-world applications quickly.

### End Goal:
The project results in one functional MVP:
- **A Food Ordering Web Application** that allows users to:
  - View menu items
  - Add items to cart
  - Place orders
  - Interact with a backend system

## 2. Quick Summary of the Technology

### What is Django?
Django is a high-level Python web framework that enables developers to build secure and scalable web applications quickly. It follows the Model-View-Template (MVT) architecture.

### Where is it used?
- Web applications
- E-commerce platforms
- Content management systems

### Real-world examples:
- Instagram (uses Django for backend services)
- Pinterest

## 3. System Requirements

### Operating System:
- Windows, macOS, or Linux

### Tools & Editors:
- Python (3.x)
- Django
- VS Code

## 4. Installation & Setup Instructions

### Step 1: Install Python
Download from: https://www.python.org

### Step 2: Install Django
```bash
pip install django
```

### Step 3: Verify Installation
```bash
python --version
django-admin --version
```

### Step 4: Create Project
```bash
django-admin startproject food_project
cd food_project
python manage.py runserver
```

### Step 5: Create App
```bash
python manage.py startapp orders
```

## 5. Minimal Working Example (MVP)

### Project Structure
```
food_project/
│
├── food_project/
├── orders/
│   ├── models.py
│   ├── views.py
│   └── urls.py
```

### Basic Model Example
```python
from django.db import models

class FoodItem(models.Model):
    name = models.CharField(max_length=100)
    price = models.FloatField()
    description = models.TextField()
```

### Basic View
```python
from django.shortcuts import render
from .models import FoodItem

def menu(request):
    items = FoodItem.objects.all()
    return render(request, 'menu.html', {'items': items})
```

### Expected Outcome
- Display food items
- Allow user interaction
- Backend processes requests

## 6. AI Tools Utilized
- ChatGPT
- Gemini
- Claude

## 7. AI Prompt Journal

### Prompt 1: Conceptual Understanding
**"Explain Django architecture and how it compares to Flask."**
- 👉 Helped understand backend structure

### Prompt 2: Setup Guidance
**"Guide me step-by-step to install Django and create my first project."**
- 👉 Helped with environment setup

### Prompt 3: Debugging
**"Why is my Django server not running?"**
- 👉 Helped fix configuration issues

### Prompt 4: Project Development
**"Help me build a food ordering system with Django step-by-step."**
- 👉 Guided full project development

## 8. Common Issues & Fixes

| Issue | Cause | Fix |
|-------|-------|-----|
| Django not recognized | Not installed properly | Reinstall Django |
| Server not running | Wrong directory | Run inside project folder |
| Page not found | URL not configured | Add routes in urls.py |

## 9. References
- [Django Documentation](https://docs.djangoproject.com)
- [Python Docs](https://docs.python.org)