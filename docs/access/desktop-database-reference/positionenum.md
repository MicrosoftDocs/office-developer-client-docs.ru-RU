---
title: Поситионенум (Справочник по базам данных Access на компьютере)
TOCTitle: PositionEnum
ms:assetid: 2a6f294b-74f2-b951-e32a-79ff5e782204
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249054(v=office.15)
ms:contentKeyID: 48543907
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4c791cbd31e346eef5ab8503cb55b0dec5e9fbbc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287505"
---
# <a name="positionenum"></a>PositionEnum

**Область применения**: Access 2013, Office 2013

Задает текущее положение указателя записи в [наборе записей](recordset-object-ado.md).

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
<td><p><strong>Адпосбоф</strong></p></td>
<td><p>–2</p></td>
<td><p>Указывает, что указатель текущей записи находится на BOF (то есть свойство <a href="bof-eof-properties-ado.md">BOF</a> имеет <strong>значение true</strong>).</p></td>
</tr>
<tr class="even">
<td><p><strong>Адпосеоф</strong></p></td>
<td><p>–3</p></td>
<td><p>Указывает, что указатель текущей записи находится на EOF (свойство <a href="bof-eof-properties-ado.md">EOF</a> имеет <strong>значение true</strong>).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адпосункновн</strong></p></td>
<td><p>–1</p></td>
<td><p>Указывает, что <strong>набор записей</strong> пуст, текущая позиция неизвестна или поставщик не поддерживает свойство <a href="absolutepage-property-ado.md">AbsolutePage</a> или <a href="absoluteposition-property-ado.md">AbsolutePosition</a> .</p></td>
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
<td><p>Адоенумс. Position. BOF</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Position. EOF</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Position. UNKNOWN</p></td>
</tr>
</tbody>
</table>

