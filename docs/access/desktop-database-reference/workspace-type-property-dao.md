---
title: Свойство Workspace.Type (DAO)
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
# <a name="workspacetype-property-dao"></a>Свойство Workspace.Type (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, указывающее операционный тип или тип данных объекта. Только для чтения, **Integer**.

## <a name="syntax"></a>Синтаксис

*выражение* .Type

*expression*: переменная, представляющая объект **Workspace**.

## <a name="remarks"></a>Заметки

Для объекта **Workspace** возможные параметры и возвращаемые значения:

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
<td><p><strong>dbUseJet</strong></p></td>
<td><p>Workspace <strong>подключена</strong> к яд базы данных Microsoft Access.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbUseODBC</strong></p></td>
<td><p>Workspace <strong>подключена</strong> к источнику данных ODBC.</p></td>
</tr>
</tbody>
</table>

