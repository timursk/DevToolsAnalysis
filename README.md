# DevToolsAnalysis

## 1. Network

### 1.1 HAR архив - ![файл](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/startHAR.zip)

<!-- ![Image alt](https://github.com/{username}/{repository}/raw/{branch}/{path}/image.png) -->

### 1.2 Неоптимальные места

1.2.1 Дублирование ресурсов

- Файлы Bootstrap
  ![Bootstrap](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/duplicate/duplicate1.png)
- Файлы cast_sender.js & code.js
  ![code.js](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/duplicate/duplicate2.png)
- Шрифты
  ![font](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/duplicate/duplicate3.png)
  ![font](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/duplicate/duplicate6.png)
- Картинка
  ![image](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/duplicate/duplicate4.png)
- Favicon
  ![favicon](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/duplicate/duplicate5.png)
- JQuery
  ![jquery](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/duplicate/duplicate7.png)
- openapi.js
  ![openapi.js](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/duplicate/duplicate8.png)
- popper.min.js
  ![popper.min.js](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/duplicate/duplicate9.png)

1.2.2 Лишний размер ресурса
  - Размер >100kb, js не разбит на чанки
  ![superfluous](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/superfluous/superfluous.png)

1.2.3 Медленно загружающиеся ресурсы
  - Долгозагружающиеся запросы с ошибками 
  ![slow requests with errors](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/slow/longtime1.png)
  ![slow requests with errors](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/slow/longtime2.png)
  - Запросы >200ms
  ![slow requests](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/slow/longtime3.png)

1.2.4 Ресурсы, блокирующие загрузку
  - Запросы JS
  ![js](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/blocking/blockingrequests1.png)
  - Запросы CSS
  ![css](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/blocking/blockingrequests2.png)
- 
  

  - CORS ошибк
  -   ![COR
  - (https:/github.com/timursk/DevToolsAnalysis/raw/main/Network/addendum/extra1.png)
  ![CORS](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/addendum/extra2.png)
  - Запросы с ошибками
  ![errors](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/addendum/extra3.png)
  - Запросы, возвращающие 302 из-за которого происходит редирект (+1 запрос)
  ![302 redirects](https://github.com/timursk/DevToolsAnalysis/raw/main/Network/addendum/extra4.png)

## 2. Pefrormance

### 2.1  Файл загрузки ![файл](https://github.com/timursk/DevToolsAnalysis/raw/main/Perfrormance/trace)
### 2.2  Dремя в миллисекундах от начала навигации до событий
- First Paint (FP) 393.4ms 
![fp](https://github.com/timursk/DevToolsAnalysis/raw/main/Perfrormance/FirstPaint.png)
- First Contentful Paint (FCP) 393.4ms
![fcp](https://github.com/timursk/DevToolsAnalysis/raw/main/Perfrormance/FirstContentfulPaint.png)
- Largest Contentful Paint (LCP) 1711.5ms
![lcp](https://github.com/timursk/DevToolsAnalysis/raw/main/Perfrormance/LargestContentfulPaint.png)
- DOM Content Loaded (DCL) 1374.0ms
![dcl](https://github.com/timursk/DevToolsAnalysis/raw/main/Perfrormance/DomContentLoaded.png)
- Load 21154.0ms
![onload](https://github.com/timursk/DevToolsAnalysis/raw/main/Perfrormance/OnLoad.png)

### 2.3  DOM Element на котором происходит LCP
- image
![image](https://github.com/timursk/DevToolsAnalysis/raw/main/Perfrormance/ElementTriggerLCP.png)

### 2.4 Время в миллисекундах на этапы обработки документа
- Loading 44ms
- Scripting 1765ms
- Rendering 784ms
- Painting 81ms
![perf timings](https://github.com/timursk/DevToolsAnalysis/raw/main/Perfrormance/PerfTimings.png)

## 3. Coverage

### 3.1  Файл загрузки 
![файл](https://github.com/timursk/DevToolsAnalysis/raw/main/Coverage/CoverageScreen.png)
### 3.2  Неиспользованный CSS
- 547kb
![файл](https://github.com/timursk/DevToolsAnalysis/raw/main/Coverage/UnusedCSS.png)
### 3.3  Неиспользованный JS
- ~2300kb
![файл](https://github.com/timursk/DevToolsAnalysis/raw/main/Coverage/UnusedJS.png)