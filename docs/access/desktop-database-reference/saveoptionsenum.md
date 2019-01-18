---
title: SaveOptionsEnum (Справочник по для настольных баз данных Access)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77a617dc54d8acd145648d926e10cf7c9a3cf252
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705997"
---
# <a name="saveoptionsenum"></a>SaveOptionsEnum

**Применимо к**: Access 2013, Office 2013

Указывает, создан или перезаписан при сохранении из объекта [потока](stream-object-ado.md) файла. Значения может использоваться совместно с оператора AND.

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


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы нет ADO/WFC эквивалентами.

