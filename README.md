# myblog

ð
_[English](/docs/README-en.md) â [ç®ä½ä¸­æ](README.md)_

## ä¸»è¦åè½ï¼

- æç« ï¼é¡µé¢ï¼åç±»ç®å½ï¼æ ç­¾çæ·»å ï¼å é¤ï¼ç¼è¾ç­ãæç« ãè¯è®ºåé¡µé¢æ¯æ`Markdown`ï¼æ¯æä»£ç é«äº®ã
- æ¯ææç« å¨ææç´¢ã
- å®æ´çè¯è®ºåè½ï¼åæ¬åè¡¨åå¤è¯è®ºï¼ä»¥åè¯è®ºçé®ä»¶æéï¼æ¯æ`Markdown`ã
- ä¾§è¾¹æ åè½ï¼ææ°æç« ï¼æå¤éè¯»ï¼æ ç­¾äºç­ã
- æ¯æ Oauth ç»éï¼ç°å·²æ Google,GitHub,facebook,å¾®å,QQ ç»å½ã
- æ¯æ`Redis`ç¼å­ï¼æ¯æç¼å­èªå¨å·æ°ã
- ç®åç SEO åè½ï¼æ°å»ºæç« ç­ä¼èªå¨éç¥ Google åç¾åº¦ã
- éæäºç®åçå¾åºåè½ã
- éæ`django-compressor`ï¼èªå¨åç¼©`css`ï¼`js`ã
- ç½ç«å¼å¸¸é®ä»¶æéï¼è¥ææªææå°çå¼å¸¸ä¼èªå¨åéæéé®ä»¶ã
- éæäºå¾®ä¿¡å¬ä¼å·åè½ï¼ç°å¨å¯ä»¥ä½¿ç¨å¾®ä¿¡å¬ä¼å·æ¥ç®¡çä½ ç vps äºã

## å®è£

mysql å®¢æ·ç«¯ä»`pymysql`ä¿®æ¹æäº`mysqlclient`ï¼å·ä½è¯·åè [pypi](https://pypi.org/project/mysqlclient/) æ¥çå®è£åçåå¤ã

ä½¿ç¨ pip å®è£ï¼ `pip install -Ur requirements.txt`

å¦æä½ æ²¡æ pipï¼ä½¿ç¨å¦ä¸æ¹å¼å®è£ï¼

- OS X / Linux çµèï¼ç»ç«¯ä¸æ§è¡:

  ```
  curl http://peak.telecommunity.com/dist/ez_setup.py | python
  curl https://bootstrap.pypa.io/get-pip.py | python
  ```

- Windows çµèï¼

  ä¸è½½ http://peak.telecommunity.com/dist/ez_setup.py å https://raw.github.com/pypa/pip/master/contrib/get-pip.py è¿ä¸¤ä¸ªæä»¶ï¼åå»è¿è¡ã

## è¿è¡

ä¿®æ¹`myblog/setting.py` ä¿®æ¹æ°æ®åºéç½®ï¼å¦ä¸æç¤ºï¼

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'myblog',
        'USER': 'root',
        'PASSWORD': '1234',
        'HOST': 'host',
        'PORT': 3306,
    }
}
```

### åå»ºæ°æ®åº

mysql æ°æ®åºä¸­æ§è¡:

```sql
CREATE DATABASE `myblog` /*!40100 DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci */;
```

ç¶åç»ç«¯ä¸æ§è¡:

```bash
python manage.py makemigrations
python manage.py migrate
```

### åå»ºè¶çº§ç¨æ·

ç»ç«¯ä¸æ§è¡:

```bash
python manage.py createsuperuser
```

### åå»ºæµè¯æ°æ®

ç»ç«¯ä¸æ§è¡:

```bash
python manage.py create_testdata
```

### æ¶ééææä»¶

ç»ç«¯ä¸æ§è¡:

```bash
python manage.py collectstatic --noinput
python manage.py compress --force
```

### å¼å§è¿è¡ï¼

æ§è¡ï¼ `python manage.py runserver`

æµè§å¨æå¼: http://127.0.0.1:8000/ å°±å¯ä»¥çå°ææäºã

æ¬é¡¹ç®å·²ç»æ¯æä½¿ç¨ docker æ¥é¨ç½²ï¼å¦æä½ æ docker ç¯å¢é£ä¹å¯ä»¥ä½¿ç¨ docker æ¥é¨ç½²ï¼å·ä½è¯·åè:[docker é¨ç½²](/docs/docker.md)

## æ´å¤éç½®:

[æ´å¤éç½®ä»ç»](/docs/config.md)  
[éæ elasticsearch](/docs/es.md)
