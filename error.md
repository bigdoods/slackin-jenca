Steps taken:
adjusted docker-compose
built docker-compose
built puffin
puffin up
ERROR!!


puffin_1    | INFO  [alembic.runtime.migration] Context impl PostgresqlImpl.
puffin_1    | INFO  [alembic.runtime.migration] Will assume transactional DDL.
puffin_1    | User puffin already exists
puffin_1    | Traceback (most recent call last):
puffin_1    |   File "puffin.py", line 196, in <module>
puffin_1    |     manager.run()
puffin_1    |   File "/usr/local/lib/python3.6/site-packages/flask_script/__init__.py", line 412, in run
puffin_1    |     result = self.handle(sys.argv[0], sys.argv[1:])
puffin_1    |   File "/usr/local/lib/python3.6/site-packages/flask_script/__init__.py", line 383, in handle
puffin_1    |     res = handle(*args, **config)
puffin_1    |   File "/usr/local/lib/python3.6/site-packages/flask_script/commands.py", line 216, in __call__
puffin_1    |     return self.run(*args, **kwargs)
puffin_1    |   File "puffin.py", line 190, in up
puffin_1    |     init()
puffin_1    |   File "puffin.py", line 181, in init
puffin_1    |     machine_proxy()
puffin_1    |   File "puffin.py", line 73, in machine_proxy
puffin_1    |     if docker.install_proxy():
puffin_1    |   File "/usr/src/app/puffin/core/docker.py", line 146, in install_proxy
puffin_1    |     return _install("_proxy")
puffin_1    |   File "/usr/src/app/puffin/core/docker.py", line 164, in _install
puffin_1    |     application = get_application(name)
puffin_1    |   File "/usr/src/app/puffin/core/applications.py", line 69, in get_application
puffin_1    |     applications = get_applications()
puffin_1    |   File "/usr/local/lib/python3.6/site-packages/cachetools/__init__.py", line 50, in wrapper
puffin_1    |     v = func(*args, **kwargs)
puffin_1    |   File "/usr/src/app/puffin/core/applications.py", line 87, in get_applications
puffin_1    |     application = load_application(application_id)
puffin_1    |   File "/usr/src/app/puffin/core/applications.py", line 100, in load_application
puffin_1    |     application = Application(application_id)
puffin_1    |   File "/usr/src/app/puffin/core/applications.py", line 44, in __init__
puffin_1    |     self.main_image = compose_data["services"]["main"]["image"]
puffin_1    | KeyError: 'main'
puffin_puffin_1 exited with code 1
