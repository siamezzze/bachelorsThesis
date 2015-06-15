# Шаблон выпускной работы для студентов направления ФИИТ мехмата ЮФУ

Это официальная версия шаблона для оформления

* курсовой,
* бакалаврской,
* магистерской

работ в [LaTeX](https://ru.wikipedia.org/wiki/LaTeX) для студентов направления ФИИТ [мехмата ЮФУ](http://mmcs.sfedu.ru/).

Шаблон сделан на основе версии, [разработанной А.М.Пеленицыным для студентов мехмата ЮФУ](https://github.com/MMCS-SFEDU/mmcs_sfedu_thesis).

## Использование

Чтобы попробовать этот проект на деле, проще всего пойти на сайт [overleaf.com](http://overleaf.com), создать там новый проект (“Create new paper”) и закачать все файлы нашего проекта в этот проект.

Для сборки проекта на локальном компьютере требуется современный дистрибутив LaTeX, например, [TeX Live](https://www.tug.org/texlive/). Для работы под Windows лучше использовать какую-либо [LaTeX IDE](https://ru.wikipedia.org/wiki/LaTeX#LaTeX-.D1.80.D0.B5.D0.B4.D0.B0.D0.BA.D1.82.D0.BE.D1.80.D1.8B) (в состав TeX Live входит IDE TeXworks). Для работы под Linux можно использовать любой редактор с подсветкой синтаксиса, (желательно) автодополнением и возможностью сборки с помощью `make` по горячей клавише.

## Состав

Большинство файлов проекта содержат достаточно подробные комментарии о своём назначении. 
Дадим краткое описание основных файлов:

* `main.tex`: основной текст работы.

* `SETUP.tex`: информация об авторе и других формальных параметрах работы, в том числе о типе работы (один из трёх типов, перечисленных выше).

* `biblio.bib`: список использованных литературных и электронных источников,
использованных в работе, в формате [BibTeX](https://ru.wikipedia.org/wiki/BibTeX).

* `my_macro.tex`: несколько полезных макросов, которые могут понадобиться для набора текста (стоит с ними ознакомиться).

Кроме того, в корневом каталоге проекта имеются:

* `Makefile`: для упрощения сборки проекта с помощью утилиты [make](https://ru.wikipedia.org/wiki/Make) (или `nmake` из состава Visual Studio). Полезно для тех, кто не использует специализированные IDE.

* `preamble.tex`: преамбула документа. Для базового использования проекта изучение этого файла не требуется.

* Каталог `core` с реализацией базового функционала в файлах:

	* `appearance.tex`: настройка внешнего вида,
	* `title_macro.tex`: настройка титульного листа,
	* `theorem_styles.tex`: определение окружений типа «Определение», «Теорема»…
	
	Для базового использования проекта изучение содержимого этого каталога не требуется. 

* Каталог `img` с иллюстрациями к работе.

## Рекомендации пользователям Windows

1. Скачайте и запустите
	[установщик TeX Live](http://mirror.ctan.org/systems/texlive/tlnet/install-tl-windows.exe).

2. Выберите самый полный вариант установки (Simple install (big) на данный,
	2015 г., момент). Он потребует около 4 Гб, но избавит от дополнительных сложностей.

3. После установки в меню *Пуск*/*Программы* должна появиться группа *TeX Live*. В ней можно открыть одну из двух опций для сборки проекта:
	* TeXworks — очень скромный редактор с возможностью сборки по горячей клавише,
	* TeX Live command-line — командная строка, в ней нужно переместиться в каталог проекта с помощью команды `cd путь` и выполнить команду сборки `make`. После этого в каталоге появится PDF файл.

	Дополнительно к этим вариантам можно установить более продвинутую LaTeX IDE, например, [TeXnicCenter](http://www.texniccenter.org/).
