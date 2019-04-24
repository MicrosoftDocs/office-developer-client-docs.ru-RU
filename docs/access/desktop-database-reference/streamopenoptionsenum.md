---
title: StreamOpenOptionsEnum
TOCTitle: StreamOpenOptionsEnum
ms:assetid: d4bbd6be-41f1-cdf2-9d8f-b77ce83fb88e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250069(v=office.15)
ms:contentKeyID: 48547951
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f335f8572fbade23b949abacce8dd3690d205e32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314751"
---
# <a name="streamopenoptionsenum"></a>StreamOpenOptionsEnum


**Область применения**: Access 2013, Office 2013

Задает параметры открытия объекта [Stream](stream-object-ado.md) . Значения можно сочетать с операцией OR.

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
<td><p><strong>Адопенстреамасинк</strong></p></td>
<td><p>1,1</p></td>
<td><p>Открывает объект <strong>Stream</strong> в асинхронном режиме.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адопенстреамфромрекорд</strong></p></td>
<td><p>SP4</p></td>
<td><p>Определяет содержимое <em>исходного</em> параметра как уже открытый объект <a href="record-object-ado.md">Record</a> . Поведение по умолчанию состоит в том, чтобы рассматривать <em>источник</em> как URL-адрес, который указывает непосредственно на узел в древовидной структуре. Открывается поток по умолчанию, связанный с этим узлом.</p></td>
</tr>
<tr class="odd">
<td><p><strong>АдопенстреамунспеЦифиед</strong></p></td>
<td><p>–1</p></td>
<td><p>Значение, используемое по умолчанию. Указывает, что открывает объект <strong>Stream</strong> с параметрами по умолчанию.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы не имеют эквивалентов ADO/WFC.

