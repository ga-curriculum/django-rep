# Django Rep

## Road Map

1. Setup
2. Toy Resource

## 1. Setup

This lesson continues to build-out Cat Collector right where the [_Django One to Many Models_](https://git.generalassemb.ly/SEB-Base-Curriculum/django-one-to-many-models) lesson left off.

Navigate to the django-catcollector directory, enter your virtual environment pipenv shell, then start the web server with python manage.py runserver.

You may notice this lesson looks rather short...that's because you are going to do most of the work. The more reps we do, the deeper our understanding becomes. Don't worry, you're not alone!

## 2. Toy Resource

For this lesson we will add a `Toy` model and associated Serializer/CBV’s/URLs.

### Toy Model

Start by adding the `Toy` model to our project. This model has a name and a color field. Set the fields to models.CharField data type with a max_length of 50 and 20, respectively. Don't forget to override the __str__ method to display the toy's name property.

<details>
<summary>
❓ Give it a try - we will review the answer in 5 minutes.
</summary>

  ```python
  # Add the Toy model
  class Toy(models.Model):
    name = models.CharField(max_length=50)
    color = models.CharField(max_length=20)

    def __str__(self):
      return self.name
  ```
  
</details>

### Admin
A new model means new entry in `**admin.py**`. Here it is!

```python
from django.contrib import admin

from .models import Cat, Feeding, Toy

admin.site.register(Cat)
admin.site.register(Feeding)
#Add the Toy model
admin.site.register(Toy)
```

