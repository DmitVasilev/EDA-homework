# <center>ИССЛЕДОВАНИЕ ДАННЫХ HR-АГЕНТСТВА</center>

<center> <img src='https://img.freepik.com/free-vector/futuristic-technology-infographic_23-2148462819.jpg?size=626&ext=jpg&ga=GA1.1.1546980028.1708992000&semt=ais'> </center>


##  <font color = #9ACD32> Содержание </font>

[1. Введение](https://github.com/DmitVasilev/EDA-homework?tab=readme-ov-file#-1-%D0%B2%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5-)   
[2. Описание задачи](https://github.com/DmitVasilev/EDA-homework?tab=readme-ov-file#2-%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%B7%D0%B0%D0%B4%D0%B0%D1%87%D0%B8)   
[3. Описание данных](https://github.com/DmitVasilev/EDA-homework?tab=readme-ov-file#3-%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85)   
[4. Результат](https://github.com/DmitVasilev/EDA-homework?tab=readme-ov-file#4-%D1%80%D0%B5%D0%B7%D1%83%D0%BB%D1%8C%D1%82%D0%B0%D1%82)                  
[5. Выводы](https://github.com/DmitVasilev/EDA-homework?tab=readme-ov-file#5-%D0%B2%D1%8B%D0%B2%D0%BE%D0%B4%D1%8B)

### <font color = #9ACD32> 1. Введение </font>

HR-агентство изучает тренды на рынке труда в IT. Компания хочет провести исследование на основе данных о зарплатах в сфере Data Science за 2020–2022 годы и получить некоторые выводы.

:arrow_up:[к содержанию](https://github.com/DmitVasilev/EDA-homework?tab=readme-ov-file#-%D1%81%D0%BE%D0%B4%D0%B5%D1%80%D0%B6%D0%B0%D0%BD%D0%B8%D0%B5-)     


###  <font color = #9ACD32>2. Описание задачи</font>
            
Исследуйте данные и сделайте выводы по полученным результатам. Подкрепите свои рассуждения и выводы визуализациями и с помощью статистического тестирования проверьте, являются ли выводы статистически значимыми.

В процессе анализа необходимо:

 1. Выяснить, какие факторы влияют на зарплату специалиста Data Scientist.                  
 2. А также ответить на ключевые вопросы HR-агентства:               
     + Наблюдается ли ежегодный рост зарплат у специалистов Data Scientist?                
     + Как соотносятся зарплаты Data Scientist и Data Engineer в 2022 году?              
     + Как соотносятся зарплаты специалистов Data Scientist в компаниях различных размеров?                  
     + Есть ли связь между наличием должностей Data Scientist и Data Engineer и размером компании?                   

Если в данных обнаружаться интересные закономерности, также отметьте их в своём анализе.

Продемонстрируйте использование разных тестов для проверки статистической значимости сделанных выводов:                   

 + тесты для количественного признака:             
     + для одной выборки;              
     + для двух выборок;             
     + для нескольких выборок;           
 + тест для категориальных признаков.

:arrow_up:[к содержанию](https://github.com/DmitVasilev/EDA-homework?tab=readme-ov-file#-%D1%81%D0%BE%D0%B4%D0%B5%D1%80%D0%B6%D0%B0%D0%BD%D0%B8%D0%B5-)               
                                 
###  <font color = #9ACD32>3. Описание данных</font>

Оригинальный датасет: ["Data Science Job Salaries (kaggle.com)"](https://www.kaggle.com/datasets/ruchi798/data-science-job-salaries)

**Описание столбцов:**               
 + work_year -	Год, в котором была выплачена зарплата.                

 + experience_level - Опыт работы на этой должности в течение года со следующими возможными значениями:              
     + EN — Entry-level/Junior;               
     + MI — Mid-level/Intermediate;               
     + SE — Senior-level/Expert;              
     + EX — Executive-level/Director.                 
 
 + employment_type - Тип трудоустройства для этой роли:                
     + PT — неполный рабочий день;               
     + FT — полный рабочий день;               
     + CT — контракт;                  
     + FL — фриланс.                 

 + job_title - Роль, в которой соискатель работал в течение года.

 + salary - Общая выплаченная валовая сумма заработной платы.

 + salary_currency - Валюта выплачиваемой заработной платы в виде кода валюты ISO 4217.

 + salary_in_usd - Зарплата в долларах США (валютный курс, делённый на среднее значение курса доллара США за соответствующий год через fxdata.foorilla.com).

 + employee_residence - Основная страна проживания сотрудника в течение рабочего года в виде кода страны ISO 3166.

 + remote_ratio - Общий объём работы, выполняемой удалённо. Возможные значения:              
     + 0 — удалённой работы нет (менее 20 %);            
     + 50 — частично удалённая работа;                 
     + 100 — полностью удалённая работа (более 80 %).

 + company_location - Страна главного офиса работодателя или филиала по контракту в виде кода страны ISO 3166.
 + company_size - Среднее количество людей, работавших в компании в течение года:

     + S — менее 50 сотрудников (небольшая компания);
     + M — от 50 до 250 сотрудников (средняя компания);
     + L — более 250 сотрудников (крупная компания).

:arrow_up:[к содержанию](https://github.com/DmitVasilev/EDA-homework?tab=readme-ov-file#-%D1%81%D0%BE%D0%B4%D0%B5%D1%80%D0%B6%D0%B0%D0%BD%D0%B8%D0%B5-)                    

###  <font color = #9ACD32>4. Результат</font>

Ноутбук с решением на GitHub: [EDA4_homework.ipynb](https://github.com/DmitVasilev/EDA-homework/blob/438919679991d481420004bdfb17e8fc45f70bed/EDA4_homework.ipynb).     
 
Обеспечить воспроизводимость кода поможет файл requirements.txt: [requirements.txt](https://github.com/DmitVasilev/EDA-homework/blob/438919679991d481420004bdfb17e8fc45f70bed/requirements.txt). 
                        
:arrow_up:[к содержанию](https://github.com/DmitVasilev/EDA-homework?tab=readme-ov-file#-%D1%81%D0%BE%D0%B4%D0%B5%D1%80%D0%B6%D0%B0%D0%BD%D0%B8%D0%B5-)     


###  <font color = #9ACD32>5. Выводы</font>

 + проведен визуальный анализ на основе которого сделаны первичные предположения о влиянии признаков на заработную плату;
 + выдвинуты дополнительные гипотезы для подтверждения с использованием статистических тестов;
 + проведен статистический анализ с использованием статистических тестов для одной, двух, нескольких выборок, а также тестов для категориальных признаков.
                             
:arrow_up:[к содержанию](https://github.com/DmitVasilev/EDA-homework?tab=readme-ov-file#-%D1%81%D0%BE%D0%B4%D0%B5%D1%80%D0%B6%D0%B0%D0%BD%D0%B8%D0%B5-)        
