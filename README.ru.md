<p align="center">
  <a href="README.md"><img src="https://img.shields.io/badge/lang-English 🇬🇧-blue?style=for-the-badge"></a>
</p>


# Расширение Яндекс Переводчик для PopClip

Расширение PopClip для перевода выделенного текста с помощью Яндекс Переводчика с возможностью выбора исходного и целевого языков.

## Скриншоты

### Окно установки расширения
При копировании сниппета PopClip отображает окно установки.

![PopClip Extension](screenshots/PopClip_Extension1.png)

### Окно настроек
Настройка исходного и целевого языка для перевода.

![Extension Options](screenshots/Extension_Options.png)

### Панель PopClip в действии
Кнопка перевода появляется при выделении текста.

![PopClip Extension](screenshots/PopClip_Extension2.png)

## Возможности

- 🌍 **Поддержка многих языков**: Перевод между 11+ популярными языками
- 🔄 **Автоопределение**: Автоматическое определение исходного языка
- ⚙️ **Настройка**: Выбор исходного и целевого языков
- 🚀 **Быстрый доступ**: Перевод одним кликом из любого выделенного текста
- 🎯 **Нативная интеграция**: Использует URL-схему приложения Яндекс Переводчик

## Поддерживаемые языки

- Русский
- English (Английский)
- Deutsch (Немецкий)
- Français (Французский)
- Español (Испанский)
- Italiano (Итальянский)
- 中文 (Китайский)
- 日本語 (Японский)
- 한국어 (Корейский)
- العربية (Арабский)
- Türkçe (Турецкий)

## Установка

### Способ 1: Установка снипета
1. Скопируйте содержимое файла [`YandexTranslate`](YandexTranslate.popclipext/Config.yaml)
2. Выделите текст и нажмите "Установить расширение" в панели PopClip
3. Настройте предпочитаемые языки в настройках PopClip

### Способ 2: Установка расширения
1. Скачайте расширение [`YandexTranslate.popclipextz`](https://github.com/nikolalek/PopClip-Extensions-for-Yandex-Translate-MacOS/raw/refs/heads/main/YandexTranslate.popclipextz)

2. Дважды щёлкните по файлу `YandexTranslate.popclipextz`, чтобы установить его
3. Настройте предпочитаемые языки в настройках PopClip

## Использование

1. Выделите любой текст для перевода
2. Нажмите кнопку "Перевести" в панели PopClip
3. Откроется приложение Яндекс Переводчик с готовым к переводу текстом

## Настройка

Откройте настройки PopClip для изменения:
- **Целевой язык**: Выберите предпочитаемый язык перевода
- **Исходный язык**: Установите исходный язык или используйте автоопределение

## Требования

- macOS 10.15 или новее
- PopClip 2021.11 или новее
- Приложение Яндекс Переводчик

## Разработка

Расширение создано как снипет PopClip с использованием YAML конфигурации. Основные файлы:

- [`YandexTranslate`](YandexTranslate.popclipext/Config.yaml) - Основной код расширения
```yaml
#popclip
name:
  en: Yandex Translate
  ru: Яндекс Переводчик
  de: Yandex Übersetzer
  fr: Yandex Traducteur
  es: Yandex Traductor
  it: Yandex Traduttore
  zh: Yandex 翻译
  ja: Yandex 翻訳
  ko: Yandex 번역
  ar: ياندكس الترجمة
  tr: Yandex Çeviri
identifier: ru.nikolalek.extension.yandex.translate
icon: iconify:material-symbols:translate-rounded
# @version 1.0.1
# @author nikolalek
# @license MIT
# @see https://apps.apple.com/app/yandex-translate/id584291439
description:
  en: "Translate selected text in Yandex Translate app"
  ru: "Перевод выделенного текста в приложении Яндекс Переводчик"
  de: "Übersetzen Sie markierten Text in der Yandex Übersetzer-App"
  fr: "Traduire le texte sélectionné dans l'application Yandex Traducteur"
  es: "Traducir el texto seleccionado en la aplicación Yandex Traductor"
  it: "Traduci il testo selezionato nell'app Yandex Traduttore"
  zh: "在 Yandex 翻译应用中翻译选定的文本"
  ja: "選択したテキストをYandex翻訳アプリで翻訳"
  ko: "Yandex 번역 앱에서 선택한 텍스트 번역"
  ar: "ترجمة النص المحدد في تطبيق ياندكس الترجمة"
  tr: "Seçili metni Yandex Çeviri uygulamasında çevirin"
app:
  name: Yandex Translate
  link: https://apps.apple.com/app/yandex-translate/id584291439
  check installed: true
  bundle identifiers:
   - ru.yandex.mobile.translate  
options title:
  en: Translation Settings
  ru: Настройки перевода
  de: Übersetzungseinstellungen
  fr: Paramètres de traduction
  es: Configuración de traducción
  it: Impostazioni di traduzione
  zh: 翻译设置
  ja: 翻訳設定
  ko: 번역 설정
  ar: إعدادات الترجمة
  tr: Çeviri Ayarları
options:
  - identifier: target_language
    type: multiple
    label:
      en: Target Language
      ru: Язык перевода
      de: Zielsprache
      fr: Langue cible
      es: Idioma de destino
      it: Lingua di destinazione
      zh: 目标语言
      ja: 翻訳先言語
      ko: 대상 언어
      ar: اللغة الهدف
      tr: Hedef Dil
    default value: ru
    values: [ru, en, de, fr, es, it, zh, ja, ko, ar, tr]
    value labels:
      - 🇷🇺 Русский
      - 🇬🇧 English
      - 🇩🇪 Deutsch
      - 🇫🇷 Français
      - 🇪🇸 Español
      - 🇮🇹 Italiano
      - 🇨🇳 中文
      - 🇯🇵 日本語
      - 🇰🇷 한국어
      - 🇸🇦 العربية
      - 🇹🇷 Türkçe
actions:
  - title:
      en: Translate
      ru: Перевести
      de: Übersetzen
      fr: Traduire
      es: Traducir
      it: Tradurre
      zh: 翻译
      ja: 翻訳
      ko: 번역
      ar: ترجمة
      tr: Çevir
    requirements: [text]
    url: "yandextranslate://translate?text={popclip text}&from=auto&to={popclip option target_language}"
    clean query: true
```

## Лицензия

Проект лицензирован под лицензией MIT - подробности в файле [LICENSE](LICENSE).

## Благодарности

- [PopClip](https://www.popclip.app) от Pilotmoon Software
- Сервис [Яндекс Переводчик](https://translate.yandex.ru)
- Дизайн иконки вдохновлен брендингом Яндекса

---

**Примечание**: Это неофициальное расширение. Яндекс Переводчик является торговой маркой ООО «Яндекс».
