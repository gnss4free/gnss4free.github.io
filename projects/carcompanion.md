---
layout: page
title: CarCompanion
---

# 🚗 CarCompanion - GNSS4Free Project

[🇷🇺 Русский](#-карcompanion---проект-gnss4free) | [🇬🇧 English](#-carcompanion---gnss4free-project)

---

## 🇷🇺 CarCompanion - Проект GNSS4Free

### 📱 Описание проекта

**CarCompanion** — это мобильное приложение на базе Android, которое преобразует смартфон в цифрового ассистента (компаньона) для автомобильных информационных систем на базе Android.

### 🎯 Текущая функциональность (Этап 1)

Первый релиз реализует две ключевые функции:

1. **Автоматическая раздача интернета**
   - Активируется при подключении автомобиля через Bluetooth
   - Автоматически включает точку доступа (HotSpot) на телефоне
   - Обеспечивает интернет-соединение для автомобильной информационной системы

2. **Передача геокоординат**
   - Активируется при наличии в сети системы-потребителя (в остальных случаях не тратится энергия на передачу данных "вхолостую")
   - Система-провайдер (как правило, телефон с GNSS-чипом) отправляет геоданные (геолокацию) по локальной сети системам-потребителям (автомобилю)
   - Система-получатель получая данные о геолокации делает их доступными Android-приложениям через функциональность ОС "Приложение для фиктивных положений"

### 📋 Предпосылки проекта

Китайские автомобили для глобального рынка, в особенности для рынка СНГ, часто поставляются без полной функциональности в информационно-развлекательной области (Infotainment). Большинство таких автомобилей лишены:
- **Телематического блока** (подключение к интернету, управление и контроль)
- **Встроенного GPS-модуля** и блока навигации

### 🔧 Почему именно CarCompanion?

На рынке уже существуют подобные решения, однако они имеют те или иные недостатки: они либо устарели, либо имеют сложный в настройке интерфейс, либо требуют внешних систем, автоматизирующих их использование (типа Macrodroid или Tasker). В любом случае, мне было просто интересно разработать систему, используя современные технологии программирования и которая устроила бы лично меня.

### ✨ Ключевые преимущества CarCompanion

#### 1. **Простой и лаконичный интерфейс**
   - Минималистичный дизайн
   - Интуитивно понятная настройка, не требующая вводить IP-адреса, названия сетевых интерфейсов и тому подобного

#### 2. **Надежная логика работы**
   - Использование **FSM** (Finite State Machine — конечный автомат) для управления состоянием приложения
   - Эффективный и предсказуемый алгоритм установления связи "Провайдер ↔ Потребитель"

#### 3. **Максимальная производительность**
   - Эффективный **Бинарный протокол**
   - Минимальная задержка при передаче данных

#### 4. **Не требует вложений**
   - Программа бесплатна для частного использования
   - Не требуется преобретать дополнительные устройства/модули, выполнять аппаратную доработку автомобиля
   - Идеально, чтобы "попробовать"

### 📊 Технические параметры

- **Платформа:** Android (минимальная версия: TBD)
- **Языки программирования:** Java/Kotlin
- **Лицензия:** GNU General Public License v3.0
- **Статус:** Активная разрабо��ка
- **Репозиторий:** https://github.com/gnss4free/CarCompanion

### 🚀 Roadmap

- [x] Этап 1: Базовая функциональность (GNSS + интернет)
- [ ] Этап 2: Расширенные функции (OBD-II интеграция, расширенная телеметрия)
- [ ] Этап 3: Веб-интерфейс и облачная синхронизация
- [ ] Этап 4: Поддержка iOS и Web-версий

### 📚 Документация

- [Архитектура проекта](https://github.com/gnss4free/CarCompanion/blob/main/docs/ARCHITECTURE.md)
- [Установка и настройка](https://github.com/gnss4free/CarCompanion/blob/main/docs/INSTALLATION.md)
- [Как контрибьютить](https://github.com/gnss4free/CarCompanion/blob/main/docs/CONTRIBUTING.md)

### 📄 Лицензия

Проект распространяется под лицензией **GNU General Public License v3.0**.

---

## 🇬🇧 CarCompanion - GNSS4Free Project

### 📱 Project Description

**CarCompanion** is an Android mobile application that transforms a smartphone into a digital assistant (companion) for Android-based car information systems.

### 🎯 Current Functionality (Phase 1)

The first release implements two key features:

1. **Automatic Internet Sharing**
   - Triggered upon Bluetooth connection with the vehicle
   - Automatically activates the HotSpot (Wi-Fi access point) on the phone
   - Provides internet connectivity for the car's information system

2. **GNSS Coordinates Broadcasting**
   - Activated only when a consumer system is present in the network (no wasted energy on idle data transmission)
   - Provider system (typically a phone with GNSS chip) sends geolocation data over the local network to consumer systems (vehicle)
   - Consumer system receives geolocation data and makes it available to Android applications through the OS functionality "Mock Location Provider"

### 📋 Project Prerequisites

Chinese vehicles for the global market, particularly for the CIS region, are often shipped without full functionality in the infotainment area. Most such vehicles lack:
- **Telematics module** (internet connectivity, management and control)
- **Built-in GPS module** and navigation unit

### 🔧 Why CarCompanion?

Similar solutions already exist on the market, but they have various drawbacks: they are either outdated, have a complex interface to configure, or require external systems to automate their use (such as Macrodroid or Tasker). In any case, I found it simply interesting to develop a system using modern programming technologies and one that would suit me personally.

### ✨ Key Advantages of CarCompanion

#### 1. **Simple and Concise Interface**
   - Minimalist design
   - Intuitive setup that doesn't require entering IP addresses, network interface names, and the like

#### 2. **Reliable Operation Logic**
   - Uses **FSM** (Finite State Machine) for managing application state
   - Efficient and predictable algorithm for establishing "Provider ↔ Consumer" connection

#### 3. **Maximum Performance**
   - Efficient **Binary protocol**
   - Minimal latency in data transmission

#### 4. **No Investment Required**
   - The application is free for personal use
   - No need to purchase additional devices/modules or perform hardware modifications to the vehicle
   - Perfect for "trying it out"

### 📊 Technical Parameters

- **Platform:** Android (minimum version: TBD)
- **Programming Languages:** Java/Kotlin
- **License:** GNU General Public License v3.0
- **Status:** Active Development
- **Repository:** https://github.com/gnss4free/CarCompanion

### 🚀 Roadmap

- [x] Phase 1: Basic functionality (GNSS + Internet sharing)
- [ ] Phase 2: Advanced features (OBD-II integration, extended telemetry)
- [ ] Phase 3: Web interface and cloud synchronization
- [ ] Phase 4: iOS and Web version support

### 📚 Documentation

- [Project Architecture](https://github.com/gnss4free/CarCompanion/blob/main/docs/ARCHITECTURE.md)
- [Installation and Setup](https://github.com/gnss4free/CarCompanion/blob/main/docs/INSTALLATION.md)
- [Contributing Guide](https://github.com/gnss4free/CarCompanion/blob/main/docs/CONTRIBUTING.md)

### 📄 License

The project is distributed under the **GNU General Public License v3.0**.

---

[← Back to Projects](index.md)
