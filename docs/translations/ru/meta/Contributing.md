---
title: Внесение вклада
description: Как внести вклад в Wiki SA-MP и документацию open.mp.
---

Этот источник документации открыт для внесений любымх зменений. Всё, что вам нужно, это аккаунт [GitHub](https://github.com) и сводобное время. Вам даже не нужно знать Git, вы можете всё сделать через веб интерфейс!

Если вы хотите помочь с поддержкой определённого языка, откройте документ [`CODEOWNERS`](https://github.com/openmultiplayer/wiki/tree/master/CODEOWNERS) и добавьте по примеру строку с директорией с переводами вместе с вашим именем пользователя.


## Редактирование контента

На каждой странице есть кнопка, которая переносит вас на страницу с редактированием:

![Кнопка редактирования находится на каждой странице](/images/contributing/edit-this-page.png)

Например, клик по [SetVehicleAngularVelocity](../scripting/functions/SetVehicleAngularVelocity) перенесёт вас на [эту страницу](https://github.com/openmultiplayer/wiki/edit/master/docs/scripting/functions/SetVehicleAngularVelocity.md), которая встретит вас с текстовым редактором для редактирования содержимого (если вы уже вошли в аккаунт GitHub, конечно же).

Сделайте ваши правки и подветрдите "Pull Request" (запрос на слияние), это означает, что руководитель Wiki и другие члены сообщества смогут увидеть ваши изменения, обсудить, что требуется добавить и/или исправить и уже после внести изменения в основной репозиторий.


## Добавление нового контента

Добавление нового контента немного сложнее. Вы можете сделать это двумя способами:

### Сайт GitHub

Когда вы просматриваете дерикторию на сайте GitHub, вы можете заметить кнопку "Добавить файл" в правом верхнем углу списка файлов:

![Кнопка добавить файл](/images/contributing/add-new-file.png)

Вы можете либо загрузить уже написанный файл Markdown, либо записать его непосредственно в текстовом редакторе GitHub.

Файл _обязан_ иметь расширение `.md` и содержать в себе разметку на языке Markdown. Для большей информации о Markdown, прочтите [данную статью](https://guides.github.com/features/mastering-markdown/).

Как только всё сделано, нажмите "Предложить новый файл" и будет открыт новый запрос на слияние (Pull requeest).

### Git

Если вы хотите использовать Git, всё, что вам необходимо - это клонировать репозиторий с Wiki:

```sh
git clone https://github.com/openmultiplayer/wiki.git
```

Откройте это в вашем любимом текстовом редакторе. Я рекомендую Visual Studio Code, поскольку он имеет некоторые полезные средства для форматирования файлов Markdown. Как можно увидеть, я пишу это, используя Visual Studio Code!

![Visual Studio Code](/images/contributing/vscode.png)

Я рекомендую 2 расширения, которые упростят ваше работу:

- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) от David Anson - это расширение, которое гарантирует, что ваш Markdown отформатирован правильно. Это предотвращает некоторые синтаксические и семантические ошибки. Не все предупреждения важны, но некоторые могут помочь улучшить читаемость. Используйте лучшее решение, а если вы сомневаетесь, просто спросите проверяющего!

- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) от Prettier.js Team - это форматер, который автоматически отформатирует ваши файлы Markdown, чтобы все они использовали согласованный стиль. Репозиторий Wiki имеет некоторые настройки в своем "package.json", которые расширение должно автоматически использовать. Обязательно включите "формат при сохранении" в настройках редактора, чтобы ваши файлы Markdown автоматически форматировались при каждом сохранении!

## Замечания, Подсказки и Соглашения

### Внутренние ссылки

Не используйте абсолютные пути на внутренние ссылки сайта. Используйте относительные пути.

- ❌

  ```md
  Используется с [OnPlayerClickPlayer](https://www.open.mp/docs/scripting/callbacks/OnPlayerClickPlayer)
  ```

- ✔

  ```md
  Используется с [OnPlayerClickPlayer](../callbacks/OnPlayerClickPlayer)
  ```

`../` означаетс "подняться на дерикторию выше", так что если вы редактируете файл в папке `functions` и ссылаетесь на папку `callbacks`, вам следует использовать `../` чтобы вернуться в папку `scripting/`, а затем `callbacks/` чтобы перейти в папку `calbacks`, а затем имя файла (без `.md`), на который вы хотите сослаться.

### Изображения

Изображения помещаются в папку `/static/images`. Затем, когда вы хотите использовать изображение через `![]()`, вам просто следует использовать `/images/`, как базовый путь (не нужно указывать `static` это просто для репозитория).

Если вы сомневаетесь, прочтите другую страницу, на которой используются изображения, и скопируйте, как сделано там.

### Метаданные

Первой вещью в _любом_ документе должны быть метаданные:

```mdx
---
title: Мой документация
description: Эта страница о различных штуках, вещах и бургерах, воу!
---
```

Каждая страница должна содержать заголовок и описание.

Для полного списка контента, который может содержаться между `---`, прочтите [документацию Docusaurus](https://v2.docusaurus.io/docs/markdown-features#markdown-headers).

### Заголовки

Не создавайте заголовки первого уровня (`<h1>`) с использованием `#`, поскольку они создаются автоматически. Ващи заголовки _всегда_ должны быть `##`

- ❌

  ```md
  # Мой заголовок

  Это документация для ...

  # Подзаголовок
  ```

- ✔

  ```md
  Эта документация для ...

  ## Подзаголовок
  ```

### Используйте сниппет `Code`, для технической документации

Когда вы пишете текст, содержаший имена функций, цифры, выражения или что-либо ещё, не относящееся к стандартной письменной речи, выделяйте их с помощью \`апострофоф\`, как здесь. Это позволяет упростить отделение обычной письменной речи от технической документации - имен функций и фрагментов кода.


- ❌

  > Функция fopen возвращает значение с тегом File:, не будет проблем на этой строке, если переменная, в которую записывается значение, тоже имеет тег File: (обратите внимание, что регистр символов должен быть одинаковым). Однако, в следующей строке значение 4 добавляется к дескриптору файла. 4 не имеет тега [...]

- ✔

  > Функция `fopen` возвращает значение с тегом `File:`, не будет проблем на этой строке, если переменная, в которую записывается значение, тоже имеет тег `File:` (обратите внимание, что регистр символов должен быть одинаковым). Однако, в следующей строке значение 4 добавляется к дескриптору файла. `4` не имеет тега [...]


В примере выше, `fopen` это имя функции, не английское слово, поэтому следует его ограничить сниппетом `code`, чтобы помочь выделить его на фоне остального контента.

Так же, если текст отсылается на блок демонстративного кода, это поможет читателю соотнести описание и остальной текст с самим примером в виде кода.

### Таблицы

Если у таблицы есть заголовок, он помещается в верхнюю часть:

- ❌

  ```md
  |         |                                      |
  | ------- | ------------------------------------ |
  | Здоровье| Статус двигателя                     |
  | 650     | Не повреждён                         |
  | 650-550 | Белый дым                            |
  | 550-390 | Серый дым                            |
  | 390-250 | Чёрный дым                           |
  | < 250   | Горит (взорвётся очень скоро)        |
  ```

- ✔

  ```md
  | Здоровье| Статус двигателя                     |
  | ------- | ------------------------------------ |
  | 650     | Не повреждён                         |
  | 650-550 | Белый дым                            |
  | 550-390 | Серый дым                            |
  | 390-250 | Чёрный дым                           |
  | < 250   | Горит (взорвётся очень скоро)        |
  ```

## Миграция из SA-MP Wiki

Множество контента было перемещено, но если вы заметили, что какая-либо страница отсуствует, то вот краткий гайд по преобразованию контента в формат Markdown.

### Получение HTML кода

1. Нажмите на кнопку

   (Firefox)

   ![image](/images/contributing/04f024579f8d.png)

   (Chrome)

   ![image](/images/contributing/f62bb8112543.png)

2. Наведите курсор на крайний левый угол главной страницы Wiki, пока не выделится тег `#content`

   ![image](/images/contributing/65761ffbc429.png)

   Или найдите `<div id=content>`

   ![image](/images/contributing/77befe2749fd.png)

3. Скопируйте внутренний HTML код

   ![image](/images/contributing/8c7c75cfabad.png)

   Сейчас у вас есть _только_ HTML код оригинального _содержимого_ страницы, то, что нас волнует, и вы можете преобразовать это в Markdown.

### Преобразование из HTML в Markdown

Для преобразования обычного HTML (без таблиц) в Markdown используйте:

https://domchristie.github.io/turndown/

![image](/images/contributing/77f4ea555bbb.png)

^^ Заметьте, что таблица теперь испорчена окончательно...

### Таблицы HTML в таблицы Markdown

Поскольку верхний инструмент не поддерживает работу с таблицами, используйте данный вариант:

https://jmalarcon.github.io/markdowntables/

И скопируйте только элемент `<table>`:

![image](/images/contributing/57f171ae0da7.png)

### Очистка

Преобразование, скорее всего, не будет совершенным. Так что вам придется сделать небольшую ручную очистку. Перечисленные выше расширения форматирования должны помочь в этом, но вам все равно придется потратить некоторое время на ручную работу.

Если у вас нет времени, не волнуйтесь! Отправьте незаконченный черновик, и кто-то другой сможет продолжить с того места, где вы остановились!

## Лицензионное соглашение

Все проекты open.mp имеют [Лицензионное Соглашение Участника][https://cla-assistant.io/openmultiplayer/homepage]. В общем, это означает, что вы соглашаетесь позволить нам использовать вашу работу и поместить ее под лицензию с открытым исходным кодом. Когда вы впервые откроете Pull-запрос, бот CLA-Assistant разместит ссылку, по которой вы сможете подписать соглашение.