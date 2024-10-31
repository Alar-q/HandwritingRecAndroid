# Handwriting-Recognition   

Разработка приложения для распознавания рукописного текста наказахском языке.

## About
School research project focusing on the development of an application for recognising handwritten text written in Kazakh.

The project's main stack was Java development for Android and used DL4J, OpenCV. A standard neural network representing non-linear logistic regression was developed from scratch.

The evolution of the project is to abstract away from the specific problem and develop tensors and operations on them for machine learning: [Tensor-Library](https://github.com/Alar-q/Tensor-library).

## Demonstration

https://github.com/Alar-q/HandwritingRecAndroid/assets/72505048/4e19404b-a9fb-493a-9e88-180db9f6ea89

https://github.com/Alar-q/HandwritingRecAndroid/assets/72505048/28f5d4d9-6dd7-48d2-9dc7-47cab7faec8b

## Documents

[Presentation](https://github.com/Alar-q/HandwritingRecAndroid/blob/master/assets/%D0%90%D0%BB%D0%B0%D1%80%20%D0%90%D0%BA%D0%B8%D0%BB%D1%8C%D0%B1%D0%B5%D0%BA%D0%BE%D0%B2%20%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%821.pdf)

[Paper](https://github.com/Alar-q/HandwritingRecAndroid/blob/master/assets/%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%90%D0%BB%D0%B0%D1%80.docx)

## References
- Прохоренок, Н. А. (2018). OpenCV и Java. Обработка изображений и компьютерное зрение. БХВ-Петербург.
- Rashid, T. (2016). Make Your own neural network. CreateSpace Independent Publishing Platform.
- Patterson, J., & Gibson, A. (2017). Deep learning: A practitioner’s approach (First edition). O’Reilly.
- Goodfellow, I., Bengio, Y., & Courville, A. (2016). Deep learning. The MIT press.

## Results

Ru: Диплом первой степени республиканского конкурса научных проектов по общеобразовательным предметам.

Eng: First degree diploma of the republican competition of scientific projects in general education subjects.

![гос_проект _page-0001](https://github.com/Alar-q/HandwritingRecAndroid/assets/72505048/e45bc32b-3a26-4a47-84e1-d2f5a625f1bd)


## Выпуски 19/03/2021

![photo_2024-02-09_15-46-34](https://github.com/Alar-q/Handwriting-Recognition/assets/72505048/1ab223ee-5c84-4734-b686-5a60ee3ea5e9)

[Телеканал 24kz (Youtube). (27 Jul 2021). Рукописное сделает печатным | Hi-Tech](https://www.youtube.com/watch?v=sn8fddtPbFc&ab_channel=%D0%A2%D0%B5%D0%BB%D0%B5%D0%BA%D0%B0%D0%BD%D0%B0%D0%BB24kz)

[ПАВЛОДАРСКИЕ РАЗРАБОТЧИКИ - ЛУЧШИЕ В РЕСПУБЛИКЕ](https://tou.edu.kz/ru/news/9824-pavlodarli-mamandar-respublikada-zdk)

[Республикалық ғылыми жобалар конкурсының қорытындысы](https://www.jasdarynpvl.edu.kz/journal/view/1/523)

[https://khabar.kz/ru/news/nauka-i-obrazovanie/item/131059-shkolnik-razrabotal-unikalnoe-prilozhenie-po-raspoznavaniyu-kazakhskogo-rukopisnogo-teksta](https://khabar.kz/ru/news/nauka-i-obrazovanie/item/131059-shkolnik-razrabotal-unikalnoe-prilozhenie-po-raspoznavaniyu-kazakhskogo-rukopisnogo-teksta)

## Description 02/2021
Программа написана на Java, с использованием открытых библиотек OpenCV и DL4J, под android, не составляет труда перенести ее на другие платформы.  На разработку ушло 2 месяца. Изначально я писал на Java полносвязную искусственную нейронную сеть с нуля, и я написал, но скорость обучения и прогнозирования медленнее библиотеки DL4J. Мне были интересны нейронные сети и интересны до сих пор. Тема проекта была выбрана при обсуждении направления проекта с научным консультантом Дарией Болатовной.  Изначально было умение программировать, чему я научился, изучая литературу, и желание сделать что-нибудь из области искусственного интеллекта.  

Я также добавил словарь казахского языка, откуда программа может предлагать наиболее похожие слова, так как ошибки при распознавании все же есть. Думаю, что можно улучшить метод со словарем, создав систему понимания контекста данного текста. Например, люди, читая записки врача, пытаются найти именно "медицинские" термины.

Проблема программы в том, что каждая буква должна быть написана раздельно, а так обычно не пишут. Я думаю, что можно объединить технологию рукописного ввода и рекуррентные нейронные сети с долгой краткосрочной памятью и, тем самым, распознавать непрерывный рукописный текст, написанный любым почерком.



## Technical Description 02/2021
                          Off line handwritten text recognition using DL4J and OpenCV libs
                          
Off line подразумевает, что слово сегментируется на буквы, эти буквы проходят через нейронку и получается криво предсказанное слово.
On line - то как работает рукописный ввод. Анализ векторизованных каракуль человека. То есть там, наверное, используется рекуррентная 
нейронная сетьможет быть обычный алгоритм k-ближайших соседей. В этом случае нужна база ВСЕХ слов. 
                          
  1) Первая Activity - меню (StartButton.java), просто запускает камеру Activity (WordRecActivity)
  
  2) WordRecActivity. Наверное, я переименую этот класс "CameraActivity". Показывает на экране вид с задней камеры обводя 
прямоугольниками объекты похожие на слова, должен слова....

  3) SelectActivity - основной класс распознавания.
  
    SelectActivity запускает SelectScreen где можно выбрать именно те слова, которые надо распознать, перевести в печатный. 
После того как выбрали и нажали на кнопочку "перевести в текст" в этом же классе обрабатываются
эти слова. 

    Обработка выбранных слов: сортируем слова слева направо (можно добавить и по высоте);
находим буквы в слове (просто проводим контуры слова через morphologyEx и выбираем непрерывные контуры);
дальше копируем эти прямоугольные области(буквы) и передаем нейронке эти картинки в том виде на котором она обучалась, в этом случае 
на черно-белых, то есть значения равны либо 1-му, либо 0-ю; 
Дальше соединяем эти предсказанные буквы слева направо и получаем слово.

Слова передаются в RecognizedScreen где можно делать с ними все что угодно. Так же я добавил казахский словарь слов из которого 
находятся наиболее похожие слова.


