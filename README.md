# `with-dotenv`

A simple way to load an env file into your environment before executing something.

### Example usage

```
$ git clone git@github.com:spadin/with-dotenv.git
$ cd with-dotenv
$ tree -a .
.
├── .env
├── README.md
├── example-script.sh
└── with-dotenv

$ cat .env
MY_ENV_VAR=test
ACCESS_KEY=access-key
SECRET_KEY=super-secret

$ cat ./example-script.sh
echo "MY_ENV_VAR: $MY_ENV_VAR"
echo "ACCESS_KEY: $ACCESS_KEY"
echo "SECRET_KEY: $SECRET_KEY"

$ ./example-script.sh
MY_ENV_VAR:
ACCESS_KEY:
SECRET_KEY:

$ ./with-dotenv .env ./example-script.sh
MY_ENV_VAR: test
ACCESS_KEY: access-key
SECRET_KEY: super-secret
```
