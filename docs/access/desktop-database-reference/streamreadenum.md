---
title: StreamReadEnum (Ссылка на настольные базы данных)
TOCTitle: StreamReadEnum
ms:assetid: 12432c0d-dc2e-10ea-13db-0c07b6ba29bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248895(v=office.15)
ms:contentKeyID: 48543336
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4d9c96a7bb34fe0ab3512a316a92e1f7a01ef4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314723"
---
# <a name="streamreadenum"></a>StreamReadEnum

**Область применения**: Access 2013, Office 2013

Указывает, следует ли читать весь поток или следующую строку с объекта [Stream.](stream-object-ado.md)

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
<td><p><strong>adReadAll</strong></p></td>
<td><p>–1</p></td>
<td><p>Значение, используемое по умолчанию. Читает все bytes из потока, от текущего положения далее до <a href="eos-property-ado.md">маркера EOS.</a> Это единственное допустимые <strong>значения StreamReadEnum</strong> с двоичными потоками<a href="type-property-ado-stream.md">(Type</a> <strong>is adTypeBinary).</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adReadLine</strong></p></td>
<td><p>–2</p></td>
<td><p>Читает следующую строку из потока (назначена <a href="lineseparator-property-ado.md">свойством LineSeparator).</a></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы не имеют эквивалентов ADO/WFC.

