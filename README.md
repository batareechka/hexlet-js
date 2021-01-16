# hexlet-js
Задание по курсу JS: Настройка окружения<br>
https://ru.hexlet.io/courses/js-setup-environment

## Введение
[Установка Ubuntu на Windows](https://docs.microsoft.com/ru-ru/windows/wsl/install-win10)<br>
[Установка GIT на Windows](https://docs.microsoft.com/ru-ru/windows/wsl/tutorials/wsl-git)<br>
[Менеджер версий языков](https://guides.hexlet.io/version_managers/)

## Установка JavaScript

### Ubuntu или Ubuntu on Windows
```
$ sudo apt-get install curl
$ curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
$ sudo apt install -y nodejs
```

### macOS
```
$ brew install nodejs
```

[Видео о REPL](https://www.youtube.com/watch?v=d4Sadokt_Hg&feature=youtu.be)

## NPM
[package.json](https://docs.npmjs.com/cli/v6/configuring-npm/package-json)<br><br>
Обратите внимание на ключ "type" в JSON. Эту часть нужно добавить самостоятельно, исправив файл. Она нужна для работы системы импортов.

## Зависимости
```js
// Так будет происходить поиск файла lodash.js в текущей директории
import _ from "./lodash";

// Так импортируется код из пакета
import _ from "lodash";
```

```
# Если мы хотим в точности те же версии всех пакетов,
# какие были у остальных разработчиков этого проекта
$ npm ci
```

[Библиотека или свое решение](https://ru.hexlet.io/blog/posts/sovershennyy-kod-biblioteka-ili-svoe-reshenie)<br>
[Отличие npm ci от npm install](https://medium.com/better-programming/npm-ci-vs-npm-install-which-should-you-use-in-your-node-js-projects-51e07cb71e26)

## Зависимости для разработки

### npm install
```
# Вот теперь зависимости из devDependencies устанавливаться не будут
$ npm install --production

# Продакшен режим можно задать и с помощью переменной окружения
$ NODE_ENV=production npm install
```