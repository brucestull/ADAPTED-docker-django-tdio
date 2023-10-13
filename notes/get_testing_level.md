# Get Django Testing Level

## Process

1. Start the docker container

```bash
docker compose -f docker-compose.yml up --build
```

1. Use `coverage` to get the testing level

```bash
docker compose exec web coverage run manage.py test
```

1. Get the coverage report

```bash
docker compose exec web coverage report
```

## Results

```bash
(app) flynntknapp@DELL-GAME-DESK:~/Programming/ADAPTED-docker-django-tdio$ docker compose exec web coverage run manage.py test
Found 34 test(s).
Creating test database for alias 'default'...
System check identified no issues (0 silenced).
..................................
----------------------------------------------------------------------
Ran 34 tests in 1.894s

OK
Destroying test database for alias 'default'...
(app) flynntknapp@DELL-GAME-DESK:~/Programming/ADAPTED-docker-django-tdio$ docker compose exec web coverage report
Name                                  Stmts   Miss  Cover
---------------------------------------------------------
accounts/__init__.py                      0      0   100%
accounts/admin.py                        16      0   100%
accounts/apps.py                          4      0   100%
accounts/forms.py                        10      0   100%
accounts/migrations/0001_initial.py       8      0   100%
accounts/migrations/__init__.py           0      0   100%
accounts/models.py                        6      0   100%
accounts/tests/__init__.py                0      0   100%
accounts/tests/test_admin.py             53      0   100%
accounts/tests/test_forms.py              0      0   100%
accounts/tests/test_models.py            24      0   100%
accounts/tests/test_views.py             88      0   100%
accounts/urls.py                          3      0   100%
accounts/views.py                        40      0   100%
config/__init__.py                        0      0   100%
config/settings.py                       27      0   100%
config/urls.py                            9      1    89%
manage.py                                12      2    83%
upload/__init__.py                        0      0   100%
upload/admin.py                           1      0   100%
upload/apps.py                            4      0   100%
upload/migrations/__init__.py             0      0   100%
upload/models.py                          1      0   100%
upload/tests.py                           1      0   100%
upload/views.py                          11      8    27%
---------------------------------------------------------
TOTAL                                   318     11    97%
(app) flynntknapp@DELL-GAME-DESK:~/Programming/ADAPTED-docker-django-tdio$
```
