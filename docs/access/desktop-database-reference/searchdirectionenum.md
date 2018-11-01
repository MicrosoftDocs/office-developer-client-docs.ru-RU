---
title: SearchDirectionEnum
TOCTitle: SearchDirectionEnum
ms:assetid: d491000b-47d0-bb28-95ed-7526dbb7c5e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250064(v=office.15)
ms:contentKeyID: 48547943
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e456cfcc344c818504cb2ae1c2af9a4294b004ed
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876416"
---
# <a name="searchdirectionenum"></a>SearchDirectionEnum


**Применимо к**: Access 2013, Office 2013

Задает направление поиска записи в наборе [записей](recordset-object-ado.md).

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
<td><p><strong>adSearchBackward</strong></p></td>
<td><p>-1</p></td>
<td><p>Выполняет поиск назад, остановив в начале <strong>набора записей</strong>. Если совпадение не найдено, указатель записи располагается в <a href="bof-eof-properties-ado.md">BOF</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adSearchForward</strong></p></td>
<td><p>1</p></td>
<td><p>Поиск вперед, остановка в конце <strong>набора записей</strong>. Если совпадение не найдено, указатель записи располагается в <a href="bof-eof-properties-ado.md">конец файла</a>.</p></td>
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
<th><p>Constant</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.SearchDirection.BACKWARD</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.SearchDirection.FORWARD</p></td>
</tr>
</tbody>
</table>

