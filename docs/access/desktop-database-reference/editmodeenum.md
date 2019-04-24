---
title: Едитмодинум (Справочник по базам данных Access на компьютере)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 246d9e29f084efb975783fd15c15993eba5a6e74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293583"
---
# <a name="editmodeenum"></a>EditModeEnum

**Область применения**: Access 2013, Office 2013

Задает состояние редактирования записи.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Адедитноне</strong></p></td>
<td><p>нуль</p></td>
<td><p>Указывает, что операции редактирования не выполняются.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адедитинпрогресс</strong></p></td>
<td><p>1,1</p></td>
<td><p>Указывает, что данные в текущей записи были изменены, но не были сохранены.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адедитадд</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает на то, что метод <a href="addnew-method-ado.md">AddNew</a> вызван, а текущая запись в буфере копии — это новая запись, которая не была сохранена в базе данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адедитделете</strong></p></td>
<td><p>SP4</p></td>
<td><p>Указывает, что текущая запись была удалена.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com. MS. WFC. Data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Адоенумс. EditMode. NONE</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. EditMode. неВЫПОЛНЕНИЕ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. EditMode. ADD</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. EditMode. DELETE</p></td>
</tr>
</tbody>
</table>

