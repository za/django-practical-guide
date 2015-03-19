Django Practical Guide
======================

Documentation on Django practical guide.

# Setup sphinx virtualenv

You can use *either* virtualenv *or* virtualenv with virtualenvwrapper installed. 

* virtualenv

    ```
    ~$ 
    ```
    *todo* ... 

    To start working on `sphinx` virtualenv

    ```
    ~$ 
    (sphinx) ~$
    ```
    
    To stop working on `sphinx` virtualenv

    ```
    (sphinx) ~$ deactivate
    ```


* virtualenv with virtualenvwrapper

    Create `sphinx` virtualenv

    ```
    ~$ mkvirtualenv sphinx
    ```

    To start working on `sphinx` virtualenv

    ```
    ~$ workon sphinx
    (sphinx) ~$
    ```
    
    To stop working on `sphinx` virtualenv

    ```
    (sphinx) ~$ deactivate
    ```

# Install sphinx

    pip install `sphinx`

    ```
    (sphinx) ~$ pip install sphinx 
    ```

# Build 

    Clone the git repository

    ```
    ~$ git clone https://github.com/marimore/django-practical-guide.git
    ```

    Change directory

    ```
    ~$ cd django-practical-guide/
    ~/django-practical-guide$ 
    ```

    Build html
 
    ```
    ~/django-practical-guide$ sphinx-build -b html . build/html
    ```

    Run the serve script 
    ```
    ~/django-practical-guide$ ./serve.sh
    Serving HTTP on 0.0.0.0 port 8000 ...
    ``` 

    Open in your favorite web browser
    ```
    http://localhost:8000
    ```

# Contribute

1. Fork the git repository
2. Make changes
3. Make pull request
4. Add another git remote repository to keep your forked repository updated
