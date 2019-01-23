---
title: Перечисление LockTypeEnum (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c2d355e2a16df632d6952802914c1f921b5e9719
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719528"
---
# <a name="locktypeenum-enumeration-dao"></a>Перечисление LockTypeEnum (DAO)


**Область применения**: Access 2013, Office 2013

Указывает тип блокировки записи, используемой при открытии набора записей.

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
<td><p>Оптимистичный параллелизм на основе идентификатора записи. Курсор сравнивает идентификатор записи в старой и новой записях и определяет, были ли внесены изменения с момента последнего доступа к записи.</p></td>
</tr>
<tr class="even">
<td><p>dbOptimisticBatch</p></td>
<td><p>5</p></td>
<td><p>Позволяет выполнять пакетные оптимистичные обновления (только для рабочих областей ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p>dbOptimisticValue</p></td>
<td><p>1</p></td>
<td><p>Оптимистичный параллелизм на основе значений записей. Курсор сравнивает значения данных в старой и новой записях и определяет, были ли внесены изменения с момента последнего доступа к записи (только для рабочих областей ODBCDirect).</p>

> [!NOTE]
> Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Если вам необходим доступ ко внешним источникам данных без использования ядра СУБД Microsoft Access, воспользуйтесь объектами ADO.


</td>
</tr>
<tr class="even">
<td><p>dbPessimistic</p></td>
<td><p>2</p></td>
<td><p>Пессимистичный параллелизм. Курсор использует минимальный уровень блокировки, достаточный для гарантированного обновления записи.</p></td>
</tr>
</tbody>
</table>

