---
title: MoveRecordOptionsEnum
TOCTitle: MoveRecordOptionsEnum
ms:assetid: 2785bca0-777c-a802-51d7-6f5cf0fb4210
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249039(v=office.15)
ms:contentKeyID: 48543842
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5bd8196670513156011d69f08eacf790fa4a0a03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288674"
---
# <a name="moverecordoptionsenum"></a>MoveRecordOptionsEnum


**Область применения**: Access 2013, Office 2013

Указывает поведение метода [Объекта](record-object-ado.md) [Записи MoveRecord.](moverecord-method-ado.md)

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
<td><p>–1</p></td>
<td><p>Значение, используемое по умолчанию. Выполняет операцию перемещения по умолчанию: операция не выполняется, если файл назначения или каталог уже существует, и операция обновляет ссылки на гипертекст.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMoveOverWrite</strong></p></td>
<td><p>1</p></td>
<td><p>Переоценка файла назначения или каталога, даже если он уже существует.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adMoveDontUpdateLinks</strong></p></td>
<td><p>2</p></td>
<td><p>Изменяет поведение метода <strong>MoveRecord</strong> по умолчанию, не обновляя гипертекстовых ссылок исходных <strong>записей.</strong> Поведение по умолчанию зависит от возможностей поставщика. Перемещение ссылок на обновления операций, если поставщик способен. Если поставщик не может исправить ссылки или если это значение не указано, перемещение успешно, даже если ссылки не исправлены.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMoveAllowEmulation</strong></p></td>
<td><p>4 </p></td>
<td><p>Запросы, которые поставщик пытается имитировать перемещение (с помощью скачивания, загрузки и удаления операций). Если попытка переместить <strong></strong> запись не удалась из-за того, что URL-адрес назначения находится на другом сервере или обслужен другим поставщиком, чем источник, это может привести к увеличению задержки или потере данных из-за различных возможностей поставщика при перемещении ресурсов между поставщиками.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы не имеют эквивалентов ADO/WFC.

