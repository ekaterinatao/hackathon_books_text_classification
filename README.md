# Hackathon. Code Crusaders (C+)

## Table of contents 
[1. Our team](https://github.com/ekaterinatao/hackathon_books_text_classification?tab=readme-ov-file#team)   
[2. Description](https://github.com/ekaterinatao/hackathon_books_text_classification?tab=readme-ov-file#description)   
[3. Aim](https://github.com/ekaterinatao/hackathon_books_text_classification?tab=readme-ov-file#aim)  
[4. Datasets and code](https://github.com/ekaterinatao/hackathon_books_text_classification?tab=readme-ov-file#datasets-and-code)  
[5. Result](https://github.com/ekaterinatao/hackathon_books_text_classification?tab=readme-ov-file#result)    

## Team
Ilia Beliakov - project manager  
[Ekaterina Tao](https://github.com/ekaterinatao) - ML engineer  
Alexander Zhuravlev - ML, data engineer  
Bogdan Kostyuk - data engineer  
Anna Rybakova - data engineer   
Danila Lyulya - data analyst  
Denisov Sergey - ML engineer  

## Description
Задача 3: Разработка модели для автоматизированного определения структуры книги и назначения стилей абзацев и символов
Заказчик: ЭКСМО   

## Aim
Описание: Цель проекта заключается в создании модели, способной анализировать текст книги и, на основе его форматирования и логической структуры, автоматически применять соответствующие стилистики шаблоны к абзацам и символам. Модель должна уметь распознавать и различать заголовки, подзаголовки, основной текст, список, цитаты и другие типичные элементы структуры текста, присваивая им предопределённые стили. Это позволит стандартизировать внешний вид различных книг в соответствии с внутренними стандартами издательства.

Что будет дано: примеры текстов, требования к назначенным стилям (руководство по подготовке электронных книг).

## Datasets and code
Код для парсинга книг в формате `fb2` [здесь](https://github.com/ekaterinatao/hackathon_books_text_classification/blob/main/Parsing_one_file_new.ipynb).  

Пример собранного датасета [здесь](https://github.com/ekaterinatao/hackathon_books_text_classification/tree/main/data).  

**Распарсеные тэги:**  
  
* `p` - любой абзац (исключая абзацы, обозначенные другими тэгами)  
* `title` - заголовок 
* `subtitle` - подзаголовок  
* `poem` - стихи  
* `cite` - цитата  
* `epigraph` - эпиграф 
* `author` - автор  
* `annotation` - аннотация  
* `book-title` - название книги   
* `publisher` - издательство  
* `keywords` - ключевые слова  
* `note` - примечания  

## Result

**Пайплайн**  
  
* На вход подается текст в формате `docx`  
* Проводится анализ и предобработка текста для его подачи в модель  
* Разметка текста с помощью предобученной модели из семейства `BERT`  
* На выход выдается файл в формате `xml`  
  
Код для запуска пайплайна и разметки текста в формате `docx` с последующим сохранением размеченного файла в формате `xml` можно найти [здесь](https://github.com/ekaterinatao/hackathon_books_text_classification/blob/main/inference_pipeline.ipynb).  
  
**Метрики лучшей модели:**  
![](https://github.com/ekaterinatao/hackathon_books_text_classification/blob/main/data/metrics_final_model.JPG) ![](https://github.com/ekaterinatao/hackathon_books_text_classification/blob/main/data/labels_final_model.JPG)  

Финальная модель [здесь](https://github.com/ekaterinatao/hackathon_books_text_classification/blob/main/code_sber_ruRoberta_ru_final.ipynb).  
Сохраненный чекпойнт модели на [huggingface](https://huggingface.co/ekaterinatao/books_text_class_roBERTa_ru_big/tree/main).  