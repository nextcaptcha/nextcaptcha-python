# NextCaptcha Python SDK
NextCaptcha - это мощный сервис для решения капч, который поддерживает различные типы капч, включая reCAPTCHA v2,
reCAPTCHA v2 Enterprise, reCAPTCHA v3, reCAPTCHA Mobile, hCaptcha и FunCaptcha. С помощью NextCaptcha вы сможете легко
решать различные проблемы с капчей в своих скриптах и программах автоматизации.

Этот SDK предоставляет простой и удобный Python-интерфейс для взаимодействия с API NextCaptcha. Он поддерживает все
все доступные типы капч и предлагает интуитивно понятные методы решения различных типов капч.

## Установка

Вы можете установить NextCaptcha Python SDK с помощью pip:

```shell
pip install nextcaptcha-python
```

## Использование

Чтобы начать использовать NextCaptcha Python SDK, вам сначала нужно получить свой API-ключ (clientKey) на 
[NextCaptcha](https://dashboard.nextcaptcha.com) Dashboard. Затем вы можете создать экземпляр NextCaptchaAPI:

```python
from nextcaptcha import NextCaptchaAPI

api = NextCaptchaAPI(client_key="YOUR_CLIENT_KEY")
```

Теперь вы можете использовать объект api для решения различных типов капч.
Для решения задач reCAPTCHA v2 используйте метод recaptchav2:

```python
result = api.recaptchav2(website_url="https://example.com", website_key="SITE_KEY")
```

Решение reCAPTCHA v2 Enterprise
Чтобы решить проблемы reCAPTCHA v2 Enterprise, используйте метод recaptchav2enterprise:

```python
result = api.recaptchav2enterprise(website_url="https://example.com", website_key="SITE_KEY")
```

Решение reCAPTCHA v3
Для решения задач reCAPTCHA v3 используйте метод recaptchav3:

```python
result = api.recaptchav3(website_url="https://example.com", website_key="SITE_KEY")
```

Решение reCAPTCHA Mobile
Чтобы решить проблемы reCAPTCHA Mobile, используйте метод recaptcha_mobile:

```python
result = api.recaptcha_mobile(app_key="APP_KEY")
```

Решение проблемы hCaptcha
Чтобы решить проблемы с hCaptcha, используйте метод hcaptcha:

```python
result = api.hcaptcha(website_url="https://example.com", website_key="SITE_KEY")
```

Решение проблем hCaptcha Enterprise
Чтобы решить проблемы hCaptcha Enterprise, используйте метод hcaptcha_enterprise:

```python
result = api.hcaptcha_enterprise(website_url="https://example.com", website_key="SITE_KEY")
```

Решение задач FunCaptcha
Чтобы решить проблемы FunCaptcha, используйте метод funcaptcha:

```python
result = api.funcaptcha(website_public_key="WEBSITE_PUBLIC_KEY")
```

Проверка баланса аккаунта
Чтобы проверить баланс вашего аккаунта NextCaptcha, используйте метод get_balance:

```python
balance = api.get_balance()
print(f "Баланс аккаунта: {баланс}")
```

Вот полный пример использования NextCaptcha Python SDK для решения задачи reCAPTCHA v2:

```python
from nextcaptcha import NextCaptchaAPI

CLIENT_KEY = "YOUR_CLIENT_KEY"
WEBSITE_URL = "https://example.com"
КЛЮЧ_САЙТА = "КЛЮЧ_САЙТА"

api = NextCaptchaAPI(client_key=CLIENT_KEY)
result = api.recaptchav2(website_url=WEBSITE_URL, website_key=WEBSITE_KEY)

if result["status"] == "ready":
    print(f "reCAPTCHA решена: {result['solution']}")
else:
    print(f "Не удалось решить reCAPTCHA: {result['error']}")
```

## Обработка ошибок

Если при решении капчи произошла ошибка, SDK вернет словарь, содержащий информацию об ошибке. Вы можете
проверить поле status, чтобы определить, был ли запрос успешным. Если статус "готов", то капча была
успешно решена, и решение будет представлено в поле solution. Если статус "не удалось", в поле ошибки
будет содержать описание ошибки.

## Вклад

Если вы обнаружили какие-либо ошибки или у вас есть предложения по улучшению, пожалуйста, не стесняйтесь оставить проблему или отправить запрос на исправление. Мы
приветствуем любой вклад!

## Лицензия

Этот проект лицензируется по лицензии MIT. Для получения дополнительной информации, пожалуйста, ознакомьтесь с файлом LICENSE.




Переведено с помощью www.DeepL.com/Translator (бесплатная версия)