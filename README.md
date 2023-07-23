# tutorial-transformers
Introduction to machine learning platforms and ML Flow

[Slides](https://docs.google.com/presentation/d/18QDEEocdfVoyKGkGgDKhdjaslEBfEWiIORwUIQwICKs/edit?usp=sharing)

## Customizing the container

If you just want to learn about mlflow, this is useless

but if you wanna have full control over it, this is probably the type of thing that you'll need to do

just execute in a terminal, from the main folder of the repository:

```bash
docker-compose -f customized-container/docker-compose.yml up
```

and go to the address `http://127.0.0.1:8888?token=c61a728d-f4e6-45f0-9bb6-65646801f994`

and you should be able to run the same notebooks as in the last part

**Cautionary note:** the file `customized-container/.env` stores the token above. Usually this file is used to store secrets/keys/credentials, and thus it's ignored in the git repo (using the `.gitignore` file). For learning purposes, <u>I'm explicitly committing this file to the repository</u>. If you want to store real secrets using this repository as base, please take this into consideration.




-----

To access the UI, just type in the terminal:
```bash
docker-compose -f customized-container/docker-compose.yml exec notebooks mlflow ui --host=0.0.0.0 --backend-store-uri /src/code
```
then go to `http://127.0.0.1:5000`
