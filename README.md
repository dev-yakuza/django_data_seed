## document
- [django_data 설명](#django_data-설명)
- [django_data説明](#django_data説明)
- [how to use django_data](#how-to-use-django_data)

## django_data 설명
django_data는 장고(django)에서 마스터 데이터 또는 테스트 데이터를 사용하는 방법을 정리한 저장소(Repository)입니다. 이 저장소(Repository)를 제작하면서 작성한 블로그가 있습니다. 자세한 내용은 아래에 링크를 통해 확인하시기 바랍니다.

- [장고(django) 프로젝트에 마스터 데이터 넣기](https://dev-yakuza.github.io/ko/django/data-seed/)

### 사용 방법
아래에 명령어를 통해 django_data 저장소(Repository)를 복사(Clone)합니다.

```bash
git clone https://github.com/dev-yakuza/django_data.git
```

아래에 명령어로 파이썬 가상 환경을 생성합니다.

```bash
virtualenv venv
```

아래에 명령어로 파이썬 가상 환경을 실행합니다.

```bash
source venv/bin/activate
```

아래에 명령어로 프로젝트에 필요한 모듈을 설치합니다.

```bash
pip install -r requirements.txt
```

데이터베이스 연동을 위해 `django_data/settings.py`를 열고 아래의 내용을 자신의 DB에 맞게 수정합니다.

```python
...
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'django_data',  # DB name
        'USER': 'root',  # DB account
        'PASSWORD': '',  # DB account's password
        'HOST': '127.0.0.1',  # DB address(IP)
        'PORT': '3306',  # DB port(normally 3306)
    }
}
...
```

아래에 명령어로 데이터베이스를 생성합니다.

```bash
# python manage.py makemigrations
python manage.py migrate
```

아래에 명령어로 장고(django) 관리자를 생성합니다.

```bash
python manage.py createsuperuser
```

아래에 명령어로 준비한 데이터를 넣습니다.(Data Seed)

```bash
python manage.py loaddata blog/fixtures/posts-data.json
```

아래에 명령어로 테스트서버를 실행합니다.

```bash
python manage.py runserver
```

관리자 페이지를 통해 추가된 데이터를 확인할 수 있습니다.

- 관리자 페이지: [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin)


## django_data説明
django_dataはジャンゴ(django)でマスターデーターやテストデーターを使う方法について纏めたレポジトリ(Repository)です。このレポジトリ(Repository)を作る時作成したブログポストがあります。詳しく内容は下記のリンクを確認してください。

- [ジャンゴ(django)のプロジェクトでマスターデーターを入れる方法](https://dev-yakuza.github.io/django/data-seed/)

### 使い方
下記のコマンドでdjango_exerciseレポジトリ(Repository)をコピー(Clone)します。

```bash
git clone https://github.com/dev-yakuza/django_exercise.git
```

下記のコマンドでパイソン仮想環境を作ります。

```bash
virtualenv venv
```

下記のコマンドでパイソンの仮想環境を実行します。

```bash
source venv/bin/activate
```

下記のコマンドでプロジェクトに必要なモジュールをインストールします。

```bash
pip install -r requirements.txt
```

データベースを連動するため、`django_exercise/settings.py`を開いて下記の内容を自分のDBに合わせて修正します。

```python
...
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'django_exercise',  # DB name
        'USER': 'root',  # DB account
        'PASSWORD': '',  # DB account's password
        'HOST': '127.0.0.1',  # DB address(IP)
        'PORT': '3306',  # DB port(normally 3306)
    }
}
...
```

下記のコマンドでデーターベースを生成します。

```bash
# python manage.py makemigrations
python manage.py migrate
```

下記のコマンドでジャンゴ(django)の管理者を生成します。

```bash
python manage.py createsuperuser
```

下記のコマンドで準備したデーターを入れます。(Data Seed)

```bash
python manage.py loaddata blog/fixtures/posts-data.json
```

下記のコマンドでテストサーバーを起動します。

```bash
python manage.py runserver
```

管理画面で追加されたデーターを確認することができます。

- 管理画面: [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin)

## how to use django_data
django_data is the repository about how to make master data or test data in django. there are blog posts about this repository. if you want to know more details, see the link below.

- [Insert master data to django project](https://dev-yakuza.github.io/en/django/data-seed/)

### How to use
execute the command below to clone the django_exercise repository.

```bash
git clone https://github.com/dev-yakuza/django_exercise.git
```

execute the command below to start python virtual environment.

```bash
virtualenv venv
```

execute the command below to execute python virtual environment.

```bash
source venv/bin/activate
```

execute the command below to install modules for the project.

```bash
pip install -r requirements.txt
```

you need to modify `django_exercise/settings.py` to connect your database like below.

```python
...
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'django_exercise',  # DB name
        'USER': 'root',  # DB account
        'PASSWORD': '',  # DB account's password
        'HOST': '127.0.0.1',  # DB address(IP)
        'PORT': '3306',  # DB port(normally 3306)
    }
}
...
```

execute the command below to migrate.

```bash
# python manage.py makemigrations
python manage.py migrate
```

execute the command below to create django administrator.

```bash
python manage.py createsuperuser
```

execute the command below to insert data. (Data seed)

```bash
python manage.py loaddata blog/fixtures/posts-data.json
```

execute the command below to start django test server.

```bash
python manage.py runserver
```

you can see the data stored well on the administrator page.

- administrator page: [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin)