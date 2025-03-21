`uv venv --python 3.12`
`django-admin startproject dcelery`
`uv pip freeze > requirements.txt`
`chmod +x ./entrypoint.sh`
`docker compose up -d --build`
`./manage.py startapp taskapp`
`docker exec -it django /bin/sh`
`./manage.py shell`

docker exec -it django /bin/sh

tp1.delay()

from celery import group
from newapp.tasks import tp1, tp2, tp3, tp4, ...
task_group = group(tp1.s(), tp2.s(), tp3.s(), tp4.s())
task_group.apply_async()
