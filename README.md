# shri_homework_dev_tools

## Network

### HAR
* [профиль загрузки ресурсов в HAR](lifehacker.ru.har)

### дублирование ресурсов
* > файл `publishertag.js` грузится 2 раза
  > ![publishertag.js](imgs/publishertag.png)
* > подключение Google Tag Manager с разным id выглядит странно..
  > ![Google Tag Manager](imgs/google_tag_manager.png)
* > рекламные скрипты подгружаются дважды
  > ![ads duplicate](imgs/ads_duplicate.png)

### лишний размер ресурса
* > шрифты грузятся для многих языков сразу, хотя на странице вряд ли они используются все. Также одновременно для шрифтов грузится расширенная версия и обычная(например, `cyrillic-ext` и `cyrillic`).
  > ![fonts ext](imgs/fonts_ext_dup.png)

### медленно загружающиеся ресурсы
* > большие изображения, размер которых точно можно соптимизировать
  > ![big images](imgs/big_images.png)

### ресурсы, блокирующие загрузку
* > 60 ресурс блокирует загрузку
  > ![60 resourse blocking](imgs/60_resourse_blocking.png)
  >
  > при чём некоторые из этих ресурсов совсем необязательные для загрузки в `head` – например скрипты для аналитики обычно подключаются в конце `body`, чтобы не блокировать загрузку страницы
  > ![analytics in head](imgs/analytics_in_head.png)

### дополнительно
* [в google-шрифтах не используется font-display](https://scotch.io/bar-talk/google-fonts-now-supports-font-display#toc-how-do-i-use-font-display-with-google-fonts-)
* > какие-то 2 запроса были отклонены
  > ![canceled](imgs/canceled.png)
* > много закомментированного кода, например в `index.html`:
  > ![commented code](imgs/commented_code.png)

---

## Performance

### профиль загрузки страницы
* [файл профиля загрузки страницы](Profile-20200322T231809.json)

### время в миллисекундах от начала навигации до:
* First Paint: 3806.7 ms
* First Meaningful Paint: 3806.7 ms
* DOM Content Loaded: 4260.4 ms
* Load: 10846.5 ms

### время в миллисекундах на разные этапы обработки документа:
* Loading: 89 ms
* Scripting: 3539 ms
* Rendering: 889 ms
* Painting: 66 ms

---

## Coverage

### скриншот вкладки после загрузки страницы
![coverage1](imgs/coverage1.png)
![coverage2](imgs/coverage2.png)

### объём неиспользованного CSS:
* 391 KB unused

### объём неиспользованного JS:
* 2.3 MB unused