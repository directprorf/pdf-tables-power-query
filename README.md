# Функция Pdf.Tables в Power Query

## Написание функции
Pdf.Tables( pdf, optional [conditions] )

**Аргументы:**  
* pdf - файл pdf в формате binary, может быть получен функцией File.Contents;  
* [conditions] - строка дополнительных свойств (необязательный параметр).


**Результат:**  
* Таблица с содержимым всех таблиц PDF-файла. 


**Свойства в строке:**
* Implementation — версия алгоритма, используемая при идентификации таблиц. Допустимые значения: "1.2", "1.1" или NULL.
* StartPage — задает первую страницу диапазона страниц для проверки. Значение по умолчанию: 1.
* EndPage — задает последнюю страницу диапазона страниц для проверки. Значение по умолчанию — последняя страница документа.
* MultiPageTables — определяет, будут ли похожие таблицы на идущих одна за другой страницах автоматически объединяться в одну таблицу. По умолчанию — TRUE.
* EnforceBorderLines — определяет, будут ли для определения границ ячеек использоваться только линии границ (при значении TRUE) или они будут использоваться просто как одно из множества указаний (при значении FALSE). По умолчанию: FALSE.

## Примеры в коде
```
let  
    pdf_file = File.Contents("c:/files/file.pdf"), // Получаем PDF-файл
    result = Pdf.Tables(pdf_file)                  // Забираем данные из PDF-файла
in 
    result                                         // Получаем таблицу с содержимым таблиц из PDF
```


```
let  
    pdf_file = File.Contents("c:/files/file.pdf"),      // Получаем PDF-файл
    result = Pdf.Tables(pdf_file, 
        [Implementation="1.2",
        StartPage=4,
        EndPage =5, 
        MultiPageTables = false,
        EnforceBorderLines = true])                     // Забираем данные из PDF-файла
in 
    result                                              // Получаем таблицу с содержимым таблиц из PDF
```


## 12 видео для новичков по Power Query: [ССЫЛКА](https://www.youtube.com/playlist?list=PL3du-Tm1nAm6SSQOCpryquOx-6aasPARM)

