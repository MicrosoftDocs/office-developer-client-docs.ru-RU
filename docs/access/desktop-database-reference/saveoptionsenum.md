---
title: SaveOptionsEnum (Справочник по для настольных баз данных Access)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 68526eca205fb41dd2789ec187514d0f9b11e35f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480681"
---
# <a name="saveoptionsenum"></a>SaveOptionsEnum


**Применимо к**: Access 2013 | Office 2013

Указывает, создан или перезаписан при сохранении из объекта [потока](stream-object-ado.md) файла. Значения может использоваться совместно с оператора AND.

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
<td><p><strong>adSaveCreateNotExist</strong></p></td>
<td><p>1</p></td>
<td><p>Значение, используемое по умолчанию. Создает новый файл, если файл, указанный с помощью параметра <em>имени файла</em> еще не существует.</p></td>
</tr>
<tr class="even">
<td><p><strong>adSaveCreateOverWrite</strong></p></td>
<td><p>2</p></td>
<td><p>Перезапись файла с данными из открытая в настоящий момент объект <strong>Stream</strong> , если файл, указанный с помощью параметра <em>имени файла</em> уже существует.</p></td>
</tr>
</tbody>
</table>


**Эквивалент ADO/WFC**

Эти константы нет ADO/WFC эквивалентами.

