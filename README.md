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

## Настройки
- Trackpad
  - Tap to click
  - Tracking speed: 7 of 9
  - Click: Light
  - Silent click
  - Gestures:
    - Swipe between pages: no
- General
   - prefer tabs: always 
   - close windows when quitting an app: no
   - allow handoff: no
- Dock
   - size: small
   - position: right
   - autohide dock: yes
   - show recent in dock: no
- Mission control
   - auto arrange spaces: no
- AppleID
 - ICloud: disable all other iCloud items except FindMyMac
- Security
  - Firewall (автоматом ничё не делать)
  - general: require pass immediately
- Sound
   - startup sound: no
   - interface sounds: no
   - alert на 1/4 громкости

## Keyboard setup

### Install karabiner-elements
  - https://karabiner-elements.pqrs.org/
  - Проверить, что разрешения есть у karabiner-grabber и karabiner-observer

### Karabiner simple modifications
- caps -> left ctrl
- escape -> fn
- fn -> escape
- left control -> escape
- right option -> caps lock

### Karabiner complex modifications
- right cmd + hjkl -> arrows

### Set up mac keyboard preferences

### Keyboard
- Key repeat: fastest
- Delay until repeat: shortest

### Preferences
- Отключить все автозамены вообще

### Shortcuts
- switch languages -> cmd space
- finder search -> f6
- Ctrl + 1..10 -> go to workspace N (1-10) (create 10 workspaces) 

### Раскладка
- Первая - стандартная английская, вторая - русская (ПК)

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

## Установили
- Word, Excel, PowerPoint
- Slack
- Numbers, Pages, Keynote, iMovie, GarageBand
- Telegram
- Skype
- Transmission

## Настройка почты


## Разработочка

- [JetBrains Mono](https://www.jetbrains.com/lp/mono/)
- `xcode-select --install` чтобы работал Git

- [VSCode](https://code.visualstudio.com/#alt-downloads) (Выбрать версию для Apple Silicon)
   - синхронизация настроек - логин через GitHub
   - логин в LiveShare - логин через GitHub
   - Включиить алиас `code`: CmdShifftP -> Install code command in path
   - `defaults write com.microsoft.VSCode ApplePressAndHoldEnabled -bool false` - для повторных нажатий клавиш



## После каждого обновления системы (когда отваливается Git)

- `xcode-select --install` Xcode, похоже, делали пидоры.

