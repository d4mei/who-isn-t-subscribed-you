Мне захотелось узнать, кто не подписан на меня в ответ в инстаграмме, поэтому решил написать для этого код.
 Проверять в ручную кто подписан, а кто нет очень долгое занятие, программа сократит это время во много раз.
 Код представлен в файле на языке Golang. Самый главный вопрос для меня это был как сделать два слайса со списками подписчиков и подписок.
 Способ к которому я пришёл довольно муторный, но зато рабочий. 
Сначала я скопировал всех людей из подписок и вставил всё в текстовый файл (далее расскажу зачем), потом этот же весь текст в книгу Excel.
 В Excel я сделал так, чтобы каждая строчка бралась в кавычки и после каждой строчки ставилась запятая.
 Казалось бы можно было сразу весь текст копировать в Excel, но проблема в том, что вместе с текстом копируются фотографии аватаров профилей. 
Текстовый документ заменяет эти фотографии на текст "Фото профиля...".
Ну и после этого копирую все ячейки из ecxel в массивы.

Сам код очень простой.
Сначала у меня идёт цикл for который работает столько раз, сколько элементов в слайсе subscriptions(подписки)
в переменную cache записываем элемент который рассматриваем в данный момент и в переменную count 0
Далее идёт следующий цикл который просматривает слайс подписчиков и ищет совпадения.
Если совпадение присутствует, то к переменной count добавляем один.
Далее делаем проверку: если переменная count=0 то совпадений не было, то есть профиля из списка подписок нету в списке подписчиков,
а это значит что человек не подписан на нас. Вот и всё.

Это мой первый довольно оригинальный и полезный проект, но мне кажется что его можно было бы немного упростить.

***Copied from google translate***

I wanted to know who did not follow me in response to instagram, so I decided to write a code for this.
 Checking manually who is signed and who is not is a very long task, the program will reduce this time many times over.
 The code is presented in a file in Golang. The most important question for me was how to make two slices with lists of subscribers and subscriptions.
 The method to which I came is rather dreary, but working.
First, I copied all the people from the subscriptions and pasted everything into a text file (I’ll tell you why later), then the same entire text into an Excel workbook.
 In Excel, I made it so that each line was taken in quotes and a comma was placed after each line.
 It would seem that it would be possible to copy all the text into Excel at once, but the problem is that profile avatars are copied along with the text.
The text document replaces these photos with the text "Profile photo...".
Well, after that I copy all the cells from ecxel to arrays.

The code itself is very simple.
First, I have a for loop that runs as many times as there are elements in the subscriptions slice (subscriptions)
in the cache variable we write the element that we are currently considering and in the count 0 variable
Next comes the next loop that looks through the slice of subscribers and looks for matches.
If there is a match, then add one to the count variable.
Next, we check: if the variable count=0, then there were no matches, that is, the profile from the list of subscriptions is not in the list of subscribers,
which means that the person is not subscribed to us. That's all.

This is my first rather original and useful project, but it seems to me that it could be simplified a bit.