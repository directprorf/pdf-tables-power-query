# Функция Pdf.Tables в Power Query

## Написание функции
Pdf.Tables( pdf, optional [conditions] )

**Аргументы:**  
* pdf - файл pdf в формате binary, может быть получен функцией File.Contents;  
* [conditions] - строка дополнительных свойств (необязательный параметр).


**Результат:**  
* Таблица с содержимым всех таблиц PDF-файла. 

## Примеры в коде
```
let  
    pdf_file = File.Contents("c:/files/file.pdf"), // Получаем PDF-файл
    result = Pdf.Tables(pdf_file)                  // Забираем данные из PDF-файла
in 
    result                                         // Получаем таблицу со содержимым таблиц из PDF
```


```
let  
    pdf_file = File.Contents("c:/files/file.pdf"), // Получаем PDF-файл
    result = Pdf.Tables(pdf_file)                  // Забираем данные из PDF-файла
in 
    result                                         // Получаем таблицу со содержимым таблиц из PDF
```

## 12 видео для новичков по Power Query: [ССЫЛКА](https://www.youtube.com/playlist?list=PL3du-Tm1nAm6SSQOCpryquOx-6aasPARM)

