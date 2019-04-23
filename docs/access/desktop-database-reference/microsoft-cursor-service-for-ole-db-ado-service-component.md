---
title: Служба курсора (Майкрософт) для OLE DB (компонент службы ADO)
TOCTitle: Microsoft Cursor Service for OLE DB (ADO Service Component)
ms:assetid: 6818fc05-9c9f-9b67-07d2-e622c93133c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249405(v=office.15)
ms:contentKeyID: 48545376
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d79d060922c6e7f28209242ebe82821c2ba97bfd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288990"
---
# <a name="microsoft-cursor-service-for-ole-db-ado-service-component"></a>Служба курсора (Майкрософт) для OLE DB (компонент службы ADO)


**Область применения**: Access 2013, Office 2013

Служба курсора Майкрософт для OLE DB дополняет функциональные возможности поставщиков данных поддержкой курсоров. В результате пользователь воспринимает сравнительно единообразные функциональные возможности у всех поставщиков данных.

Служба курсора делает динамические свойства доступными и улучшает поведение определенных методов. Например, динамическое свойство [optimize](optimize-property-dynamic-ado.md) позволяет создавать временные индексы для упрощения определенных операций, например метода [Find](find-method-ado.md) .

Служба курсоров обеспечивает поддержку пакетного обновления во всех случаях. Он также имитирует дополнительные типы курсоров, например динамические курсоры, когда поставщик данных может предоставлять только менее доступные курсоры, например статические курсоры.

## <a name="keyword"></a>Ключевое слово

Чтобы вызвать этот компонент службы, присвойте свойству [CursorLocation](cursorlocation-property-ado.md) объекта [Recordset](recordset-object-ado.md) или объекта [подключения](connection-object-ado.md) значение **адусеклиент**.

`connection.CursorLocation=adUseClientrecordset.CursorLocation=adUseClient`

## <a name="dynamic-properties"></a>Динамические свойства

При вызове службы курсора для OLE DB следующие динамические свойства добавляются в коллекцию [свойств](properties-collection-ado.md) объекта **Recordset** . Полный список динамических свойств **подключения** и объекта **Recordset** указан в динамическом индексе [свойства ADO](ado-dynamic-property-index.md). Соответствующие имена свойств OLE DB, где это уместно, включаются в скобки после имени свойства ADO.

Изменения, внесенные в некоторые динамические свойства, не отображаются в базовом источнике данных после вызова службы курсора. Например, установка свойства *времени ожидания для команды* для объекта **Recordset** не будет отображаться для базового поставщика данных.

```vb 
... 
Recordset1.CursorLocation = adUseClient 'invokes cursor service 
Recordset1.Open "authors", _ 
 "Provider=SQLOLEDB;Data Source=DBServer;User Id=usr;" & _ 
 "Password=pwd;Initial Catalog=pubs;",,adCmdTable 
Recordset1.Properties.Item("Command Time out") = 50 
' 'Command Time out' property on DBServer is still default (30). 
... 

```

Если для приложения требуется служба курсора, но вам нужно задать динамические свойства для базового поставщика, задайте свойства перед вызовом службы курсора. Параметры свойства объекта Command всегда передаются базовому поставщику данных независимо от положения курсора. Таким образом, вы также можете использовать объект Command для задания свойств в любое время.

