# VKbot

## Description
### The bot trained on https://otvet.mail.ru/ and https://ru.stackoverflow.com/ He can answer questions in Russian by VK messages.

### Easy start: 
#### python bot.py  OR  docker build -> docker run
#### To use only bot: comment(#) in "response.py" line "return good_answer(..."
#### To use api: change webadress in "bot.py" and "login.py"
#### To not use api: comment(#) all requests (expect "_get_user_name_from_vk_id")
#### To use Api for DB: change options in "flask_app.py" (and run it on another docker container or web site)
#### To use Model: download files (in zip) from https://yadi.sk/d/2ILoEcx_NHBp-Q/%D0%9C%D0%BE%D0%B4%D0%B5%D0%BB%D1%8C 
#### To use another Model: in "response.py" change "return good_answer(..." to " return urfunction(text)" (return str in utf8)


## Bot Files 
### 1)admin.py
#### File for admins function (such as generate tokens)
### 2)bot.py
#### Main file for connect with VK
### 3)login.py
#### Autification for users and admins 
### 4)response.py
#### Simple answers and call main model 
### 5)tokens.py
#### Tokens generate and validate (for login)
### 6)flask_app.py
#### Api for MySQLDB


## Model files:
### 0)result.py
#### Simple example for use Model function
### 1)test_1.py 
#### Объявление функций (нормализация, векторизация, предсказание класс, annoy, предсказание ответа), импорт обученных моделей (w2v, annoy, вектора)
### 2)true_project.py
#### Объявление функции, в которой осуществляется классификация и находится ответ
### 3)anothers_files_with_data(not upload to github)
### 4)Rabota_s_subtitrami.ipynb
#### Парсинг, обработка, сохранение данных в csv
### 5)my_part.ipynb
#### Нормализация, векторизация, обучение классификатора, annoy, предсказание класса, предсказание ответа, сохранение моделей

## Dockerfiles
### Dockerfile()
#### File to compile in docker
### requirements.txt
#### Requirements for docker
