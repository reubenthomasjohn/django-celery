uv venv --python 3.12
uv pip freeze > requirements.txt
chmod +x ./entrypoint.sh
docker compose up -d --build
