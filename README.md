# VozduhLaucher

## Установка
Запусти **VozduhLaucher-Setup.exe** — мастер установки поставит лаунчер, добавит ярлык в меню Пуск и на рабочий стол.

**VozduhLaucher.exe** — портативная версия, работает без установки.

## Данные
Всё хранится в `%APPDATA%\VozduhLaucher` (версии, инстансы, Java, конфиг).
У каждой версии — своя папка в `instances\`.

## Требования
Windows 10/11 x64. Java находится автоматически, при отсутствии — скачивается сама (Adoptium).
Окно рендерится через Edge/WebView2 (есть в каждой Windows 10/11) — поэтому лаунчер весит мегабайты и почти не ест RAM.

## Сборка из исходников (VozduhLaucher-source.zip)
```
go build -ldflags "-s -w -H=windowsgui" -o VozduhLaucher.exe .
makensis installer/installer.nsi
```
Ничего выкладывать на GitHub не нужно — лаунчер работает с публичными API (Mojang, Fabric, Forge, NeoForge, Quilt, LiteLoader, Modrinth, Adoptium) напрямую.
