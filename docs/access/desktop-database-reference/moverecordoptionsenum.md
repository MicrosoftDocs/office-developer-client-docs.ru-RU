---
title: MoveRecordOptionsEnum
TOCTitle: MoveRecordOptionsEnum
ms:assetid: 2785bca0-777c-a802-51d7-6f5cf0fb4210
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249039(v=office.15)
ms:contentKeyID: 48543842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc621f620a7d55571aa55296a4d294fff9566bf5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862242"
---
# <a name="moverecordoptionsenum"></a>MoveRecordOptionsEnum


**Применимо к**: Access 2013 | Office 2013

Задает поведение объекта [записи](record-object-ado.md) метод [MoveRecord](moverecord-method-ado.md) .

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
<td><p><strong>adMoveUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Значение, используемое по умолчанию. Выполняет операцию перемещения по умолчанию: операция не выполняется, если конечный файл или каталог уже существует, а операция обновляет ссылкам.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMoveOverWrite</strong></p></td>
<td><p>1</p></td>
<td><p>Перезапись файла или каталога назначения, даже в том случае, если он уже существует.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adMoveDontUpdateLinks</strong></p></td>
<td><p>2</p></td>
<td><p>Выполняется изменение поведения по умолчанию метод <strong>MoveRecord</strong> , не изменив ссылки гипертекста источника <strong>записей</strong>. Поведение по умолчанию зависит от возможностей поставщика. Операции перемещения обновляет ссылки, если поставщик поддерживает. Если поставщик не удается исправить ссылки или если это значение не указано, перемещение успешно, даже если ссылки не исправлены.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMoveAllowEmulation</strong></p></td>
<td><p>4</p></td>
<td><p>Запросы, что поставщик попытка моделировать move (с помощью загрузки, отправляемых операций и удаления). Если попытка переместить <strong>записи</strong> не удается выполнить из-за конечный URL-адрес на другом сервере, или обслуживаемых другого поставщика, чем источник, это может привести к увеличению задержки или потерю данных, из-за возможности другого поставщика при перемещении ресурсы между поставщиками.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы нет ADO/WFC эквивалентами.

