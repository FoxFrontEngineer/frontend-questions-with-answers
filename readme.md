# Подбор наиболее частный вопросов на собеседования для фронтэнда с ответами, чтобы освежить память

Пулреквесты с доп. вопросами и ответами приветствуются!

## Общие вопросы о веб-разработке:

- Можете ли пояснить разницу между progressive enhancement и graceful degradation?
	> graceful degradation будет пониматься как отказоустойчивость клиентских веб-интерфейсов.
	> Постепенная деградация может выражаться в возможности работы при отключённом JavaScript, в достаточно аккуратном отображении интерфейса в браузере, не поддерживающем новые свойства CSS3, в адекватном отображении сайта при отключенных изображениях. В каждом из этих случаев работа пользователя с интерфейсом будет в принципе возможна, хотя и не так удобна.

	> Что же такое progressive enhancement? Чаще всего этот термин переводят, как прогрессивное улучшение. Прогрессивное улучшение предполагает, что веб-интерфейсы должны создаваться поэтапно, циклически, от простого к сложному. На каждом из этапов должен получаться законченный веб-интерфейс, который будет лучше, красивее и удобнее предыдущего. Можно сказать, что сейчас таких этапов четыре:
	- «Старый-добрый-HTML»
	- «CSS»
	- «CSS3»
	- «JavaScript»
	> Источник: https://htmlacademy.ru/blog/7-progressive-enhancement

- Объясните, что означает "Семантическая разметка"
	> Семантическая вёрстка, или семантический HTML-код, — это подход к созданию веб-страниц на языке HTML, основанный на использовании HTML-тегов в соответствии с их семантикой (предназначением)[1], а также предполагающий логичную и последовательную иерархию страницы[2][3]. Он противопоставляется подходу, при котором написание HTML-кода определяется внешним видом веб-страницы. Для оформления веб-страниц, написанных в соответствии с семантикой, используются каскадные таблицы стилей (CSS). Стандарт HTML с самого начала включал в себя ряд семантических тегов[4], но большую популярность семантическая вёрстка получила после начала работ над HTML5.

	> Источник: https://ru.wikipedia.org/wiki/Семантическая_вёрстка

- Как можно оптимизировать загрузку внешних ресурсов на странице?
	1. Уменьшите количество HTTP-запросов
	2. Используйте поддомены для параллельного скачивания
	3. Используйте кэш браузера
	4. Используйте CDN для загрузки популярных JavaScript библиотек
	5. Используйте Gzip- сжатие

	> Подробней по каждому пункту: https://habrahabr.ru/post/137239/

- Каково преимущество в подгрузке внешних ресурсов с нескольких доменов?
	> Cогласно спецификации HTTP/1.1 на браузеры накладываются ограничения на количество одновременно загружаемых компонентов сайта, а именно не более 2-х компонентов с одного хоста. Поэтому если на Вашем сайте много графики, то ее лучше вынести на отдельный поддомен или поддомены. Для Вас это будет один и тот же сервер, а для браузера – разные. Чем больше поддоменов Вы создадите, тем больше файлов браузер сможет одновременно загрузить и тем быстрее загрузится вся страница сайта. Вам остается лишь изменить адрес картинок на новый. Очень простой, но действенный способ.

- Назовите три способа уменьшения времени загрузки страницы (воспринимаемого или реального)
	1. Помещайте CSS файлы в начале страницы
	2. Помещайте javascript в конец страницы
	3. Минимизируйте css и javascript
	4. Оптимизируйте ваши изображения
	5. Не масштабируйте изображения

	> Подробней по каждому пункту: https://habrahabr.ru/post/137239/

- Если Вы присоединились к проекту, где для форматирования используются табы, а Вы привыкли использовать пробелы, как Вы поступите?
	> Не спрашивайте, НИКОГДА!!!

