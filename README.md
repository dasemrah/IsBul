# İsBul
Django-Web iş bulma ve ilan yayınlama platformu

Özellikler :
1) İlan yayınlama
2) İş ilanları bulma
3) Özgeçmiş yükleme
4) Google yöntemi ile kayıt ve oturum açma
5) İlanları kaydet
6) Özelliklerine göre iş ilanı önerisi
7) Tercihe göre filtreleme
8) Yönetici ve iş arayan tarafında e posta ile kayıt ve oturum açma 
9) Şifre sıfırlama
## Setup

After cloning the github repo, run the following command in the application root directory:
```
pip install requirements.txt
```

Create the DB tables:
```
python manage.py migration
python manage.py migrate
```
##Runnig the application
```
cd findjob
python manage.py runserver
```
then open on
http://127.0.0.1:8000/ || http://localhost:8000/

The application comes with sqlite database. Follow below steps to use application with postgresql:
```
#open to the findjob/findjob/settings.py
#remove comment line to 96-105. lines and add above code 
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'findjob',
        'USER': 'postgres',
        'PASSWORD': 'isbul2525',
        'HOST': 'localhost',
    }
}
#after add comment line 90-95. lines same file
#The application used to postgresql min version 11

```
