В приложении по доставке готовых продуктов были проведены АВ-тесты:  
- в первом тестировали разрешение фотографий блюд в приложении: пользователям показывались либо прямоугольные (два вида), либо новые квадратные  
- во втором была обновлена кнопка заказа, и часть юзеров видела старый вариант, а часть – новый  
Необходимо сделать соответствующие выводы на основе статистических тестов и принять решения.

## Описание данных: ##  
*1 тест:*  
id – id клиента в эксперименте  
group – в каком разрешении показывались картинки (A – прямоугольные 16:9, B – квадратные, C – прямоугольные 12:4)  
events – сколько блюд суммарно было заказано за период  

*2 тест:*  
id – id клиента в эксперименте  
segment – сегмент (high/low)  
group – вид кнопки (control – старая версия, test – новая версия)  
events – сколько блюд суммарно было заказано за период  

## Реализация: ##  
1. Проверены гипотезы о нормальности данных и гомоскедастичности дисперсий
2. Использован критерий Тьюки для сравнения попарно средних на предмет наличия между всеми группами статзначимых различий
3. Использован многофакторный ANOVA для проверки гипотезы о стат значимых различиях в реакциях юзеров каждой группы