> [!NOTE]
> Служба курсора ДБПРОП_СЕРВЕРДАТАОНИНСЕРТ не поддерживает динамическое свойство, даже если оно поддерживается базовым поставщиком данных.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя свойства</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Автоматическое перерасчет<br />
(ДБПРОП_АДК_АУТОРЕКАЛК)</p></td>
<td><p>Для наборов записей, созданных с помощью службы формирования данных, это значение указывает, как часто рассчитываются вычисляемые и статистические вычисляемые столбцы. Значение по умолчанию (Value = 1) используется для пересчета, когда служба формирования данных определит, что значения изменились. Если значение равно 0, вычисляемые или статистические столбцы рассчитываются только при первоначальном построении иерархии.</p></td>
</tr>
<tr class="even">
<td><p>Размер пакета<br />
(ДБПРОП_АДК_БАТЧСИЗЕ)</p></td>
<td><p>Указывает количество инструкций UPDATE, которые можно пакетировать перед отправкой в хранилище данных. Чем больше инструкций в пакете, тем меньше обращений к хранилищу данных.</p></td>
</tr>
<tr class="odd">
<td><p>ДоЧерние строки кэша<br />
(ДБПРОП_АДК_КАЧЕЧИЛДРОВС)</p></td>
<td><p>Для наборов записей, созданных с помощью службы формирования данных, это значение указывает, хранятся ли в кэше дочерние наборы записей для последующего использования.</p></td>
</tr>
<tr class="even">
<td><p>Версия обработчика курсора<br />
(ДБПРОП_АДК_ЦЕВЕР)</p></td>
<td><p>Указывает версию используемой службы курсоров.</p></td>
</tr>
<tr class="odd">
<td><p>Ведение состояния изменения<br />
(ДБПРОП_АДК_МАИНТАИНЧАНЖЕСТАТУС)</p></td>
<td><p>Указывает текст команды, используемой для повторной синхронизации одной или нескольких строк в соединении с несколькими таблицами.</p></td>
</tr>
<tr class="even">
<td><p><a href="optimize-property-dynamic-ado.md">Оптимизация</a></p></td>
<td><p>Указывает, следует ли создать индекс. Если задано <strong>значение true, выполняется</strong>авторизация временного создания индексов для оптимизации выполнения определенных операций.</p></td>
</tr>
<tr class="odd">
<td><p><a href="reshape-name-property-dynamic-ado.md">Изменение имени фигуры</a></p></td>
<td><p>Указывает имя объекта <strong>Recordset</strong>. Могут быть указаны в текущих или последующих командах формирования данных.</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-command-property-dynamic-ado.md">Команда Resync</a></p></td>
<td><p>Указывает пользовательскую строку команды, используемую методом <a href="resync-method-ado.md">Resync</a> , когда действует свойство <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">UNIQUE Table</a> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальный каталог</a></p></td>
<td><p>Указывает имя базы данных, содержащей таблицу, на которую ссылается свойство <strong>UNIQUE Table</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальная схема</a></p></td>
<td><p>Указывает имя владельца таблицы, указанной в свойстве <strong>UNIQUE Table</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальная таблица</a></p></td>
<td><p>Указывает имя одной таблицы в <strong>наборе записей</strong> , созданной на основе нескольких таблиц, которые могут быть изменены при вставке, обновлении или удалении.</p></td>
</tr>
<tr class="even">
<td><p>Условия обновления<br />
(ДБПРОП_АДК_УПДАТЕКРИТЕРИА)</p></td>
<td><p>Указывает, какие поля в предложении <strong>WHERE</strong> используются для обработки конфликтов, происходящих во время обновления.</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-resync-property-dynamic-ado.md">Повторная синхронизация обновлений</a> (ДБПРОП_АДК_УПДАТЕРЕСИНК)</p></td>
<td><p>Указывает, является <strong></strong> ли метод Resync неявно вызванным после метода <a href="updatebatch-method-ado.md">UpdateBatch</a> (и его поведения), когда действует свойство <strong>UNIQUE Table</strong> .</p></td>
</tr>
</tbody>
</table>


Вы также можете задать или получить динамическое свойство, указав его имя в качестве индекса для коллекции **свойств** . Например, получите и распечатайте текущее значение динамического свойства [Оптимизация](optimize-property-dynamic-ado.md) , а затем задайте новое значение, как показано ниже:

```vb 
 
Debug.Print rs.Properties("Optimize") 
rs.Properties("Optimize") = True 
```

## <a name="built-in-property-behavior"></a>Поведение встроенного свойства

Служба курсора для OLE DB также влияет на поведение определенных встроенных свойств.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя свойства</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>Дополняет типы курсоров, доступные для объекта <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>Дополняет типы блокировок, доступные для объекта <strong>Recordset</strong>. Включает пакетное обновление.</p></td>
</tr>
<tr class="odd">
<td><p><a href="sort-property-ado.md">Sort</a></p></td>
<td><p>Задает одно или несколько имен полей, по которым сортируется <strong>набор записей</strong> , а также отсортировать каждое поле в возрастающем или убывающем порядке.</p></td>
</tr>
</tbody>
</table>


## <a name="method-behavior"></a>Поведение метода

Служба курсора для OLE DB включает или влияет на поведение метода [append](append-method-ado.md) объекта [field](field-object-ado.md) ; и методы [Open](open-method-ado-recordset.md), Resync, [](resync-method-ado.md) [UpdateBatch](updatebatch-method-ado.md)и [Save](save-method-ado.md) объекта **Recordset** .

