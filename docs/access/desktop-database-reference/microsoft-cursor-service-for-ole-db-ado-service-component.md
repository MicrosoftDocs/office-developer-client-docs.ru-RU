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

Служба Microsoft Cursor для OLE DB дополняет функции поддержки курсоров поставщиков данных. В результате пользователь воспринимает относительно однородные функции всех поставщиков данных.

Служба Cursor делает динамические свойства доступными и улучшает поведение определенных методов. Например, [динамическое](optimize-property-dynamic-ado.md) свойство Оптимизируйте позволяет создавать временные индексы для облегчения определенных операций, например метода [Find.](find-method-ado.md)

Служба Cursor во всех случаях поддерживает пакетное обновление. Он также имитирует более способные типы курсоров, например динамические курсоры, когда поставщик данных может поставлять только менее способные курсоры, например статические курсоры.

## <a name="keyword"></a>Ключевое слово

Чтобы вызвать этот компонент службы, [](connection-object-ado.md) установите свойство [CursorLocation](cursorlocation-property-ado.md) объекта [Recordset](recordset-object-ado.md) или Connection **в adUseClient.**

`connection.CursorLocation=adUseClientrecordset.CursorLocation=adUseClient`

## <a name="dynamic-properties"></a>Dynamic Properties

При вызове службы cursor для OLE DB в коллекцию Свойств объекта **Recordset** добавляются следующие [динамические](properties-collection-ado.md) свойства. Полный список динамических свойств **объектов Подключения** и **Recordset** указан в [индексе динамического свойства ADO.](ado-dynamic-property-index.md) Соответствующие имена свойств OLE DB, если это необходимо, включаются в скобки после имени свойства ADO.

Изменения некоторых динамических свойств не видны основному источнику данных после вызова службы Cursor. Например, установка свойства *Командное время в* **наборе записей** не будет видна основному поставщику данных.

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

Если вашему приложению требуется служба Cursor, но вам необходимо установить динамические свойства на основном поставщике, установите свойства перед обращением к службе Cursor. Параметры свойства объектов команд всегда передаются основному поставщику данных независимо от расположения курсора. Таким образом, вы также можете использовать объект команды для набора свойств в любое время.

> [!NOTE]
> Динамическое свойство DBPROP_SERVERDATAONINSERT не поддерживается службой курсоров, даже если она поддерживается поставщиком данных.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя свойства</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Автоматический пересчет<br />
(DBPROP_ADC_AUTORECALC)</p></td>
<td><p>Для записей, созданных с помощью службы формирования данных, это значение указывает, как часто вычисляются и вычисляются совокупные столбцы. По умолчанию (значение=1) необходимо пересчитать каждый раз, когда служба формирования данных определяет, что значения изменились. Если значение 0, вычисляются или совокупные столбцы вычисляются только при первоначальном построении иерархии.</p></td>
</tr>
<tr class="even">
<td><p>Размер пакета<br />
(DBPROP_ADC_BATCHSIZE)</p></td>
<td><p>Указывает количество заявлений об обновлении, которые можно пакетно отправить перед отправлением в хранилище данных. Чем больше заявлений в пакете, тем меньше поездок в хранилище данных.</p></td>
</tr>
<tr class="odd">
<td><p>Детские строки кэша<br />
(DBPROP_ADC_CACHECHILDROWS)</p></td>
<td><p>Для наборов записей, созданных службой формирования данных, это значение указывает, хранятся ли детские записи в кэше для более позднего использования.</p></td>
</tr>
<tr class="even">
<td><p>Версия двигателя cursor<br />
(DBPROP_ADC_CEVER)</p></td>
<td><p>Указывает версию используемой службы Cursor.</p></td>
</tr>
<tr class="odd">
<td><p>Сохранение состояния изменений<br />
(DBPROP_ADC_MAINTAINCHANGESTATUS)</p></td>
<td><p>Указывает текст команды, используемой для повторной синхронизации одной или нескольких строк в нескольких таблицах.</p></td>
</tr>
<tr class="even">
<td><p><a href="optimize-property-dynamic-ado.md">Оптимизация</a></p></td>
<td><p>Указывает, следует ли создавать индекс. При наборе <strong>True</strong>разрешает временное создание индексов для улучшения выполнения определенных операций.</p></td>
</tr>
<tr class="odd">
<td><p><a href="reshape-name-property-dynamic-ado.md">Переописываю имя</a></p></td>
<td><p>Указывает имя <strong>recordset</strong>. Можно ссылаться в текущих или последующих командах формирования данных.</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-command-property-dynamic-ado.md">Команда Resync</a></p></td>
<td><p>Указывает настраиваемую строку команд, которая используется методом <a href="resync-method-ado.md">Resync,</a> когда свойство <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a> действует.</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальный каталог</a></p></td>
<td><p>Указывает имя базы данных, содержащей таблицу, указанную в <strong>свойстве Unique Table.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальная схема</a></p></td>
<td><p>Указывает имя владельца таблицы, ссылаясь на свойство <strong>Unique Table.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальная таблица</a></p></td>
<td><p>Указывает имя одной таблицы в наборе <strong>записей,</strong> созданных из нескольких таблиц, которые могут изменяться вставки, обновления или удаления.</p></td>
</tr>
<tr class="even">
<td><p>Критерии обновления<br />
(DBPROP_ADC_UPDATECRITERIA)</p></td>
<td><p>Указывает, какие поля в пункте <strong>WHERE</strong> используются для обработки столкновений, происходящих во время обновления.</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-resync-property-dynamic-ado.md">Обновление Resync</a>(DBPROP_ADC_UPDATERESYNC)</p></td>
<td><p>Указывает, вызывается ли метод <strong>Resync</strong> неявно после метода <a href="updatebatch-method-ado.md">UpdateBatch</a> (и его поведения), когда свойство <strong>Unique Table</strong> действует.</p></td>
</tr>
</tbody>
</table>


Вы также можете задать или получить динамическое свойство, указав его имя в качестве индекса для коллекции **Свойств.** Например, получите и распечатайте текущее значение динамического свойства Оптимизируйте, а затем установите новое значение, например: [](optimize-property-dynamic-ado.md)

```vb 
 
Debug.Print rs.Properties("Optimize") 
rs.Properties("Optimize") = True 
```

## <a name="built-in-property-behavior"></a>Встроенное поведение свойств

Служба cursor для OLE DB также влияет на поведение определенных встроенных свойств.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя свойства</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>Дополняет типы курсоров, доступные для <strong>Recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>Дополняет типы замков, доступных для <strong>recordset.</strong> Включает пакетные обновления.</p></td>
</tr>
<tr class="odd">
<td><p><a href="sort-property-ado.md">Sort</a></p></td>
<td><p>Указывает одно или несколько имен полей, в которых сортируется <strong>Набор</strong> записей, и отсортирует ли каждое поле в порядке по возрастанию или убыванию.</p></td>
</tr>
</tbody>
</table>


## <a name="method-behavior"></a>Поведение метода

Служба cursor для OLE DB включает или [](field-object-ado.md) влияет на поведение метода приложения объекта [Field;](append-method-ado.md) и методы **Open,** [](open-method-ado-recordset.md) [Resync,](resync-method-ado.md)UpdateBatch и Save объекта [Recordset.](updatebatch-method-ado.md) [](save-method-ado.md)

