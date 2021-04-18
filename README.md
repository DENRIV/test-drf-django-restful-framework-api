# Test Django RESTful API

add : 

migrations

  __init__.py	(size 0)
 
 python manage.py makemigrations
 
python manage.py migrate

> check

SELECT * FROM puppies_puppy

#  name, age, breed, color,   created_at, updated_at




> run test
> 
python manage.py test

	Creating test database for alias 'default'...
  
	Ran 10 tests in 0.836s
  
	OK
  
	Destroying test database for alias 'default'...

> Serializers


class PuppySerializer(serializers.ModelSerializer):

    class Meta:
    
        model = Puppy
        
        fields = ('name', 'age', 'breed', 'color', 'created_at', 'updated_at')


> RESTful Structure

Endpoint	HTTP 	Method	CRUD Method	Result

puppies		GET	READ	Get		 all puppies

puppies/:id	GET	READ	Get		 a single puppy

puppies		POST	CREATE	Add		 a single puppy

puppies/:id	PUT	UPDATE	Update 		a single puppy

puppies/:id	DELETE	DELETE	Delete 		a single puppy

test api


python manage.py runserver

http://localhost:8000/api/v1/puppies

# Run  test 

python manage.py test

or

manage.py test


# Run  test(s)

python manage.py test puppies.tests.test_views.GetAllPuppiesTest

python manage.py test puppies.tests.test_views.GetAllPuppiesTest.test_get_all_puppies

python manage.py test puppies.tests.test_views.GetSinglePuppyTest

python manage.py test puppies.tests.test_views.GetSinglePuppyTest.setUp

python manage.py test puppies.tests.test_views.GetSinglePuppyTest.test_get_valid_single_puppy

python manage.py test puppies.tests.test_views.GetSinglePuppyTest.test_get_invalid_single_puppy

python manage.py test puppies.tests.test_views.CreateNewPuppyTest

python manage.py test puppies.tests.test_views.UpdateSinglePuppyTest

python manage.py test puppies.tests.test_views

python manage.py test puppies.tests.test_models

python manage.py test puppies.tests

# 10 methods : test_*


[Source]

https://developer.mozilla.org/es/docs/Learn/Server-side/Django/Testing
