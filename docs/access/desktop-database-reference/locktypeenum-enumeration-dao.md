---
title: LockTypeEnum Enumeration (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f0e12f8d60ee3147eb456df302122a5b7eac684d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879930"
---
# <a name="locktypeenum-enumeration-dao"></a>LockTypeEnum Enumeration (DAO)


**Применимо к**: Access 2013, Office 2013

Указывает тип записи блокировки, используемый при открытии набора записей.

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
<td><p>dbOptimistic</p></td>
<td><p>3</p></td>
<td><p>Оптимистичный параллелизм на основе идентификатора записи. Курсор сравнивает идентификатор записи в старых и новых записей для определения, если изменения были внесены с момента последнего обращения к записи.</p></td>
</tr>
<tr class="even">
<td><p>dbOptimisticBatch</p></td>
<td><p>5</p></td>
<td><p>Позволяет производить пакетную оптимистичный обновлений (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p>dbOptimisticValue</p></td>
<td><p>1</p></td>
<td><p>Оптимистичный параллелизм на основании значения записей. Курсор сравнивает значения данных в старой и новой записи, чтобы определить, если изменения были внесены момента записи последнего к которому предоставляется доступ (технология ODBCDirect рабочие области только).</p>

> [!NOTE]
> <P>Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</P>


</td>
</tr>
<tr class="even">
<td><p>dbPessimistic</p></td>
<td><p>2</p></td>
<td><p>Жесткой одновременно. Курсор использует самый низкий уровень блокировки достаточными для обеспечения можно обновить запись.</p></td>
</tr>
</tbody>
</table>

