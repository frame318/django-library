## django-cloudinary
> upload medie ไปที่ cloudinary
```python
pip install cloudinary
pip install django-cloudinary-storage
```
```python
INSTALLED_APPS = [
    'cloudinary_storage',
    'cloudinary',
]
```
```python
CLOUDINARY_STORAGE = {
    'CLOUD_NAME': 'YOUR_CLOUD_NAME',
    'API_KEY': 'YOUR_API_KEY',
    'API_SECRET': 'YOUR_API_SECRET',
}
DEFAULT_FILE_STORAGE = 'cloudinary_storage.storage.MediaCloudinaryStorage'
```
## django-admin-rangefilter
> เพิ่มการค้นหาด้วย วัน-เวลา ในหน้า Admin
```python
pip install django-admin-rangefilter
```
```python
INSTALLED_APPS = (
    ...
    'rangefilter',
    ...
)
```
```python
from rangefilter.filter import DateRangeFilter
class PostAdmin(admin.ModelAdmin):
    list_filter = (
        ('news_date', DateRangeFilter),
    )
```
## django-feather
> ใส่ icon หน้าเว็บด้วย feather

> https://feathericons.com/
```python
pip install django-feather
```
```python
INSTALLED_APPS = [
    'django_feather',
]
```
```python
{% load icon %}
{% icon "coffee" class="css-class" height="40" width="40" %}
```
