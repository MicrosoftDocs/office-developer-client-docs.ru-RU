---
title: Свойство Workspace. Type (DAO)
TOCTitle: Type Property
ms:assetid: 89e59280-d2cd-b6a2-16c5-9f14f42fdd99
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197086(v=office.15)
ms:contentKeyID: 48546177
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e698963d60809e8d88c4ff87532fb7b74cff275c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311307"
---
# <a name="workspacetype-property-dao"></a>Свойство Workspace. Type (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое указывает операционный тип или тип данных объекта. Только для чтения, **Integer**.

## <a name="syntax"></a>Синтаксис

*Expression* . Тип

*expression*: переменная, представляющая объект **Workspace**.

## <a name="remarks"></a>Замечания

Для объекта **Workspace** возможны следующие параметры и возвращаемые значения.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Тип рабочей области</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Дбусежет</strong></p></td>
<td><p><strong>Рабочая область</strong> подключена к ядру СУБД Microsoft Access.</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбусеодбк</strong></p></td>
<td><p><strong>Рабочая область</strong> подключена к источнику данных ODBC.</p></td>
</tr>
</tbody>
</table>

