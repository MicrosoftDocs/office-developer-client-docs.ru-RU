---
title: Курсортипинум (Справочник по базам данных Access на компьютере)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0bcaaa1298f12d72c5e836dcfe1e74cdcda68d19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295165"
---
# <a name="cursortypeenum"></a>CursorTypeEnum

**Область применения**: Access 2013, Office 2013

Указывает тип курсора, используемого в объекте [Recordset](recordset-object-ado.md) .

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
<td><p><strong>Адопендинамик</strong></p></td>
<td><p>2</p></td>
<td><p>Использование динамического курсора. Для других пользователей отображаются дополнения, изменения и удаления, а также все типы передвижений по <strong>набору записей</strong> , кроме закладок, если они не поддерживаются поставщиком.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адопенфорвардонли</strong></p></td>
<td><p>нуль</p></td>
<td><p>Значение, используемое по умолчанию. Использует однонаправленный курсор. Идентично статическому курсору, за исключением того, что можно прокручивать только записи вперед. Это повышает производительность, если необходимо выполнить только один проход через <strong>набор записей</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адопенкэйсет</strong></p></td>
<td><p>1,1</p></td>
<td><p>Использует курсор KEYSET. Как и динамический курсор, за исключением того, что записи, добавленные другими пользователями, не видны, хотя записи, которые другие пользователи удаляют, недоступны из <strong>набора записей</strong>. Изменения данных, внесенные другими пользователями, по-прежнему видимы.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адопенстатик</strong></p></td>
<td><p>4</p></td>
<td><p>Использует статический курсор. Статическая копия набора записей, которую можно использовать для поиска данных или создания отчетов. Добавленные, измененные или удаленные пользователи не отображаются.</p></td>
</tr>
<tr class="odd">
<td><p><strong>АдопенунспеЦифиед</strong></p></td>
<td><p>–1</p></td>
<td><p>Не указывает тип курсора.</p></td>
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
<td><p>Адоенумс. CursorType. DYNAMIC</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. CursorType. ФОРВАРДОНЛИ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. CursorType. KEYSET</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. CursorType. STATIC</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. CursorType. unspecifieded</p></td>
</tr>
</tbody>
</table>

