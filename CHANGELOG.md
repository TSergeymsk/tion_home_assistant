# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
## [1.0.9] - 2024-02-13
### Изменения
  - Поправил код на соответствие новой версии НА, начиная с 2024.2
    (https://developers.home-assistant.io/blog/2024/01/24/climate-climateentityfeatures-expanded)

## [1.0.8] - 2024-02-10
### Изменения
  - Изменение нумерации версий, для соотвествия AwesomeVersion 
  - Обновление манифеста для соответствия требованиям НА 2024.2
  - Исправление ошибки включения TION через сервис обогрева. Переключение на вентилятор было, а скорость не включалась. И бризер оставался выключеным по факту.

## [1.07] - 2024-02-08
### Изменения
#### Исправил баг режима AUTO.
  - После включения режима AUTO отключить режим можно было только через PRESET.
  - Сейчас при установке скорости 1-6 режим AUTO отключается

## [1.06] - 2024-02-04
### Изменения
#### Поменял настройки режима AUTO.
  - Сейчас реально работает по параметру target_co2.
  - Скорость 1-6
  - Забор воздуха с улицы
  - target_co2 = 800 по дефолту. Изменить можно ТОЛЬКО через пресеты, сделал 2 пресета для этого.
####
#### Изменен пресет: 
  - PRESET_AWAY: Режим AUTO, target_c02 = 600, с улицы, скорость 1-6, обогреватель выключен
####
#### Добавлен пресет:
  - PRESET_ECO:  Режим AUTO, target_c02 = 700, с улицы, скорость 1-4, обогреватель выключен
####
#### Пресеты без изменения:
    PRESET_SLEEP:    с улицы,     скорость 1, обогреватель выключен
    PRESET_ACTIVITY: с улицы,     скорость 2, обогреватель выключен
    PRESET_BOOST:    с улицы,     скорость 6, обогреватель выключен
    PRESET_HOME:     из квартиры, скорость 2, обогреватель выключен           
    PRESET_COMFORT:  смешанный,   скорость 3, обогреватель выключен 

## [1.05] - 2024-01-24
### Изменения
#### Поменял управление потоком воздуха. 
  Сейчас управления потоком сделано через свойство SWING (Режим качания). 
     SWING_VERTICAL = воздух из квартиры
     SWING_BOTH = смешанный
     SWING_HORIZONTAL = воздух с улицы
####
#### Переделал все пресеты на более нормальные, которые как-то соответствуют названию:
    PRESET_SLEEP:    с улицы,     скорость 1, обогреватель выключен
    PRESET_ACTIVITY: с улицы,     скорость 2, обогреватель выключен
    PRESET_BOOST:    с улицы,     скорость 6, обогреватель выключен
    PRESET_HOME:     из квартиры, скорость 2, обогреватель выключен           
    PRESET_COMFORT:  смешанный,   скорость 3, обогреватель выключен 
    PRESET_AWAY:     с улицы,     скорость 1, обогреватель выключен


## [1.03] - 2022-11-10
### Added
- библиотека Tion обновлена до 1.28. Исправлена работа 4S с нагревателем

## [1.02] - 2022-11-10
### Added
- библиотека Tion обновлена до 1.27

## [1.01] - 2022-11-10
### Added
- добавлена поддержка HVAC_MODE_OFF, версия библиотеки tion обновлена до 1.26
