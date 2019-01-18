---
title: EditModeEnum (Справочник по для настольных баз данных Access)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 246d9e29f084efb975783fd15c15993eba5a6e74
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726290"
---
# <a name="editmodeenum"></a>EditModeEnum

**Применимо к**: Access 2013, Office 2013

Указывает состояние редактирования записи.

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
<td><p><strong>как таковые</strong></p></td>
<td><p>0</p></td>
<td><p>Указывает, что операция редактирования не находится в стадии разработки.</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditInProgress</strong></p></td>
<td><p>1</p></td>
<td><p>Указывает, что данные в текущей записи были изменены, но не сохраняются.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adEditAdd</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает, что был вызван метод <a href="addnew-method-ado.md">AddNew</a> и текущую запись в буфер копирования является новую запись, которая не была сохранена в базе данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditDelete</strong></p></td>
<td><p>4</p></td>
<td><p>Указывает, что текущая запись был удален.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com.ms.wfc.data**

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
<td><p>AdoEnums.EditMode.NONE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EditMode.INPROGRESS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EditMode.ADD</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EditMode.DELETE</p></td>
</tr>
</tbody>
</table>

