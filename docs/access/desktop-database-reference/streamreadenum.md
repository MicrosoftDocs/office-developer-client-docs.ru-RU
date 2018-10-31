---
title: StreamReadEnum (Справочник по для настольных баз данных Access)
TOCTitle: StreamReadEnum
ms:assetid: 12432c0d-dc2e-10ea-13db-0c07b6ba29bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248895(v=office.15)
ms:contentKeyID: 48543336
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 69a8c49fd9d07c1e0d67a91e131be76ad9803ad0
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861052"
---
# <a name="streamreadenum"></a>StreamReadEnum

**Применимо к**: Access 2013 | Office 2013

Указывает, следует ли считывать весь поток или следующую строку из объекта [потока](stream-object-ado.md) .

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
<td><p>-1</p></td>
<td><p>Значение, используемое по умолчанию. Считывает все байты из потока из текущей позиции добавляющего <a href="eos-property-ado.md">EOS</a> маркер. Это допустимо только значение <strong>StreamReadEnum</strong> с двоичных потоков (<a href="type-property-ado-stream.md">Тип</a> — <strong>adTypeBinary</strong>).</p></td>
</tr>
<tr class="even">
<td><p><strong>adReadLine</strong></p></td>
<td><p>-2</p></td>
<td><p>Считывает следующую строку в потоке (обозначенного свойство <a href="lineseparator-property-ado.md">LineSeparator</a> ).</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы нет ADO/WFC эквивалентами.

