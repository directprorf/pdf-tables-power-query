# Функция Pdf.Tables в Power Query

## Написание функции
Pdf.Tables( pdf, [optional conditions] )

**Аргументы:**  
* pdf - список значений в формате списка,  
* [conditions] - строка дополнительных свойств (необязательный параметр).


**Результат:**  
* Таблица с содержимым всех таблиц из PDF-файла. 

## Примеры в коде
```
let  
    letters = {"a","б","в","г"},          // Задаём список из букв
    one = "Б",                            // Задаём букву для поиска в списке
    result = List.Contains(letters, one)  // Проверяем наличие буквы в списке
in 
    result                                // Выдаёт FALSE так как большая буква Б не содержится в списке.
```


```
let  
    letters = {"a","б","в","г"},                                      // Задаём список из букв
    one = "Б",                                                        // Задаём букву для поиска в списке
    result = List.Contains(letters, one, Comparer.OrdinalIgnoreCase)  // Проверяем наличие буквы в списке
in 
    result                                                            //Выдаёт TRUE так как при сравнении игнорируется регистр.
```

## 12 видео для новичков по Power Query: [ССЫЛКА](https://www.youtube.com/playlist?list=PL3du-Tm1nAm6SSQOCpryquOx-6aasPARM)

