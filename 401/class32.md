# Django REST Framework Permissions
in the WWW development, permessions stand for granting or denying the request made, wheather it's an API request, login or other operation being done on the internet.
  
## How permissions are determined?
permessions in REST framework are defined as list of classes, once the website is being called it checks for permission before even the home page is viewed.
there are many responses for failing, **403 forbidden** or **401 unauthorized**

## setting the permission policy
it's being set in settings.py using DEFAULT_PERMISSION_CLASSES:
```python
REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permissions.IsAuthenticated',
    ]
}
```
and if not specified, here's the default value for it:
```python
# the default is allowing unrestricted access
'DEFAULT_PERMISSION_CLASSES': [
   'rest_framework.permissions.AllowAny',
]
```
## Custom Permission Examples
User Properties
You may want to give different levels of access to different users, based on their properties -- i.e., are they the creators of the object or are they a staff member?

Let's say you don't want staff members to be able to edit objects. Here's how a custom permission class for that case might look like:

# permissions.py

```python
from rest_framework import permissions


class AuthorAllStaffAllButEditOrReadOnly(permissions.BasePermission):

    edit_methods = ("PUT", "PATCH")

    def has_permission(self, request, view):
        if request.user.is_authenticated:
            return True

    def has_object_permission(self, request, view, obj):
        if request.user.is_superuser:
            return True

        if request.method in permissions.SAFE_METHODS:
            return True

        if obj.author == request.user:
            return True

        if request.user.is_staff and request.method not in self.edit_methods:
            return True

        return False
```
Here, the AuthorAllStaffAllButEditOrReadOnly class extends BasePermission and overrides both has_permission and has_object_permission.