- Что такое FOUC (Flash Of Unstyled Content)? Как его избежать?
	> Flash of Unstyled Content (FOUC) – это кратковременное появление неоформленных HTML-элементов в некоторых версиях браузеров – сразу же после создания визуальных элементов и до полного применения стилей CSS.
	> css {display: block} на компонент
	> В <head> инлайнится код, необходимый для показа минимум 600px высоты страницы без загрузки дополнительных стилей.

- Что такое критический путь рендеринга веб-страниц?
	> Критический путь рендеринга – это набор минимально необходимых для начала отрисовки страницы действий, ресурсов и вычислений.
	> Критический путь можно измерять в количестве критических ресурсов, минимальном времени загрузки (измеряется в RTT) и объеме критических ресурсов (в байтах).
	> Для иллюстрации возьмем простейший пример: HTML страницу размером 1 кб без внешних ресурсов. Критический путь будет: 1 ресурс (HTML-документ), 1 RTT (минимально), 1 кб трафика. Однако, таких простых страниц в природе почти не встретить, поэтому покажем, как можно определять критический путь на реальных веб-страницах.

	> Подробней: https://habrahabr.ru/post/262239/

## Вопросы по HTML:

- Для чего нужен doctype и сколько разновидностей Вы можете назвать?
	> Элемент <!DOCTYPE> предназначен для указания типа текущего документа — DTD (document type definition, описание типа документа). Это необходимо, чтобы браузер понимал, как следует интерпретировать текущую веб-страницу, поскольку HTML существует в нескольких версиях, кроме того, имеется XHTML (EXtensible HyperText Markup Language, расширенный язык разметки гипертекста), похожий на HTML, но различающийся с ним по синтаксису. Чтобы браузер «не путался» и понимал, согласно какому стандарту отображать веб-страницу и необходимо в первой строке кода задавать <!DOCTYPE>.

	> HTML 4.01
	> HTML 5
	> XHTML 1.0
	> XHTML 1.1

	> Подробней про то, как указывать теги для определенного Doctype: http://htmlbook.ru/html/%21doctype
	> Хорошая полезная подробная статья: https://habrahabr.ru/post/71364/

- Что такое режим совместимости (Quirks Mode) и стандартный режим (Standards Mode)
	> На сегодняшний день существует три режима отображения, которые используются движками разметки (layout engines) браузеров: режим совместимости (quirks mode), частично стандартный режим (almost standards mode) и стандартный режим (full standards mode). В режиме совместимости (quirks mode), разметка эмулирует нестандартное поведение браузеров Navigator 4 и Internet Explorer 5. Этот режим необходим для поддержки сайтов, созданных до начала широкого применения веб стандартов. В стандартном режиме (full standards mode) поведение браузера соответствует (будем надеяться) описанному в спецификациях HTML и CSS. В частично стандартном режиме (almost standards mode)  реализовано лишь незначительное количество так называемых "странностей" (quirks).

	> Если вы будете пользоваться неполным тегом DOCTYPE, устаревшим его видом, или вообще забудете про него, броузер перейдет в «загадочный» (quirk) режим и будет исходить из предположения, что вы писали код страницы с ошибками и вольно отступали от стандартов, т.е. так, как писали в конце 90-ых годов.  В этом режиме броузер попытается разобрать вашу страницу по правилам обратной совместимости и выведет на экран, например, CSS так, как его вывел бы Internet Explorer 4-ой версии, а DOM будет работать так, как он работал именно в этом броузере (IE переключается в свой старый DOM, а Mozilla и Netscape 6 переключается вообще в бог знает что).

	> Подробней: https://developer.mozilla.org/ru/docs/Web/HTML/Quirks_Mode_and_Standards_Mode
	> Подробней: https://habrahabr.ru/post/71364/

