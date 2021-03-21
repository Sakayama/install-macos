# install-macos

## Чтобы переустановить macOS
- Нужно выключить, а затем включать, удерживая кнопку включения

## Установка macOS

- WiFi подключили сразу
- Пропускаем Ассистента миграции
- Входим в Apple ID
- Cвязка ключей iCloud: не использовать
- Локатор
- Экспресс-настройка -> Настроить параметры -> 
  - Включить службы геолокации на этом Mac: Да
  - Предоставлять данные для аналитики: нет
- Экранное время: настроить позже
- Siri : Выкл
- FileVault: включаем шифрование и разрешаем разблокировку через iCloud
- TouchID: Настраиваем.
- Apple Pay: настроить позже
- Тема оформления: светлая
- True Tone: Продолжить

## После загрузки и появления рабочего стола
- Скачиваем Chrome
- Логинимся на гитхабе и корректируем инструкцию (по мере использования)

## Chrome setup:

- восстановить закладки
- убрать ярлык Apps
- отключить запросы на уведомления (конфиденциальность -> настройки сайтов -> уведомления-> сайты могут запрашивать: нет)
- on startup: continue where left off
- extensions:
   - adblock plus (and set up)
   - blank new tab
- manage extensions: adblock -> allow incognito
- disable mail hotkeys
```sh
defaults write com.google.Chrome NSUserKeyEquivalents -dict-add 'Email Page Location' '\0'
defaults write com.google.Chrome.canary NSUserKeyEquivalents -dict-add 'Email Page Location' '\0'
defaults write com.apple.Safari NSUserKeyEquivalents -dict-add 'Email Link to This Page' '\0' 'Email This Page' '\0'
defaults write com.google.Chrome NSUserKeyEquivalents -dict-add 'Email Page Location' '\0'
killall cfprefsd
killall Finder
```
