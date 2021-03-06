---
title: Макрокоманда "ЗадатьЗначение"
TOCTitle: SetValue macro action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 6b6f16c22e9265159c73279cfa1b2644adbc0277
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306820"
---
# <a name="setvalue-macro-action"></a>Макрокоманда "ЗадатьЗначение"

**Область применения**: Access 2013, Office 2013

С помощью макрокоманды **ЗадатьЗначение** можно задать значение для поля, элемента управления или свойства в форме (в режиме формы или таблицы) или в отчете Microsoft Access.

> [!NOTE]
> - Чтобы задать значение свойства Access, которое возвращает объект, нельзя использовать макрокоманду **ЗадатьЗначение**.
> - Эта макрокоманда доступна только для доверенных баз данных. 

## <a name="setting"></a>Параметр

Макрокоманда **ЗадатьЗначение** имеет следующие аргументы:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент макрокоманды</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Элемент</strong></p></td>
<td><p>Имя поля, элемента управления или свойства, значение которого вы хотите задать. Введите имя поля, элемента управления или свойства в поле <strong>Элемент</strong> в разделе <strong>Аргументы макрокоманды</strong> области построителя макросов. Следует использовать полный синтаксис в ссылке на этот элемент, например, <em>имя_элемента_управления</em> (для элемента управления в форме или отчете, из которого вызывается макрос) или <strong>Forms</strong>!<em>имя_формы</em>!<em>имя_элемента_управления</em>. Это обязательный аргумент.</p></td>
</tr>
<tr class="even">
<td><p><strong>Выражение</strong></p></td>
<td><p>Выражение, которое Access использует, чтобы задать значение для указанного элемента. Следует всегда использовать полный синтаксис для ссылки на любой объект в выражении. Например, чтобы увеличить значение элемента управления "Зарплата" в форме "Сотрудники" на 10 процентов, следует использовать синтаксис Forms!Сотрудники!Зарплата*1.1. Это обязательный аргумент.</p><p><strong>ПРИМЕЧАНИЕ</strong>. В этом аргументе не следует использовать знак равенства (=) перед выражением. В противном случае Access вычисляет выражение и затем использует полученное значение для этого аргумента. Это может привести к непредвиденным результатам, если выражение является строкой.</p>
<p>Например, если ввести <strong>=&quot;Строка1&quot;</strong> для этого аргумента, Access сначала вычислит выражение как "Строка1". Затем Access будет использовать "Строка1" как выражение в этом аргументе и попытается найти элемент управления или свойство с именем "Строка1" в форме или отчете, из которого вызывался макрос.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> В базе данных Access (MDB или ACCDB) нажмите кнопку **Построить**, чтобы создать выражение для любого из этих аргументов с помощью построителя выражений.

## <a name="remarks"></a>Примечания

Данную макрокоманду можно использовать, чтобы задать значение для поля или элемента управления в форме (в режиме формы или в режиме таблицы) или в отчете. Вы также можете задать значения практически для любого свойства элемента управления, формы или отчета в любом режиме. Чтобы определить, можно ли задать значение конкретного свойства с помощью макроса и в каких режимах это сделать, см. раздел для этого свойства в справке редактора Visual Basic.

Можно также задать значение для поля в базовой таблице формы, даже если форма не содержит элемент управления, привязанный к полю. Используйте для этого синтаксис **Forms**\!*имя_формы*\!*имя_поля* в поле **Элемент**. Вы также можете указать поле в базовой таблице отчета, используя синтаксис **Reports**\!*имя_отчета*\!*имя_поля*, но в отчете должен быть элемент управления, привязанный к этому полю, или на поле должен ссылаться вычисляемый элемент управления в отчете.

Если задать значение элемента управления в форме, макрокоманда **ЗадатьЗначение** не будет запускать для него правила проверки на уровне формы, но если элемент управления является связанным, запускаются правила проверки на уровне таблицы для соответствующего поля. Макрокоманда **ЗадатьЗначение** также вызывает пересчет, который может выполняться не сразу. Чтобы запустить немедленное обновление и принудительно выполнить пересчет, используйте макрокоманду **ОбновитьОбъект**. На значение, заданное в элементе управления с помощью макрокоманды **ЗадатьЗначение**, также не влияет маска ввода, заданная в свойстве **InputMask** элемента управления или соответствующего ему поля.

