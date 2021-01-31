# Report Portal

## Installation

- `mkdir report-portal && report-portal`
- `curl https://raw.githubusercontent.com/reportportal/reportportal/master/docker-compose.yml -o docker-compose.yml`
- `docker-compose -p reportportal up -d`
- `start http://localhost:8080`
- accounts
  - `default\1q2w3e` and
  - `superadmin\erebus`

Cloud:

- `start https://demo.reportportal.io/`

## Poetry

- `poetry init`
- `poetry add pytest`
- `poetry add pytest-reportportal`

## Write tests

- `mkdir tests && cd tests`
- write some tests

## Run tests

### Pytest.ini

Get access data from portal account and add to _pytest.ini_.

```ini
[pytest]
rp_endpoint = http://localhost:8080
rp_uuid = 072de04a-797e-4a24-8c92-02dee47dda5f
rp_launch = default_TEST_EXAMPLE
rp_project = default_personal
```

- `poetry run pytest --reportportal`

## Git

- `git init`
- `echo "\_\_pycache\_\_/" >> .gitignore`
- `echo ".vscode/" >> .gitignore`
- `echo data/" >> .gitignore`
