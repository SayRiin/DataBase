# UnemployedCenter
База данных для хранения информации  о безработных в центре занятости.


## Таблицы базы данных

### PersonalInfo
| Поле             | Тип     | Описание                 |
|------------------|---------|--------------------------|
| ID               | int     | Уникальный идентификатор |
| FullName         | varchar | ФИО безаработного        |
| Gender           | varchar | Пол безработного         |
| Address          | varchar | Адрес                    |
| Phone_number     | varchar | Номер телефона           |
| Email            | varchar | Электронная почта        |
| Passport         | varchar | Пасспорт                 |
| Birthday         | date    | Дата рождения            |
| Education_level  | varchar | Уровень образования      |

### Vacancy
| Поле             | Тип       | Описание                                      |
|------------------|-----------|-----------------------------------------------|
| ID               | int       | Уникальный идентификатор                      |
| Unemployed_ID    | int       | Внешний ключ, ссылающийся на PersonalInfo(ID) |
| Job_vacancy      | varchar   | Вакансия                                      |
| Summary          | varchar   | Резюме                                        |
| Job_title        | varchar   | Название работы                               |
| Company_name     | varchar   | Название компании                             |
| Salary           | int       | Зарплата                                      |
| Location         | varchar   | Местоположение                                |
| Contact_email    | varchar   | Электронная почта компании                    |

### EmploymentHistory
| Поле                    | Тип     | Описание                                      |
|-------------------------|---------|-----------------------------------------------|
| ID                      | int     | Уникальный идентификатор                      |
| Unemployed_ID           | int     | Внешний ключ, ссылающийся на PersonalInfo(ID) |
| Work_experience         | int     | Опыт работы                                   |
| Last_job_title          | varchar | Название последней работы                     |
| Last_employer           | varchar | Название последней должности                  |
| Reason_for_unemployment | varchar | Причина увольнения с прошлой работы           |
| Date_registered         | date    | Дата регистрации                              |
