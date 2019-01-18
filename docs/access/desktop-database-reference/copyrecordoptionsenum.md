---
title: CopyRecordOptionsEnum
TOCTitle: CopyRecordOptionsEnum
ms:assetid: ab9426e9-0e4e-6c85-43cf-e4a205a7c4c0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249795(v=office.15)
ms:contentKeyID: 48546975
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eb1637d1757a8507c6b6abb2a0c71867e3d1177b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703848"
---
# <a name="copyrecordoptionsenum"></a>CopyRecordOptionsEnum


**Применимо к**: Access 2013, Office 2013

Задает поведение метода [CopyRecord](copyrecord-method-ado.md) .

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
<td><p><strong>adCopyAllowEmulation</strong></p></td>
<td><p>4</p></td>
<td><p>Указывает, что поставщик <em>источника</em> пытается моделирования копии, с помощью загрузки и отправьте операции, если этот метод не удается выполнить из-за <em>назначения</em> , на другом сервере, или обслуживаемых другого поставщика, чем <em>источник</em>. Обратите внимание, что разные возможности поставщика может препятствовать производительности или потери данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCopyNonRecursive</strong></p></td>
<td><p>2</p></td>
<td><p>Копирует текущий каталог, но ни один из его подкаталогов в место назначения. Операция копирования не рекурсивный.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCopyOverWrite</strong></p></td>
<td><p>1</p></td>
<td><p>Перезапись файла или папки <em>назначения</em> указывает на существующий файл или каталог.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCopyUnspecified</strong></p></td>
<td><p>–1</p></td>
<td><p>Значение, используемое по умолчанию. Выполняет операцию копирования по умолчанию: завершится неудачно, если конечный файл или каталог уже существует и рекурсивно копирует операции.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы нет ADO/WFC эквивалентами.

