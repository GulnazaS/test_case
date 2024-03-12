Задача
Создать и обучить классификатор, эффективно классифицирующий рентгенографические снимки (далее - РГ) на три класса:
- Фронтальная проекция(frontal), 
- Боковые проекции(lateral)
- Cнимки, содержащие иные проекции и органы (trash)

Условия
Для решения задачи представлено два датасета:
1)	Тренировочный датасет (Train)
2)	Валидационный датасет (Validation)
Ссылка на датасет:
(train)https://drive.google.com/file/d/1fAS2HSxciUzeqK3SqEXdRTOwTZS5tM6s/view?usp=sharing
(validation)https://drive.google.com/file/d/1Q0D76IoLQU2BrEJe5yYQUj7qia6FflyF/view?usp=sharing
Датасет Train (находится в соответствующей папке) состоит из 4188 РГ снимков формата PNG, разбитых на подвыборки. Данный датасет предназначен для обучения классификатора.
Класс «FRONTAL» (находится в соответствующей папке) датасета Train состоит из 1399 снимков во фронтальной проекции.
Класс «LATERAL» (находится в соответствующей папке) датасета Train состоит из 1400 снимков в боковой проекции.
Класс «TRASH» (находится в соответствующей папке) датасета Train состоит из 1389 снимков, содержащих иные проекции и органы.
 
Датасет Validation состоит из 1000 РГ изображений формата PNG. 
Класс «FRONTAL» (находится в соответствующей папке) датасета Validation состоит из 330 снимков во фронтальной проекции.
Класс «LATERAL» (находится в соответствующей папке) датасета Validation состоит из 330 снимков в боковой проекции. 
Класс «TRASH» (находится в соответствующей папке) датасета Validation состоит из 340 снимков, содержащих иные проекции и органы.
Датасет Validation предназначен для открытой валидации классификатора, снимки из данного датасета не принимают участие в обучении.

Результат
Результат работы должен быть представлен в виде CSV таблицы, где в 1-м столбце (image_id) должны быть построчно записаны все идентификаторы (названия) файлов изображений из датасета Validation (1000 штук), а в трех последующих столбцах каждому из идентификаторов должно быть поставлено в соответствии значение активации создаваемого классификатором:frontal, lateral, trash. Кроме того, должен быть представлен скрипт самого классификатора на языке python для инференса и файлы весов
