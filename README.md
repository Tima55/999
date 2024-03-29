![](https://upload.wikimedia.org/wikipedia/ru/4/48/Geekbrains_logo.svg)



## 🟥 Инфopмaция o пpoeктe

Необходимо организовать систему учета для питомника, в котором живут домашние и вьючные животные.

## 🟧 Зaдaниe

### 1. Задание на проверку навыков работы в операционной системе Linux Ubuntu

1.1. Используя команду `cat` в терминале операционной системы `Linux`, создать два файла:
  - `Домашние животные` (заполнив файл `собаками`, `кошками`, `хомяками`)
  - `Вьючные животные` (заполнив файл `лошадьми`, `верблюдами`, `ослами`)

Затем объединить их. Просмотреть содержимое созданного файла. Переименовать файл, дав ему новое имя - `Друзья человека`.

1.2. Создать директорию, переместить файл туда  
1.3. Подключить дополнительный репозиторий `MySQL`. Установить любой пакет из этого репозитория  
1.4. Установить и удалить `deb-пакет` с помощью `dpkg`  
1.5. Выложить историю команд в терминале `Ubuntu`  

### 2. Задание на проверку навыков работы c MySQL

2.1. Нарисовать диаграмму, в которой есть класс родительский класс, домашние животные и вьючные животные, в составы которых в случае `домашних животных` войдут классы: `собаки`, `кошки` и `хомяки`, а в класс `вьючные животные`
войдут: `лошади`, `верблюды` и `ослы`  
2.2. В подключенном `MySQL` репозитории создать базу данных `Друзья человека`  
2.3. Создать таблицы с иерархией из диаграммы в БД  
2.4. Заполнить низкоуровневые таблицы `именами животных`, `командами` которые они выполняют и `датами рождения`  
2.5. Объединить таблицы `лошади` и `ослы` в одну таблицу, удалив из таблицы `верблюдов`, так как верблюдов решили перевезти в другой питомник на зимовку  
2.6. Создать новую таблицу `молодые животные` в которую попадут все животные старше `1` года, но младше `3` лет и в отдельном столбце с точностью до месяца подсчитать возраст животных в новой таблице  
2.7. Объединить все таблицы в одну, при этом сохраняя поля, указывающие на прошлую принадлежность к старым таблицам  

### 3. Заключительное задание итоговой aттecтaции

3.1. Создать класс с __инкапсуляцией__ методов и наследованием по диаграмме  
3.2. Написать программу, имитирующую работу реестра домашних животных  
3.3. В программе должен быть реализован следующий функционал:  
&#8203; &#8203; &#8203; &#8203; &#8203; &#8203; &#8203; &#8203;3.3.1. *Заводить новое животное*  
&#8203; &#8203; &#8203; &#8203; &#8203; &#8203; &#8203; &#8203;3.3.2. *Определять животное в правильный класс*  
&#8203; &#8203; &#8203; &#8203; &#8203; &#8203; &#8203; &#8203;3.3.3. *Увидеть список команд, которое выполняет животное*  
&#8203; &#8203; &#8203; &#8203; &#8203; &#8203; &#8203; &#8203;3.3.4. *Обучить животное новым командам*  
&#8203; &#8203; &#8203; &#8203; &#8203; &#8203; &#8203; &#8203;3.3.5. *Реализовать навигацию по меню*  
3.4. Создайте класс `Счетчик`, у которого есть метод `add()`, увеличивающий начение внутренней `int` переменной на `1` при нажатии `Завести новое животное`. Сделайте так, чтобы с объектом такого типа можно было работать в блоке `try-with-resources`. Нужно бросить исключение, если работа с объектом типа счетчик была не в ресурсном `try` и/или ресурс остался открыт. Значение считать в ресурсе `try`, если при заведении животного заполнены все поля  

## 🟩 Cтpyктypa пpoeктa

```txt
java/
└─ final-certification-2023/
   ├─ diagrams/
   │  ├─ uml.drawio
   │  └─ uml.drawio.png
   ├─ images/
   │  ├─ 1.1_task_screenshot.png
   │  ├─ 1.2_task_screenshot.png
   │  ├─ 1.3.1_task_screenshot.png
   │  ├─ 1.4_task_screenshot.png
   │  ├─ 2.2_task_screenshot.png
   │  ├─ 2.3_task_screenshot.png
   │  ├─ 2.4.1_task_screenshot.png
   │  ├─ 2.4.2_task_screenshot.png
   │  ├─ 2.4.3_task_screenshot.png
   │  ├─ 2.4.4_task_screenshot.png
   │  ├─ 2.4.5_task_screenshot.png
   │  ├─ 2.5.1_task_screenshot.png
   │  ├─ 2.5.2_task_screenshot.png
   │  ├─ 2.6_task_screenshot.png
   │  └─ 2.7_task_screenshot.png
   ├─ src/
   │  └─ com/
   │     └─ kennel/
   │        ├─ controller/
   │        ├─ └─ KennelAccounting.java
   │        ├─ model/
   │        │  ├─ implement/
   │        │  │  ├─ Camel.java
   │        │  │  ├─ Cat.java
   │        │  │  ├─ Dog.java
   │        │  │  ├─ Donkey.java
   │        │  │  ├─ Hamster.java
   │        │  │  └─ Horse.java
   │        │  ├─ AbstractAnimal.java
   │        │  ├─ AbstractPackAnimal.java
   │        │  ├─ AbstractPet.java
   │        │  ├─ AnimalGenius.java
   │        │  └─ Skill.java
   │        ├─ storage/
   │        │  ├─ KennelStorage.java
   │        │  └─ Storage.java
   │        ├─ util/
   │        │  └─ Counter.java
   │        ├─ view/
   │        │  ├─ ConsoleView.java
   │        │  └─ View.java
   │        └─ Main.java
   ├─ Животные/
   │  └─ Друзья_человека
   ├─ Вьючные_животные
   ├─ Домашние_животные
   ├─.gitignore
   └─ README.md
```

Пpoeкт итоговой аттестации cтpyктypиpoвaн в oднoм кaтaлoгe. Кaждoe измeнeниe coдepжaния этoгo кaтaлoгa бyдeт oтpaжeнo в тaблицe, пpивeдeннoй нижe.

Кaтaлoги и фaйлы                                    | Опиcaниe
----------------------------------------------------|--------------------------------------------------------------------------------------------
`/java/final-certification-2023/`                   | Кaтaлoг итоговой аттестации
`/final-certification-2023/diagrams/`               | Каталог с диаграммой классов к заданию 2.1.
`/final-certification-2023/images/`                 | Каталог со скриншотами, подтверждающими выполнение заданий с 1.1. по 2.7
`/final-certification-2023/Животные/`               | Каталог с файлом к заданию 1.2.
`/final-certification-2023/src/com/kennel`          | Каталог программы на языке Java
`/final-certification-2023/Вьючные_животные`        | Фaйл задания 1.1.
`/final-certification-2023/Домашние_животные`       | Фaйл задания 1.1.
`/final-certification-2023/.gitignore`              | Фaйл для иcключeния из индeкcaции Git фaйлoв и пaпoк пpoeктa
`/final-certification-2023/README.md`               | Oпиcaниe зaдaчи, eё peшeния, a тaкжe дpyгих фaйлoв пpoeктa

## 🟦 Решение

### 1. Задание на проверку навыков работы в операционной системе Linux Ubuntu

<details>
<summary><b>1.1.</b></summary>

Создаем файл `Домашние_животные` и вводим в него данные с клавиатуры:

```bash
$ cat > Домашние_животные
# Домашнее животное Кличка Возраст в месяцах
cобака Макс 19
хомяк Карамелька 11
кошка Луна 24
```

Нажимаем `Ctrl+D` для сохранения данных.

Создаем файл `Вьючные_животные` и вводим в него данные с клавиатуры:

```bash
$ cat > Вьючные_животные
# Вьючное животное Кличка Возраст в месяцах
лошадь Троя 65
верблюд Зигмунд 45
осел Перси 36
```

Нажимаем `Ctrl+D` для сохранения данных.

Объединяем созданные файлы `Домашние_животные` и `Вьючные_животные`:

```bash
$ cat Домашние_животные Вьючные_животные > Все_животные
```

Просматриваем содержимое созданного файла `Все_животные`:

```bash
$ cat Все_животные
```

Переименовываем файл `Все_животные` в `Друзья_человека`:

```bash
$ mv Все_животные Друзья_человека
```

![](./images/1.1_task_screenshot.png "Подтверждение выполнения задания 1.1.")

</details>

<details>
<summary><b>1.2.</b></summary>

Создаем директорию `Животные`:

```bash
$ mkdir Животные
```

Перемещаем файл `Друзья_человека` в директорию `Животные`:

```bash
$ mv Друзья_человека Животные/
```

![](./images/1.2_task_screenshot.png "Подтверждение выполнения задания 1.2.")

</details>

<details>
<summary><b>1.3.</b></summary>

Подключаем дополнительный репозиторий `MySQL`. Устанавливаем любой пакет из этого репозитория:

```bash
$ sudo wget https://dev.mysql.com/get/mysql-apt-config_0.8.24-1_all.deb
$ sudo dpkg -i mysql-apt-config_0.8.24-1_all.deb
$ sudo apt update
$ sudo apt install mysql-server mysql-client
$ systemctl status mysql.service
```

![](./images/1.3.1_task_screenshot.png "Подтверждение выполнения задания 1.3.")
![](./images/1.3.2_task_screenshot.png "Подтверждение выполнения задания 1.3.")

</details>

<details>
<summary><b>1.4.</b></summary>

Устанавливаем и удаляем `deb-пакет` с помощью `dpkg`:

```bash
$ sudo dpkg -i mysql-apt-config_0.8.24-1_all.deb
$ sudo dpkg -r mysql-apt-config
$ sudo dpkg --purge mysql-apt-config
```

![](./images/1.4_task_screenshot.png "Подтверждение выполнения задания 1.4.")

</details>

<details>
<summary><b>1.5.</b></summary>

Подтверждение истории команд в терминале для заданий с 1.1. по 1.4.:

![](./images/1.1_task_screenshot.png "Подтверждение выполнения задания 1.1.")
![](./images/1.2_task_screenshot.png "Подтверждение выполнения задания 1.2.")
![](./images/1.3.1_task_screenshot.png "Подтверждение выполнения задания 1.3.")
![](./images/1.3.2_task_screenshot.png "Подтверждение выполнения задания 1.3.")
![](./images/1.4_task_screenshot.png "Подтверждение выполнения задания 1.4.")

</details>

### 2. Задание на проверку навыков работы c MySQL

<details>
<summary><b>2.1.</b></summary>

Диаграмма классов:

![](./diagrams/uml.drawio.png "Диаграмма классов")
 
</details>

<details>
<summary><b>2.2.</b></summary>

Cоздаем базу данных `Друзья человека`:

```sql
CREATE DATABASE IF NOT EXISTS HumanFriends;
USE HumanFriends;
```

![](./images/2.2_task_screenshot.png "Подтверждение выполнения задания 2.2.")

</details>

<details>
<summary><b>2.3.</b></summary>

Создаем таблицы с иерархией из диаграммы в БД:

```sql
CREATE TABLE Commands
(
    id INT PRIMARY KEY NOT NULL AUTO_INCREMENT,
    name varchar(30),
    description varchar(255)
);

CREATE TABLE AnimalGroup
(
    id INT PRIMARY KEY NOT NULL AUTO_INCREMENT,
    name varchar(30)
);
   
CREATE TABLE AnimalGenius
(
    id INT PRIMARY KEY NOT NULL AUTO_INCREMENT,
    name varchar(30),
    group_id INT,
    FOREIGN KEY (group_id) REFERENCES AnimalGroup (id)
    ON DELETE CASCADE ON UPDATE CASCADE
);
   
CREATE TABLE KennelAnimal
(
    id INT PRIMARY KEY NOT NULL AUTO_INCREMENT,
    name varchar(30),
    birthDate DATE,
    genius_id INT,
    FOREIGN KEY (genius_id) REFERENCES AnimalGenius (id)
    ON DELETE CASCADE ON UPDATE CASCADE
);
   
CREATE TABLE AnimalCommands
(
    animal_id INT NOT NULL,
    command_id INT NOT NULL,

    PRIMARY KEY (animal_id, command_id),
    FOREIGN KEY (animal_id) REFERENCES KennelAnimal (id)
     ON DELETE CASCADE ON UPDATE CASCADE,
    FOREIGN KEY (command_id) REFERENCES Commands (id)
     ON DELETE CASCADE  ON UPDATE CASCADE
);
```

![](./images/2.3_task_screenshot.png "Подтверждение выполнения задания 2.3.")

</details>

<details>
<summary><b>2.4.</b></summary>

Заполняем низкоуровневые таблицы `именами животных`, `командами` которые они выполняют и `датами рождения`:

```sql
USE HumanFriends;

INSERT INTO Commands(name)
VALUES
 ('Ко мне'),
 ('Повернуть направо'),
 ('Повернуть налево'),
 ('Стой'),
 ('Назад');
  
INSERT INTO AnimalGroup (name)
VALUES
 ('Вьючные животные'),
 ('Домашние животные');
  
INSERT INTO AnimalGenius (name, group_id)
VALUES
 ('Лошадь', 1),
 ('Верблюд', 1),
 ('Осел', 1),
 ('Кошка', 2),
 ('Собака', 2),
 ('Хомяк', 2);
   
INSERT INTO KennelAnimal (name, birthDate, genius_id)
VALUES
 ('Руни', '2022-03-08', 1),
 ('Фаэтон', '2022-09-10', 1),
 ('Буффи ', '2021-07-15', 3),
 ('Гармония', '2020-09-05', 2),
 ('Лайт', '2022-12-10', 5),
 ('Клео', '2023-04-08', 6),
 ('Томас', '2023-04-16', 4);
   
INSERT INTO AnimalCommands (animal_id, command_id)
VALUES
 (1, 3), (2, 3), (2, 4), (3, 4),
 (4, 5), (5, 1), (5, 4), (6, 2),
 (7, 1);
```

![](./images/2.4.1_task_screenshot.png "Подтверждение выполнения задания 2.4.")
![](./images/2.4.2_task_screenshot.png "Подтверждение выполнения задания 2.4.")
![](./images/2.4.3_task_screenshot.png "Подтверждение выполнения задания 2.4.")
![](./images/2.4.4_task_screenshot.png "Подтверждение выполнения задания 2.4.")
![](./images/2.4.5_task_screenshot.png "Подтверждение выполнения задания 2.4.")

</details>

<details>
<summary><b>2.5.</b></summary>

Объединяем таблицы `лошади` и `ослы` в одну таблицу, удалив из таблицы `верблюдов`, так как верблюдов решили перевезти в другой питомник на зимовку:

```sql
USE HumanFriends;
DELETE FROM KennelAnimal WHERE genius_id = 2;

CREATE TABLE HorseAndDonkey AS
SELECT * from KennelAnimal WHERE genius_id = 1
UNION
SELECT * from KennelAnimal WHERE genius_id = 3;
```

![](./images/2.5.1_task_screenshot.png "Подтверждение выполнения задания 2.5.")
![](./images/2.5.2_task_screenshot.png "Подтверждение выполнения задания 2.5.")

</details>

<details>
<summary><b>2.6.</b></summary>

Создаем новую таблицу `молодые животные` в которую попадут все животные старше `1` года, но младше `3` лет и в отдельном столбце с точностью до месяца подсчитать возраст животных в новой таблице:

```sql
USE HumanFriends;
CREATE TABLE YoungAnimals AS
SELECT id, name, birthDate, 
datediff(curdate(),birthDate) DIV 31 as age, genius_id 
from KennelAnimal 
WHERE date_add(birthDate, INTERVAL 1 YEAR) < curdate() 
AND date_add(birthDate, INTERVAL 3 YEAR) > curdate();
```

![](./images/2.6_task_screenshot.png "Подтверждение выполнения задания 2.6.")

</details>

<details>
<summary><b>2.7.</b></summary>

Объединяем все таблицы в одну, при этом сохраняя поля, указывающие на прошлую принадлежность к старым таблицам:

```sql
USE HumanFriends;
CREATE TABLE CombinedAnimals
(
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(30),
    birthDate DATE,
    age INT,
    genius_id INT,
    source_table VARCHAR(30)
);
```

```sql
INSERT INTO CombinedAnimals (name, birthDate, age, genius_id, source_table)
SELECT name, birthDate, age, genius_id, 'YoungAnimals' FROM YoungAnimals;

INSERT INTO CombinedAnimals (name, birthDate, age, genius_id, source_table)
SELECT name, birthDate, NULL, genius_id, 'AnimalGenius' FROM AnimalGenius;

INSERT INTO CombinedAnimals (name, birthDate, age, genius_id, source_table)
SELECT name, NULL, NULL, id, 'AnimalGroup' FROM AnimalGroup;

INSERT INTO CombinedAnimals (name, birthDate, age, genius_id, source_table)
SELECT name, NULL, NULL, id, 'Commands' FROM Commands;

INSERT INTO CombinedAnimals (name, birthDate, age, genius_id, source_table)
SELECT name, birthDate, NULL, genius_id, 'HorseAndDonkey' FROM HorseAndDonkey;

INSERT INTO CombinedAnimals (name, birthDate, age, genius_id, source_table)
SELECT name, birthDate, NULL, genius_id, 'KennelAnimal' FROM KennelAnimal;
```

![](./images/2.7_task_screenshot.png "Подтверждение выполнения задания 2.7.")

</details>

### 3. Заключительное задание итоговой aттecтaции

<details>
<summary><b>Класс Main</b></summary>

Основной класс программы, содержащий метод `main()`, который запускает приложение. В этом классе создаются экземпляры классов `KennelAccounting`, `ConsoleView` и `KennelStorage`, а также осуществляется взаимодействие между ними.

</details>

<details>
<summary><b>Класс KennelAccounting</b></summary>

Контроллер, отвечающий за обработку пользовательского ввода, выполнение операций над данными и вызов методов для отображения результатов в пользовательском интерфейсе.

</details>

<details>
<summary><b>Класс ConsoleView</b></summary>

Отвечает за представление данных в консоли. Реализует интерфейс `View`, имеет методы для отображения информации о животных и их навыках, а также вывода сообщений об ошибках и результатов операций.

</details>

<details>
<summary><b>Класс KennelStorage</b></summary>

Отвечает за хранение и управление данными о животных. Реализует интерфейс `Storage`, предоставляет методы для добавления, удаления и т.д.

</details>

<details>
<summary><b>Интерфейс View</b></summary>

Cодержит объявления методов для представления данных в пользовательском интерфейсе.

</details>

<details>
<summary><b>Класс Counter</b></summary>

Утилитный класс, используемый для подсчета количества экземпляров животных.

</details>

<details>
<summary><b>Интерфейс Storage</b></summary>

Cодержит объявления методов для управления данными о животных.

</details>

<details>
<summary><b>Классы Camel, Cat, Dog, Donkey, Hamster и Horse</b></summary>

Представляют различные виды животных. Каждый из них наследуется от соответствующего абстрактного класса `AbstractPet` или `AbstractPackAnimal` и реализует интерфейс `AnimalGenius`.

</details>

<details>
<summary><b>Класс AbstractAnimal</b></summary>

Абстрактный класс, содержащий общую информацию и методы для всех видов животных.

</details>

<details>
<summary><b>Класс AbstractPackAnimal</b></summary>

Абстрактный класс, наследуется от `AbstractAnimal` и содержит дополнительные поля и методы для животных.

</details>

<details>
<summary><b>Класс AbstractPet</b></summary>

Абстрактный класс, наследуется от `AbstractAnimal` и содержит дополнительные поля и методы для домашних животных.

</details>

<details>
<summary><b>Интерфейс AnimalGenius</b></summary>

Cодержит объявления методов, которые должны быть реализованы каждым видом животного, такие как получение информации о навыках животного.

</details>

<details>
<summary><b>Класс Skill</b></summary>

Представляет собой навык, который может быть связан с животным.

</details>

## 🟫 Git

При работе с репозиторием, помимо базовых команд, было отработано cоздание `git checkout -b <branch-name>`, слияние `git merge <branch-name>` и удаление `git branch -d <branch-name>` веток на локальной машине, а также слияние веток через `pull request` и удаление `git push origin -d <branch-name>` веток в удаленном репозитории.
