# DevToolsAnalysis

## 1. Network

### 1.1 HAR архив - [файл](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/startHAR.zip)

### 1.2 Неоптимальные места

1.2.1 Дублирование ресурсов

- Файлы Bootstrap <br>
  ![Bootstrap](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/duplicate/duplicate1.png)
- Файлы cast_sender.js & code.js <br>
  ![code.js](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/duplicate/duplicate2.png)
- Шрифты <br>
  ![font](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/duplicate/duplicate3.png)
  ![font](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/duplicate/duplicate6.png)
- Картинка <br>
  ![image](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/duplicate/duplicate4.png)
- Favicon <br>
  ![favicon](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/duplicate/duplicate5.png)
- JQuery <br>
  ![jquery](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/duplicate/duplicate7.png)
- openapi.js <br>
  ![openapi.js](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/duplicate/duplicate8.png)
- popper.min.js <br>
  ![popper.min.js](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/duplicate/duplicate9.png)

1.2.2 Лишний размер ресурса
  - Размер >100kb, js не разбит на чанки <br>
  ![superfluous](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/superfluous/superfluous.png)

1.2.3 Медленно загружающиеся ресурсы
  - Долгозагружающиеся запросы с ошибками <br>
  ![slow requests with errors](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/slow/longtime1.png)
  ![slow requests with errors](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/slow/longtime2.png)
  - Запросы >200ms <br>
  ![slow requests](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/slow/longtime3.png)

1.2.4 Ресурсы, блокирующие загрузку
  - Запросы JS <br>
  ![js](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/blocking/blockingrequest1.png)
  - Запросы CSS <br>
  ![css](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/blocking/blockingrequest2.png)

1.2.5 Дополнительно
  - CORS ошибки <br>
  ![CORS](https:/github.com/timursk/DevToolsAnalysis/raw/main/Network/addendum/extra1.png)
  ![CORS](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/addendum/extra2.png)
  - Запросы с ошибками <br>
  ![errors](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/addendum/extra3.png)
  - Запросы, возвращающие 302 из-за которого происходит редирект (+1 запрос) <br>
  ![302 redirects](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/addendum/extra4.png)

## 2. Pefrormance

### 2.1  Файл загрузки [файл](https://github.com/timursk/DevToolsAnalysis/raw/main/Performance/trace.json)
### 2.2  Dремя в миллисекундах от начала навигации до событий
- First Paint (FP) 393.4ms <br>
![fp](https://github.com/timursk/DevToolsAnalysis/raw/main/Performance/FirstPaint.png)
- First Contentful Paint (FCP) 393.4ms <br>
![fcp](https://github.com/timursk/DevToolsAnalysis/raw/main/Performance/FirstContentfulPaint.png)
- Largest Contentful Paint (LCP) 1711.5ms <br>
![lcp](https://github.com/timursk/DevToolsAnalysis/raw/main/Performance/LargestContentfulPaint.png)
- DOM Content Loaded (DCL) 1374.0ms <br>
![dcl](https://github.com/timursk/DevToolsAnalysis/raw/main/Performance/DomContentLoaded.png)
- Load 21154.0ms <br>
![onload](https://github.com/timursk/DevToolsAnalysis/raw/main/Performance/OnLoad.png)

### 2.3  DOM Element на котором происходит LCP
- image <br>
![image](https://github.com/timursk/DevToolsAnalysis/raw/main/Performance/ElementTriggerLCP.png)

### 2.4 Время в миллисекундах на этапы обработки документа
- Loading 44ms
- Scripting 1765ms
- Rendering 784ms
- Painting 81ms <br>
![perf timings](https://github.com/timursk/DevToolsAnalysis/raw/main/Performance/PerfTimings.png)

## 3. Coverage

### 3.1  Файл загрузки <br>
![Coverage](https://github.com/timursk/DevToolsAnalysis/raw/main/Coverage/CoverageScreen.png)
### 3.2  Неиспользованный CSS
- 547kb <br>
![unused css](https://github.com/timursk/DevToolsAnalysis/raw/main/Coverage/UnusedCSS.png)
### 3.3  Неиспользованный JS
- ~2300kb <br>
![unused js](https://github.com/timursk/DevToolsAnalysis/raw/main/Coverage/UnusedJS.png)