# Celestial_Bodies_Database

Это мини-проект Celestial_Bodies_Database представляет собой базу данных на основе PostgreSQL, которая содержит информацию о галактиках, планетах, кораблях, лунах и звездах. Ниже приведена структура базы данных:

## Таблицы

### Таблица "galaxy"

Таблица "galaxy" содержит информацию о галактиках.

Структура таблицы:
```
CREATE TABLE public.galaxy (
    galaxy_id integer NOT NULL,
    name character varying(30) NOT NULL,
    description text,
    galaxy_age integer,
    galaxy_size integer
);
```

### Таблица "planet"

Таблица "planet" содержит информацию о планетах.

Структура таблицы:
```
CREATE TABLE public.planet (
    planet_id integer NOT NULL,
    name character varying(30),
    description text,
    suitable_for_life boolean NOT NULL,
    star_id integer,
    alien_presence boolean
);
```

### Таблица "ship"

Таблица "ship" содержит информацию о космических кораблях.

Структура таблицы:
```
CREATE TABLE public.ship (
    ship_id integer NOT NULL,
    name character varying(30) NOT NULL,
    ship_speed integer NOT NULL
);
```

### Таблица "moon"

Таблица "moon" содержит информацию о лунах.

Структура таблицы:
```
CREATE TABLE public.moon (
    moon_id integer NOT NULL,
    name character varying(30) NOT NULL,
    description text,
    moon_size integer,
    planet_id integer
);
```

### Таблица "star"

Таблица "star" содержит информацию о звездах.

Структура таблицы:
```
CREATE TABLE public.star (
    star_id integer NOT NULL,
    name character varying(30) NOT NULL,
    star_mass numeric(10,2),
    galaxy_id integer,
    description text
);
```

Это базовая структура Celestial_Bodies_Database. Вы можете использовать эту базу данных для хранения и извлечения информации о различных космических объектах, таких как галактики, планеты, корабли, луны и звезды. Вы можете добавлять, изменять и удалять записи в таблицах с помощью соответствующих операций базы данных.

Более подробную информацию о каждой таблице и их взаимосвязях вы можете получить, изучив исходный код и выполнение запросов в базе данных. Удачи в использовании Celestial_Bodies_Database!
