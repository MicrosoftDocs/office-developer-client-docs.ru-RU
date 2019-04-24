---
title: Свойство Recordset. Type (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a55af8aaa5cfb3d87e13125871a6ccbe1e7f2dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307555"
---
# <a name="recordsettype-property-dao"></a>Свойство Recordset. Type (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое указывает операционный тип или тип данных объекта. Только для чтения, **Integer**.

## <a name="syntax"></a>Синтаксис

*Expression* . Тип

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

Для объекта **Recordset** возможны следующие параметры и возвращаемые значения.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Тип набора записей</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbOpenTable</strong></p></td>
<td><p>Таблица (только для рабочих областей Microsoft Access)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbOpenDynamic</strong></p></td>
<td><p>Dynamic (только для рабочих областей ODBCDirect)</p>
<p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbOpenDynaset</strong></p></td>
<td><p>Типа dynaset</p></td>
</tr>
<tr class="even">
<td><p><strong>dbOpenSnapshot</strong></p></td>
<td><p>Статически</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbOpenForwardOnly</strong></p></td>
<td><p>Только вперед</p></td>
</tr>
</tbody>
</table>

