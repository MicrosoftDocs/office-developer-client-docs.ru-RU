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

Задает поведение метода [MoveRecord](moverecord-method-ado.md) объекта [Record](record-object-ado.md) .

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
<td><p><strong>АдмовеунспеЦифиед</strong></p></td>
<td><p>–1</p></td>
<td><p>Значение, используемое по умолчанию. Выполняет операцию перемещения по умолчанию: операция завершается с ошибкой, если конечный файл или каталог уже существует, а операция обновляет гипертекстовые ссылки.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адмовеоверврите</strong></p></td>
<td><p>1,1</p></td>
<td><p>Перезаписывает конечный файл или каталог, даже если он уже существует.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адмоведонтупдателинкс</strong></p></td>
<td><p>2</p></td>
<td><p>Изменяет поведение метода <strong>MoveRecord</strong> по умолчанию, не обновляя гипертекстовые ссылки исходной <strong>записи</strong>. Поведение по умолчанию зависит от возможностей поставщика. Операция перемещения обновляет ссылки, если поставщик поддерживает эту возможность. Если поставщик не может исправить ссылки или это значение не указано, то перемещение выполняется, даже если ссылки не были исправлены.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адмовеалловемулатион</strong></p></td>
<td><p>SP4</p></td>
<td><p>ЗаПрашивает, чтобы поставщик пытался имитировать перемещение (с помощью операций скачивания, отправки и удаления). Если не удается переместить <strong>запись</strong> , так как конечный URL-адрес находится на другом сервере или обслуживается другим поставщиком, чем исходный, это может привести к увеличению задержки или потере данных из-за различных возможностей поставщика при перемещении ресурсов. между поставщиками.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы не имеют эквивалентов ADO/WFC.

