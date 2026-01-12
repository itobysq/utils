# Code style
- Use Google Style Docstrings

# Testing
All testing is done through containers. 

To test things in the Python API use
docker compose exec -T \
-e DB_USER=application_user \
-e DB_PASSWORD=mypass \
-e DB_HOST=db \
-e B_PORT=5432 \
api uv run pytest tests/src/core_api/test_api.py