Изменить значение элемента управления можно с помощью макрокоманды **ЗадатьЗначение** в макросе, который указан в свойстве события **После обновления** элемента управления. Однако с помощью макрокоманды **ЗадатьЗначение** в макросе, указанном в свойстве события **До обновления** элемента управления, невозможно изменить значение для этого элемента управления (хотя с помощью макрокоманды **ЗадатьЗначение** можно изменять значения других элементов управления). Макрокоманду **ЗадатьЗначение** в макросе, который указан в свойствах событий **До обновления** или **После обновления** формы, можно также использовать для изменения значений любых элементов управления в текущей записи.

> [!NOTE]
> С помощью макрокоманды **ЗадатьЗначение** невозможно задать значение для следующих элементов управления:
> - связанных и вычисляемых элементов управления в отчетах;
> - вычисляемых элементов управления в формах.

> [!TIP]
> С помощью макрокоманды **ЗадатьЗначение** можно скрыть или отобразить форму в режиме формы. Введите **Forms**!*имя_формы***.Visible** в поле **Элемент** и **Нет** или **Да** в поле **Выражение**. Если для свойства **Visible** модальной формы задано значение **Нет**, форма скрывается и становится немодальной. Чтобы отобразить форму и снова сделать ее модальной, выберите значение **Да**.

При изменении значения или добавления новых данных в элемент управления с помощью макрокоманды **ЗадатьЗначение** в макросе не запускаются такие события, как **До обновления**, **До вставки** или **Изменение**, которые происходят при изменении или вводе данных в эти элементы управления через пользовательский интерфейс. Эти события также не происходят, если задать значение элемента управления в модуле Visual Basic для приложений (VBA).

Эта макрокоманда недоступна в модуле VBA.  Нужное значение следует задавать непосредственно в VBA.

## <a name="example"></a>Пример

**Установка значения элемента управления с помощью макроса**

Следующий макрос открывает форму "Добавить товары" с помощью кнопки в форме "Поставщики". Он демонстрирует применение макрокоманд **ВыводНаЭкран**, **ЗакрытьОкно**, **ОткрытьФорму**, **ЗадатьЗначение** и **КЭлементуУправления**. Макрокоманда **ЗадатьЗначение** задает в качестве значения элемента управления "Код поставщика" в форме "Товары" текущего поставщика в форме "Поставщики". После этого макрокоманда **КЭлементуУправления** перемещает фокус на поле "Код категории", с которого начинается ввод данных для нового товара. Этот макрос должен быть привязан к кнопке "Добавить товары" в форме "Поставщики".

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Макрокоманда</p></th>
<th><p>Аргументы: параметр</p></th>
<th><p>Примечание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>ВыводНаЭкран</strong></p></td>
<td><p><strong>Включить вывод</strong>: <strong>Нет</strong></p></td>
<td><p>Приостанавливает обновление экрана, пока выполняется макрос.</p></td>
</tr>
<tr class="even">
<td><p><strong>ЗакрытьОкно</strong></p></td>
<td><p><strong>Тип объекта</strong>: <strong>FormObject Имя</strong>: Список товаров <strong>Сохранить</strong>: <strong>Нет</strong></p></td>
<td><p>Закрывает форму "Список товаров".</p></td>
</tr>
<tr class="odd">
<td><p><strong>ОткрытьФорму</strong></p></td>
<td><p><strong>Имя формы</strong>: Товары <strong>Представление</strong>: <strong>FormData Режим</strong>: <strong>AddWindow Режим</strong>: <strong>Обычный</strong></p></td>
<td><p>Открывает форму "Товары".</p></td>
</tr>
<tr class="even">
<td><p><strong>ЗадатьЗначение</strong></p></td>
<td><p><strong>Элемент</strong>: [Forms]![Товары]![КодПоставщика] <strong>Выражение</strong>: КодПоставщика</p></td>
<td><p>Задает в качестве значения элемента управления "КодПоставщика" текущего поставщика в форме "Поставщики".</p></td>
</tr>
<tr class="odd">
<td><p><strong>КЭлементуУправления</strong></p></td>
<td><p><strong>Имя элемента управления</strong>: КодКатегории</p></td>
<td><p>Выполняет переход к элементу управления "КодКатегории".</p></td>
</tr>
</tbody>
</table>

