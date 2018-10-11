---
title: Microsoft Cursor Service for OLE DB (ADO Service Component)
TOCTitle: Microsoft Cursor Service for OLE DB (ADO Service Component)
ms:assetid: 6818fc05-9c9f-9b67-07d2-e622c93133c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249405(v=office.15)
ms:contentKeyID: 48545376
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 175023f12d1efa23422afb15e693d44976421cc0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480602"
---
# <a name="microsoft-cursor-service-for-ole-db-ado-service-component"></a>Microsoft Cursor Service for OLE DB (ADO Service Component)


**Применимо к**: Access 2013 | Office 2013

Служба курсора для OLE DB дополняет функции поддержки курсора поставщиков данных. В результате пользователь понимает относительно универсальный код функции из всех поставщиков данных.

Служба курсора доступны динамические свойства и расширяет поведение некоторых методов. К примеру динамическое свойство [оптимизировать](optimize-property-dynamic-ado.md) позволяет создавать временных индексов для облегчения определенные операции, такие как метод [поиска](find-method-ado.md) .

Служба курсора обеспечивает поддержку для пакетного обновления во всех случаях. Также более производительные курсора типов, таких как динамические курсоры моделирует, когда поставщик данных может поддерживать только менее производительные курсоры, такие как статические курсоры.

## <a name="keyword"></a>Keyword

Чтобы вызвать этот компонент службы, свойства объекта [записей](recordset-object-ado.md) или [подключения к](connection-object-ado.md) [CursorLocation](cursorlocation-property-ado.md) значение **adUseClient**.

`connection.CursorLocation=adUseClientrecordset.CursorLocation=adUseClient`

## <a name="dynamic-properties"></a>Динамические свойства

При вызове служба курсора для OLE DB следующие динамические свойства добавляются в коллекцию [свойств](properties-collection-ado.md) объекта **набора записей** . Полный список динамических свойств объекта **подключения** и **записей** отображается в [ADO динамических свойство индекса](ado-dynamic-property-index.md). Связанные имена свойств OLE DB, при необходимости включаются в скобках после имени свойства ADO.

Изменения в некоторые динамические свойства не видны в источнике данных после выполнялся вызов службы курсора. Например задание свойства *Команда времени ожидания* для **набора записей** будет недоступен для базового поставщика данных.

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

Если приложения требуются службы курсора, но необходимо задать динамические свойства в базовом поставщика, задайте свойства до вызова службы курсора. Параметры свойства объекта команды, всегда передаются базового поставщика данных, независимо от расположения курсора. Таким образом можно также использовать объект команды для установки свойств в любое время.

