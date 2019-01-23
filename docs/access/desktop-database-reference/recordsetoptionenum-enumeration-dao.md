---
title: Перечисление RecordsetOptionEnum (DAO)
TOCTitle: RecordsetOptionEnum Enumeration
ms:assetid: 3a9d8664-dcb6-cb60-7cf6-e229eb699ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192649(v=office.15)
ms:contentKeyID: 48544266
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: b9e2a69f6952feb892de736e7ff3c3ca94e9da64
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717281"
---
# <a name="recordsetoptionenum-enumeration-dao"></a>Перечисление RecordsetOptionEnum (DAO)


**Область применения**: Access 2013, Office 2013

Используется с методом **OpenRecordset** для указания характеристик нового объекта **Recordset**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbAppendOnly</p></td>
<td><p>8</p></td>
<td><p>Дает пользователю возможность добавлять новые записи в динамическое подмножество данных, но запрещает ему чтение существующих записей.</p></td>
</tr>
<tr class="even">
<td><p>dbConsistent</p></td>
<td><p>32</p></td>
<td><p>Применяет обновления только к тем полям, которые не окажут влияния на другие записи в динамическом подмножестве данных (только для типов "динамическое подмножество данных" и "моментальный снимок").</p></td>
</tr>
<tr class="odd">
<td><p>dbDenyRead</p></td>
<td><p>2</p></td>
<td><p>Запрещает другим пользователям чтение записей объекта Recordset (только для табличного типа).</p></td>
</tr>
<tr class="even">
<td><p>dbDenyWrite</p></td>
<td><p>1</p></td>
<td><p>Запрещает другим пользователям изменять записи объекта Recordset.</p></td>
</tr>
<tr class="odd">
<td><p>dbExecDirect</p></td>
<td><p>2048</p></td>
<td><p>Выполняет запрос, не вызывая перед этим функцию ODBC SQLPrepare.</p></td>
</tr>
<tr class="even">
<td><p>dbFailOnError</p></td>
<td><p>128</p></td>
<td><p>Откатывает обновления при возникновении ошибки.</p></td>
</tr>
<tr class="odd">
<td><p>dbForwardOnly</p></td>
<td><p>256</p></td>
<td><p>Создает объект Recordset типа "моментальный снимок" с прокруткой только вперед (только для типа "моментальный снимок").</p></td>
</tr>
<tr class="even">
<td><p>dbInconsistent</p></td>
<td><p>16</p></td>
<td><p>Применяет обновления ко всем полям динамического подмножества данных, даже если это повлияет на другие записи (только для типов "динамическое подмножество данных" и "моментальный снимок").</p></td>
</tr>
<tr class="odd">
<td><p>dbReadOnly</p></td>
<td><p>4</p></td>
<td><p>Открывает объект Recordset только для чтения.</p></td>
</tr>
<tr class="even">
<td><p>dbRunAsync</p></td>
<td><p>1024</p></td>
<td><p>Выполняет запрос асинхронно.</p></td>
</tr>
<tr class="odd">
<td><p>dbSeeChanges</p></td>
<td><p>512</p></td>
<td><p>Создает ошибку во время выполнения, если другой пользователь пытается изменить данные, которые вы редактируете (только для типа "динамическое подмножество данных").</p></td>
</tr>
<tr class="even">
<td><p>dbSQLPassThrough</p></td>
<td><p>64</p></td>
<td><p>Отправляет инструкцию SQL в базу данных ODBC (только для типа "моментальный снимок").</p></td>
</tr>
</tbody>
</table>

