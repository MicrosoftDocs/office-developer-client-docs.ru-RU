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

Служба курсоров Майкрософт для OLE DB дополняет курсором функции поддержки поставщиков данных. В результате пользователь получает относительно однородные функции от всех поставщиков данных.

Служба курсоров делает динамические свойства доступными и улучшает поведение определенных методов. Например, [динамическое](optimize-property-dynamic-ado.md) свойство Optimize позволяет создавать временные индексы для упрощения определенных операций, таких как метод [Find.](find-method-ado.md)

Служба курсоров обеспечивает поддержку пакетного обновления во всех случаях. Он также имитирует более способные типы курсоров, такие как динамические курсоры, когда поставщик данных может предоставить только менее способные курсоры, такие как статические курсоры.

## <a name="keyword"></a>Ключевое слово

Чтобы вызвать этот компонент службы, задайте свойству [Recordset](recordset-object-ado.md) или [Connection](connection-object-ado.md) [объекта CursorLocation](cursorlocation-property-ado.md) свойство **adUseClient.**

`connection.CursorLocation=adUseClientrecordset.CursorLocation=adUseClient`

## <a name="dynamic-properties"></a>Динамические свойства

При вызове службы курсора для OLE DB в коллекцию свойств объекта **Recordset** добавляются следующие [динамические](properties-collection-ado.md) свойства. Полный список динамических свойств **объекта Connection** и **Recordset** указан в индексе [динамических свойств ADO.](ado-dynamic-property-index.md) При необходимости связанные имена свойств OLE DB включаются в скобки после имени свойства ADO.

Изменения некоторых динамических свойств не видны основному источнику данных после вызова службы курсора. Например, установка свойства *"Время простоя* команды" в **наборе записей** не будет видна для поставщика данных, находящегося в основе.

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

Если вашему приложению требуется служба курсора, но вам необходимо настроить динамические свойства для поставщика, установите свойства перед тем, как вызовет службу курсора. Параметры свойства командного объекта всегда передаются поставщику данных, независимо от расположения курсора. Таким образом, вы также можете использовать объект команды, чтобы в любое время установить свойства.

> [!NOTE]
> Динамическое DBPROP_SERVERDATAONINSERT не поддерживается службой курсора, даже если оно поддерживается поставщиком данных.



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
<td><p>Автоматический пересчет<br />
(DBPROP_ADC_AUTORECALC)</p></td>
<td><p>Для наборов записей, созданных с помощью службы формирования данных, это значение указывает, как часто вычисляются и агрегируются столбцы. Значение по умолчанию (значение=1) пересчитывалось каждый раз, когда служба формирования данных определяет, что значения изменились. Если значение — 0, вычисляются или агрегируются столбцы только при первоначальной построении иерархии.</p></td>
</tr>
<tr class="even">
<td><p>Размер пакета<br />
(DBPROP_ADC_BATCHSIZE)</p></td>
<td><p>Указывает количество пакетных отчетов об обновлении перед их отправлением в хранилище данных. Чем больше заявлений в пакете, тем меньше круговой передачи в хранилище данных.</p></td>
</tr>
<tr class="odd">
<td><p>Кэш child Rows<br />
(DBPROP_ADC_CACHECHILDROWS)</p></td>
<td><p>Для наборов записей, созданных с помощью службы формирования данных, это значение указывает, хранятся ли эти наборы в кэше для использования в дальнейшем.</p></td>
</tr>
<tr class="even">
<td><p>Версия курсора<br />
(DBPROP_ADC_CEVER)</p></td>
<td><p>Указывает используемую версию службы курсора.</p></td>
</tr>
<tr class="odd">
<td><p>Обслуживание состояния изменения<br />
(DBPROP_ADC_MAINTAINCHANGESTATUS)</p></td>
<td><p>Указывает текст команды, используемой для повторной синхронизации одной или нескольких строк в многосторонном подмосковном окне.</p></td>
</tr>
<tr class="even">
<td><p><a href="optimize-property-dynamic-ado.md">Оптимизация</a></p></td>
<td><p>Указывает, следует ли создать индекс. Если за <strong>установлено true,</strong>авторизирует временное создание индексов для улучшения выполнения определенных операций.</p></td>
</tr>
<tr class="odd">
<td><p><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></p></td>
<td><p>Указывает имя <strong>recordset</strong>. На них можно ссылаться в текущих или последующих командах формирования данных.</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-command-property-dynamic-ado.md">Resync Command</a></p></td>
<td><p>Указывает настраиваемую строку команд, которая используется методом <a href="resync-method-ado.md">Resync,</a> когда действует свойство <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table.</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальный каталог</a></p></td>
<td><p>Указывает имя базы данных, содержащей таблицу, указанную в <strong>свойстве Unique Table.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальная схема</a></p></td>
<td><p>Указывает имя владельца таблицы, на который ссылается свойство <strong>Unique Table.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальная таблица</a></p></td>
<td><p>Указывает имя одной таблицы в наборе <strong>записей,</strong> созданном из нескольких таблиц, которые можно изменить путем вставки, обновления или удаления.</p></td>
</tr>
<tr class="even">
<td><p>Условия обновления<br />
(DBPROP_ADC_UPDATECRITERIA)</p></td>
<td><p>Указывает, какие поля в предложении <strong>WHERE</strong> используются для обработки столкновений, происходящих во время обновления.</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</p></td>
<td><p>Указывает, вызывается ли метод <strong>Resync</strong> неявно после метода <a href="updatebatch-method-ado.md">UpdateBatch</a> (и его поведения), когда действует свойство <strong>Unique Table.</strong></p></td>
</tr>
</tbody>
</table>


Вы также можете задать или получить динамическое свойство, указав его имя в качестве индекса для **коллекции свойств.** Например, получите и распечатайте текущее значение динамического свойства [Optimize,](optimize-property-dynamic-ado.md) а затем установите новое значение, например:

```vb 
 
Debug.Print rs.Properties("Optimize") 
rs.Properties("Optimize") = True 
```

## <a name="built-in-property-behavior"></a>Встроенное поведение свойства

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
<td><p>Дополняет типы курсоров, доступные для <strong>recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>Дополняет типы блокировок, доступных для <strong>recordset.</strong> Включает пакетные обновления.</p></td>
</tr>
<tr class="odd">
<td><p><a href="sort-property-ado.md">Sort</a></p></td>
<td><p>Указывает одно или несколько имен <strong></strong> полей, по которых сортируется набор записей, и указывает, сортирует ли каждое поле по возрастанию или убыванию.</p></td>
</tr>
</tbody>
</table>


## <a name="method-behavior"></a>Поведение метода

Служба курсоров для OLE DB включает или влияет на поведение метода [Append](field-object-ado.md) объекта [Field;](append-method-ado.md) и методы **Open,** [](open-method-ado-recordset.md) [Resync,](resync-method-ado.md) [UpdateBatch](updatebatch-method-ado.md)и Save объекта [Recordset.](save-method-ado.md)

