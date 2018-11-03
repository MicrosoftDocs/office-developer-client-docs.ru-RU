---
title: Перечисление RecordsetOptionEnum (DAO)
TOCTitle: RecordsetOptionEnum Enumeration
ms:assetid: 3a9d8664-dcb6-cb60-7cf6-e229eb699ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192649(v=office.15)
ms:contentKeyID: 48544266
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 75b69adbe8c3851afa33f729a108ac579f84c683
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947142"
---
# <a name="recordsetoptionenum-enumeration-dao"></a>Перечисление RecordsetOptionEnum (DAO)


**Применимо к**: Access 2013, Office 2013

Используется с методом **OpenRecordset** , чтобы указать характеристики объекта **набора записей** .

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
<td><p>Позволяет пользователям добавлять новые записи динамический набор, но не позволяет пользователю читать существующие записи.</p></td>
</tr>
<tr class="even">
<td><p>dbConsistent</p></td>
<td><p>32</p></td>
<td><p>Применяет обновления только для тех полях, которые не влияет на другие записи в динамический набор (динамический набор - и типа только).</p></td>
</tr>
<tr class="odd">
<td><p>dbDenyRead</p></td>
<td><p>2</p></td>
<td><p>Чтение записей набора записей (только типа таблица) не позволяет другим пользователям.</p></td>
</tr>
<tr class="even">
<td><p>dbDenyWrite</p></td>
<td><p>1</p></td>
<td><p>Пользователям запрещается изменение записей набора записей.</p></td>
</tr>
<tr class="odd">
<td><p>dbExecDirect</p></td>
<td><p>2048</p></td>
<td><p>Выполняет запрос без первого вызова функции SQLPrepare ODBC.</p></td>
</tr>
<tr class="even">
<td><p>dbFailOnError</p></td>
<td><p>128</p></td>
<td><p>Откат обновления при возникновении ошибки.</p></td>
</tr>
<tr class="odd">
<td><p>dbForwardOnly</p></td>
<td><p>256</p></td>
<td><p>Создает прокрутки, однонаправленные моментальный снимок тип набора записей (только типа моментальный снимок).</p></td>
</tr>
<tr class="even">
<td><p>dbInconsistent</p></td>
<td><p>16</p></td>
<td><p>Применяет обновления всех полей динамический набор даже в том случае, если другие записи, затронутых (динамический набор - и типа только).</p></td>
</tr>
<tr class="odd">
<td><p>dbReadOnly</p></td>
<td><p>4</p></td>
<td><p>Открывается записей с доступом только для чтения.</p></td>
</tr>
<tr class="even">
<td><p>dbRunAsync</p></td>
<td><p>1024</p></td>
<td><p>Выполняет асинхронный запрос.</p></td>
</tr>
<tr class="odd">
<td><p>dbSeeChanges</p></td>
<td><p>512</p></td>
<td><p>Создает ошибку времени выполнения, если другой пользователь изменение данных редактирования (добавляющий только).</p></td>
</tr>
<tr class="even">
<td><p>dbSQLPassThrough</p></td>
<td><p>64</p></td>
<td><p>Отправляет инструкции SQL в базе данных ODBC (только типа моментальный снимок).</p></td>
</tr>
</tbody>
</table>