- В чем разница между HTML и XHTML?
	> XHTML - это приложение XML, которое является довольно строгим языком с угловыми скобками.
	> HTML - это приложение SGML, которое является гораздо менее строгим языком с угловой скобкой.
	> (XML также является применением SGML.)

	> При написании кода XHTML придерживаются того же синтаксиса, который характерен для HTML. При этом разница между HTML и XHTML состоит в наборе некоторых обязательных правил.

	> Правила XHTML следующие.

	1. Все теги и их атрибуты должны быть набраны в нижнем регистре (строчными символами).
	2. Значения любых атрибутов необходимо заключать в кавычки.
	3. Требуется закрывать все теги, даже такие, которым не сопоставлен закрывающий тег.
	4. Должна соблюдаться правильная вложенность тегов.
	5. Нельзя использовать сокращенные атрибуты тегов.
	6. Вместо атрибута name следует указывать id.
	7. Следует определять DTD (document type definition, описание типа документа) с помощью элемента <!DOCTYPE>.

	> Подробнее с примерами: http://htmlbook.ru/xhtml/sintaksis-xhtml

- Могут ли возникнуть проблемы при подаче страниц с типом application/xhtml+xml?
	> MIME (Multipurpose Internet Mail Extensions, многоцелевые расширения интернет-почты) — стандарт Интернет, является частью протокола HTTP. Задача MIME это идентификация типа содержимого документа по его заголовку. К примеру, текстовый файл имеет тип text/plain, а HTML-файл — text/html. Отправка заголовка обычно происходит на основе расширения файла веб-сервером.
	> Документы XHTML по умолчанию отправляются как text/html, что в действительности говорит о том, что мы имеем дело с HTML, а не XHTML-файлом. Чтобы задействовать возможности XHTML требуется отдавать файл с типом application/xhtml+xml. Если у вас установлен веб-сервер Apache, то вы можете сделать это через директиву AddType, добавив следующую строку в файл .htaccess, расположенный в корне сайта.
	```AddType application/xhtml+xml .xhtml```
	> В данном случае мы говорим, что все файлы с расширением .xhtml отдавать как application/xhtml+xml. Если документы формируются через PHP, то можно отдавать заголовок следующим образом:
	```header ("Content-type: application/xhtml+xml");```
	> чтите, что эта строка должна идти до вывода любого текста на странице.
	> Браузер Internet Explorer до версии 8.0 включительно не поддерживает тип application/xhtml+xml и не сможет отобразить страницу, которая отдаётся с этим типом. Остальные браузеры, в том числе IE9, понимают этот тип как переход в стандартный режим.
	> Тип application/xhtml+xml необходим в случае, когда в документе применяется MathML (Mathematical Markup Language, язык математической разметки), предназначенный для добавления формул или SVG (Scalable Vector Graphics, масштабируемая векторная графика), язык разметки для создания на странице векторных рисунков. Если вы ничего не знаете об этих технологиях и пока не собираетесь их использовать, лучше отдавать документ как text/html. Это позволит охватить наибольшее количество браузеров и поисковых систем.
	> По сути, тип text/html для файлов с расширением .html или .htm настроен автоматически, поэтому не требуется предпринимать каких-либо действий для этого типа.

	> согласование содержимого для переключения между application/xhtml+xml и text/html так же, как вы описываете, не замечая проблем с поисковыми роботами. Строго говоря, вы должны учитывать значения q в заголовке accept, который указывает предпочтение пользовательского агента к каждому типу контента. Если пользовательский агент предпочитает принимать text/html, но будет принимать application/xhtml+xml в качестве альтернативы, то для обеспечения максимальной безопасности вы должны иметь страницу text/html.

- Как следует оформлять страницу, в которой контент может быть на разных языках?
	> От гугла: https://support.google.com/webmasters/answer/182192?hl=ru

- Чем полезны data- атрибуты?
	> HTML5 спроектирован с возможностью расширения данных ассоциированных с каким-либо элементом, но в то же время не обязательно имеющих определённое значение. data-* атрибуты позволяют хранить дополнительную информацию в стандартных элементах HTML, без хаков вроде нестандартных атрибутов, лишних DOM-свойств или Node.setUserData().

	> Синтаксис HTML

	> Доступ в JavaScript

	> Доступ в CSS