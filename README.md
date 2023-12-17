# Hackathon. Code Crusaders (C+)

## Table of contents 
[1. Our team](https://github.com/ekaterinatao/hackathon_books_text_classification#team)   
[2. Description](https://github.com/ekaterinatao/hackathon_books_text_classification#description)   
[3. Aim](https://github.com/ekaterinatao/hackathon_books_text_classification#aim)  
[4. Datasets and code](https://github.com/ekaterinatao/hackathon_books_text_classification#datasets-and-code)  
[5. Result](https://github.com/ekaterinatao/hackathon_books_text_classification#result)    

## Team
Ilia Beliakov - project manager  
[Ekaterina Tao](https://github.com/ekaterinatao) - ML engineer  
Alexander Zhuravlev - data engineer  
Bogdan Kostyuk - data engineer  
Anna Rybakova - data engineer   
Danila Lyulya - data analyst  

## Description
Задача 3: Разработка модели для автоматизированного определения структуры книги и назначения стилей абзацев и символов
Заказчик: ЭКСМО   

## Aim
Описание: Цель проекта заключается в создании модели, способной анализировать текст книги и, на основе его форматирования и логической структуры, автоматически применять соответствующие стилистики шаблоны к абзацам и символам. Модель должна уметь распознавать и различать заголовки, подзаголовки, основной текст, список, цитаты и другие типичные элементы структуры текста, присваивая им предопределённые стили. Это позволит стандартизировать внешний вид различных книг в соответствии с внутренними стандартами издательства.

Что будет дано: примеры текстов, требования к назначенным стилям (руководство по подготовке электронных книг).

## Datasets and code
Код для парсинга книг в формате `fb2` [здесь](https://github.com/ekaterinatao/hackathon_books_text_classification/blob/main/Parsing_one_file_new.ipynb).  

Пример собранного датасета [здесь](https://github.com/ekaterinatao/hackathon_books_text_classification/tree/main/raw_data).  

**Распарсено 10 тэгов:**  
  
* `p` - любой абзац  
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

Код базовой модели классификации текста на основе RoBERTa RU [здесь]().

## Result 
С базовыми настройками модели достигнуты следующие метрики:  


Отчет об обучении модели на [wandb]().  
Сохраненный чекпойнт модели на [huggingface]().  