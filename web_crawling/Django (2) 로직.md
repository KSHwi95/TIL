# **Django Logic**

> 장고는 '프로젝트'라는 단위로 웹 서비스의 전체적인 환경을 관리하고, 'App'이라는 소규모 단위(.py/모듈)를 이용해 프로젝트를 구성하게끔 한다.

## **1. 가상환경 설치, 생성**

```bash
pip3 install virtualenv

virtualenv _____(가상환경명)

.\____\Scripts\activate
```

cmd 앞에 (venv) 가상환경이 실행되면 OK

## **2. Django 설치**

```
pip install django==2.1.7
```

## **3. 프로젝트 만들기**

```
django-admin startproject _____(프로젝트명)
```

> 프로젝트를 만들었다면 프로젝트 디렉토리 '안에서' 장고 서버를 실행할 수 있다.

```
cd ____ (프로젝트명)
```

```bash
#장고 서버 실행
python manage.py runserver
```

## **4. 새로운 APP 만들기**

**APP** <br>
하나의 기능 구현을 위한 모듈

```
django-admin startapp ____
```

## **5. models.py에서 데이터 기본구조 입력**

```python

from django.db import models

# Create your models here.
# 모델 추가

class User(models.Model):
  user_id=models.CharField(max_length=64, verbose_name='사용자 아이디')
  user_email = models.EmailField(max_length=128, verbose_name='사용자 이메일')
  password=models.CharField(max_length=64, verbose_name='비밀번호')
  registered_dttm = models.DateTimeField(auto_now_add=True, verbose_name='등록시간')

  def __str__(self):
    return self.user_id

  #Meta 클래스의 이름은 고정입니다.

  class Meta:
    # db_table 멤버 변수는 고정입니다.
    db_table = "tb_user"

```

## **6. 프로젝트에 App 등록**

프로젝트 폴더에 같은 프로젝트 명을 가진 폴더가 하나 더있고, 그 안에 settings.py가 존재