> [!NOTE]
> Свойство DBPROP_SERVERDATAONINSERT не поддерживается службой курсора, даже в том случае, если он поддерживается базового поставщика данных.



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
<td><p>Автоматическое обновление ссылок<br />
(DBPROP_ADC_AUTORECALC)</p></td>
<td><p>Для наборов записей, созданных с помощью служба формирования данных, это значение указывает, как часто рассчитываются столбцы вычисляемые и статистической обработки. Значение по умолчанию (значение = 1) — для пересчета каждый раз, когда служба формирования данных определяет, что значения были изменены. Если значение равно 0, вычисляемых или статистической обработки столбцов рассчитываются только при построенных иерархии.</p></td>
</tr>
<tr class="even">
<td><p>Размер пакета<br />
(DBPROP_ADC_BATCHSIZE)</p></td>
<td><p>Показывает, сколько инструкций update, которые могут быть помещены в пакет перед отправкой в хранилище данных. Дополнительные инструкции в пакете, хранить меньшее количество обращений к данным.</p></td>
</tr>
<tr class="odd">
<td><p>Кэш дочерних строк<br />
(DBPROP_ADC_CACHECHILDROWS)</p></td>
<td><p>Для наборов записей, созданных с помощью службы формирования данных это значение указывает ли наборы дочерних записей хранятся в кэше для дальнейшего использования.</p></td>
</tr>
<tr class="even">
<td><p>Версия модуля текущей позиции<br />
(DBPROP_ADC_CEVER)</p></td>
<td><p>Указывает версию используемой службой курсора.</p></td>
</tr>
<tr class="odd">
<td><p>Обслуживание изменений состояния<br />
(DBPROP_ADC_MAINTAINCHANGESTATUS)</p></td>
<td><p>Указывает текст команды, используемой для повторной синхронизации одна или несколько строк в нескольких присоединиться к таблице.</p></td>
</tr>
<tr class="even">
<td><p><a href="optimize-property-dynamic-ado.md">Оптимизация</a></p></td>
<td><p>Указывает, должен быть создан индекс. Если параметр имеет значение <strong>True</strong>, авторизует временные создание индексов для улучшения выполнение определенных операций.</p></td>
</tr>
<tr class="odd">
<td><p><a href="reshape-name-property-dynamic-ado.md">Изменить форму имя</a></p></td>
<td><p>Указывает имя <strong>набора записей</strong>. Возможно, на который указывает ссылка в текущем или последующих, формирования команд данных.</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-command-property-dynamic-ado.md">Команда синхронизации</a></p></td>
<td><p>Указывает строку пользовательской команды, используемый с помощью метода <a href="resync-method-ado.md">выполнить повторную синхронизацию</a> , если свойство <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальной таблицы</a> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальный каталога</a></p></td>
<td><p>Указывает имя базы данных, содержащий таблицу, указанный в свойстве <strong>Уникальной таблицы</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальный схемы</a></p></td>
<td><p>Указывает имя владельца таблицы, указанный в свойстве <strong>Уникальной таблицы</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальная таблица</a></p></td>
<td><p>Указывает, что имя одной таблицы в <strong>набор записей</strong> , созданного из нескольких таблиц, которые можно изменить путем вставки, обновления или удаления.</p></td>
</tr>
<tr class="even">
<td><p>Обновление критериев<br />
(DBPROP_ADC_UPDATECRITERIA)</p></td>
<td><p>Указывает, какие поля в предложения <strong>WHERE</strong> используются для обработки конфликтов, которые возникают в процессе обновления.</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-resync-property-dynamic-ado.md">Выполнить повторную синхронизацию обновления</a> (DBPROP_ADC_UPDATERESYNC)</p></td>
<td><p>Указывает ли метод <strong>выполнить повторную синхронизацию</strong> неявно вызывается метод <a href="updatebatch-method-ado.md">UpdateBatch</a> (и его поведение), если свойство <strong>Уникальной таблицы</strong> фактически имеет.</p></td>
</tr>
</tbody>
</table>


Можно также задать или получить динамического свойства, указав его имя в качестве индекса в коллекции **свойств** . К примеру получить и печать текущее значение свойства динамической [оптимизировать](optimize-property-dynamic-ado.md) , а затем задать новое значение, следующим образом:

```vb 
 
Debug.Print rs.Properties("Optimize") 
rs.Properties("Optimize") = True 
```

## <a name="built-in-property-behavior"></a>Поведение встроенных свойств

Служба курсора для OLE DB также влияет на поведение некоторых встроенных свойств.

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
<td><p>Дополнения типов курсоров, доступных для <strong>набора записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType для</a></p></td>
<td><p>Текстовое дополнение типах блокировок, доступные для <strong>набора записей</strong>. Позволяет производить пакетную обновлений.</p></td>
</tr>
<tr class="odd">
<td><p><a href="sort-property-ado.md">Sort</a></p></td>
<td><p>Указывает одно или несколько имен полей сортировки <strong>набора записей</strong> , которые ли сортироваться в каждом поле в возрастающем или убывающем порядке.</p></td>
</tr>
</tbody>
</table>


## <a name="method-behavior"></a>Метод поведение

Служба курсора для OLE DB позволяет включать и влияет на поведение метод [Append](append-method-ado.md) объекта [поля](field-object-ado.md) ; и методов [Open](open-method-ado-recordset.md), [выполнить повторную синхронизацию](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md)и [Сохраните](save-method-ado.md) объект **набора записей** .

