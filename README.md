# python_packagingPythonProjects
Practice Python Package files : https://packaging.python.org/tutorials/packaging-projects/

# Example Package

This is a simple example package. You can use
[Github-flavored Markdown](https://guides.github.com/features/mastering-markdown/)
to write your content.

Key take aways:
1. In each module, have a __init__.py file
2. Create a LICENSE / README / setup.py file at root level
3. Register a test account : https://test.pypi.org/account/register/ 
4. Create your source and build distribution files
with this commands (make sure wheel is installed):
    * python3 -m pip install --user --upgrade setuptools wheel
    * python3 setup.py sdist bdist_wheel
5. When pushing your source code to test distrubution
    * Make sure twine is installed
    ** python3 -m pip install --user --upgrade twine
    * Push to test distrobution
    ** python3 -m twine upload --repository-url https://test.pypi.org/legacy/ dist/*
6. To test your newly pushed code, pull down from test.pypi repo
    * Install virtualenv (sandbox env for python)
    ** pip install virtualenv
    ** virtualenv ENV_NAME
    ** ENV_NAME active
    * pull down code from pip
    ** python3 -m pip install --index-url https://test.pypi.org/simple/ --no-deps example-pkg-your-username

to review, look back at the original documentation 
https://packaging.python.org/tutorials/packaging-projects/