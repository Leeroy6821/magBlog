---
title: Налаштування Git
date: 2020-03-17 13:59:00
---
Ми будемо використовувати Git для нашої системи керування версіями, тому ми збираємося налаштувати її так, щоб вона відповідала нашому обліковому запису Github. Якщо ви ще не маєте облікового запису Github, не забудьте зареєструватися.

Замініть ім'я та адресу електронної пошти на наступні кроки на ті, які ви використовували для свого облікового запису Github.

```bash
$ git config --global color.ui true
$ git config --global user.name "YOUR NAME"
$ git config --global user.email "YOUR@EMAIL.com"
$ ssh-keygen -t rsa -b 4096 -C "YOUR@EMAIL.com"
```

Наступним кроком є ​​прийняття новоствореного ключа SSH та додавання його до вашого облікового запису Github. Скопіюйте вивід наступної команди.

```bash
$ cat ~/.ssh/id_rsa.pub
```

Перейдіть на Github і вставте вміст тут.

Після цього ви можете перевірити, чи він працює:

```bash
$ ssh -T git@github.com
```

Ви повинні отримати таке повідомлення:

```bash
Hi your_name! You''ve successfully authenticated, but GitHub does not provide shell access.
```

Якщо сталася помилка і ви не можете отримати доступ по ssh, перевірте віддалені підключення.

```bash
$ git remote -v # View current remotes
```

Встановіть нові віддалені репозиторії.

### Git репозиторій

Ініціалізуємо git папці з сайтом progter-hexo:

```bash
$ git init
```

Переглянемо git status:

```bash
$ git status
```

Додаємо всі файли в git:

```bash
$ git add --all
```

Робимо коміт:

```bash
$ git commit -m "Create My Site"
```

```bash
Переглянемо git status: $ git status
```

Якщо все додано правильно то має повернутися:

```bash
$ nothing to commit, working tree clean
```
