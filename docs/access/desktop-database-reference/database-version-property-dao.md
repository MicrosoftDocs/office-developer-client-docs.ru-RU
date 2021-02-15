---
title: Свойство Database.Version (DAO)
TOCTitle: Version Property
ms:assetid: 40faaa0c-e764-e968-f606-7e06ded80c3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192887(v=office.15)
ms:contentKeyID: 48544440
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 41b408f63522902fd1d4f806090eef7563a3492a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294654"
---
# <a name="databaseversion-property-dao"></a>Свойство Database.Version (DAO)

**Область применения**: Access 2013, Office 2013

В рабочей области Microsoft Access возвращается замещение ямы баз данных Microsoft Jet или Microsoft Access, которые создали базу данных. Только для чтения, **String**.

## <a name="syntax"></a>Синтаксис

*выражение .* Версия

*выражение*: переменная, представляющая объект **Database**.

## <a name="remarks"></a>Заметки

Возвращаемая величина — это строка, которая оценивается как номер версии, отформатированный следующим образом.

- Рабочее пространство Microsoft Access представляет номер версии в формате *major.minor.* Например, "3.0". Номер версии продукта состоит из номера версии (3), даты и выпуска (0).

В следующей таблице показано, какая версия яда базы данных была включена в различные версии продуктов Майкрософт.

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Database Engine</p></th>
<th><p>Версия (год выпуска)</p></th>
<th><p>Microsoft Access</p></th>
<th><p>Microsoft Visual Basic</p></th>
<th><p>Microsoft Excel</p></th>
<th><p>Microsoft Visual C++</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>1.0 (1992)</p></td>
<td><p>1.0</p></td>
<td><p>Н/Д</p></td>
<td><p>Н/Д</p></td>
<td><p>Н/Д</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Jet</p></td>
<td><p>1.1 (1993)</p></td>
<td><p>1.1</p></td>
<td><p>3.0</p></td>
<td><p>Н/Д</p></td>
<td><p>Н/Д</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>2.0 (1994)</p></td>
<td><p>2.0</p></td>
<td><p>Н/Д</p></td>
<td><p>Н/Д</p></td>
<td><p>Н/Д</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Jet</p></td>
<td><p>2.5 (1995)</p></td>
<td><p>Недоступно</p></td>
<td><p>4.0 (16-битная)</p></td>
<td><p>Н/Д</p></td>
<td><p>Н/Д</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>3.0 (1995)</p></td>
<td><p>'95 (7.0)</p></td>
<td><p>4.0 (32-битная)</p></td>
<td><p>'95 (7.0)</p></td>
<td><p>4.x</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Jet</p></td>
<td><p>3.5 (1996)</p></td>
<td><p>'97 (8.0)</p></td>
<td><p>5.0</p></td>
<td><p>'97 (8.0)</p></td>
<td><p>5.0</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>4.0 (2000)</p></td>
<td><p>2000 (9.0)</p></td>
<td><p></p></td>
<td><p>2000 (9.0)</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Яд данных Microsoft Access</p></td>
<td><p>12.0 (2007)</p></td>
<td><p>2007</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

