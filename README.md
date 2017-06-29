# Deploy EC2

## requirements

**Python**

3.5.3

**pip**

```
pip install -r requirements.txt
```

## Create secret config files

### Project structure

```
project_folder/
	.conf_secret/
		settings_common.json
		settings_debug.json
		settings_deploy.json
	.django_app/
	...
	...
```

### settings_common.json example

```
{
  "django": {
    "secret_key": "Django project secret key"
  }
}
```

### settings_debug.json example

```
{
  "django": {
    "allowed_hosts": [
      "*"
    ]
  }
}
```

### settings_deploy.json example

```
{
  "django": {
    "allowed_hosts": [
      "*"
    ]
  }
}
```

## runserver

```
# local developement
python3 manage.py runserver --settings=config.settings.debug
```