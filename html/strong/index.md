---
title: "`<strong>`"
description: "Семантически выделяет важный текст."
authors:
  - gingerraccoon
contributors:
  - tatianafokina
keywords:
  - семантическое выделение
  - важность
  - screen reader
  - ридер
  - a11y
related:
  - a11y/role-strong
  - html/b
  - html/i
tags:
  - doka
---

## Кратко

Тег `<strong>` добавляет обёрнутому в него слову или фразе очень высокую важность. Он может использоваться для выделения предупреждений или части документа, которую пользователь должен увидеть раньше остального. При этом обозначение части текста тегом `<strong>` не должно изменять смысла предложения.

## Пример

```html
<p>Эта правка <strong>критически важна</strong> для проекта!</p>
```

<iframe title="Как выглядит" src="demos/view/" height="300"></iframe>

## Как пишется

### `<strong>` против `<b>`

Теги `<strong>` и [`<b>`](/html/b/) внешне похожи: оба по умолчанию имеют стиль [`font-weight: bold`](/css/font-weight/). Но по смыслу эти теги отличаются. Тег `<b>` только внешне выделяет текст, а тег `<strong>` добавляет важности обёрнутому в него тексту.

Не используйте тег `<strong>` только для визуального выделения текста.

### Атрибуты

Тег `<strong>` поддерживает [глобальные атрибуты](/html/global-attrs/) и [события](/js/events/).

### Доступность

Хотя `<strong>` считается элементом семантической вёрстки, у него пока нет встроенной [роли `strong`](/a11y/role-strong/). Так что для [скринридеров](/a11y/screenreaders/) это простой текст, который они никак не выделяют интонацией.

Чтобы магия произошла и скринридер понял, что слово или фраза крайне важные, достаточно стилизовать элемент с помощью `font-weight: bold`. Если у пользователя скринридера включена специальная настройка, он услышит небольшое изменение в озвучивании такого текста.

Несмотря на эту странность, всё равно лучше использовать `<strong>` вместо `<b>`. Так ваша вёрстка будет валидной и в будущем, когда у тега появится встроенная роль `strong`, вам не нужно будет переписывать код.
