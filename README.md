# django-testing-tutorial

1 ) D:\subject\django-testing-tutorial-master\budgetproject>python manage.py test
System check identified no issues (0 silenced).

----------------------------------------------------------------------
Ran 0 tests in 0.000s

OK

after creating __init__.py in tests folder

2 ) D:\subject\django-testing-tutorial-master\budgetproject>python manage.py test budget
System check identified no issues (0 silenced).
F
======================================================================
FAIL: test_list_url_is_resolved (tests.test_urls.TestUrls)
----------------------------------------------------------------------
Traceback (most recent call last):
  File "D:\subject\django-testing-tutorial-master\budgetproject\budget\tests\test_urls.py", line 5, in test_list_url_is_resolved
    assert 1 ==2
AssertionError

----------------------------------------------------------------------
Ran 1 test in 0.001s

FAILED (failures=1)

3 ) class TestUrls(SimpleTestCase):        (/tests.py/test_urls.py)
    def test_list_url_is_resolved(self):
        url = reverse('list')
        print(resolve(url))  

D:\subject\django-testing-tutorial-master\budgetproject>python manage.py test budget
System check identified no issues (0 silenced).
ResolverMatch(func=budget.views.project_list, args=(), kwargs={}, url_name=list, app_names=[], namespaces=[], route=)
.
----------------------------------------------------------------------
Ran 1 test in 0.011s

OK

4 ) def test_list_url_is_resolved(self):
        url = reverse('add')
        print(resolve(url))
        self.assertEqual(resolve(url).func, ProjectCreateView)  

   D:\subject\django-testing-tutorial-master\budgetproject>python manage.py test budget
System check identified no issues (0 silenced).
E
======================================================================
ERROR: tests.test_urls (unittest.loader._FailedTest)
----------------------------------------------------------------------
ImportError: Failed to import test module: tests.test_urls
Traceback (most recent call last):
  File "C:\Python38\lib\unittest\loader.py", line 436, in _find_test_path
    module = self._get_module_from_name(name)
  File "C:\Python38\lib\unittest\loader.py", line 377, in _get_module_from_name
    __import__(name)
  File "D:\subject\django-testing-tutorial-master\budgetproject\budget\tests\test_urls.py", line 11
    def test_list_url_is_resolved(self):
                                       ^
IndentationError: unindent does not match any outer indentation level     