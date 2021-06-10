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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295487"
---
# <a name="copyrecordoptionsenum"></a>CopyRecordOptionsEnum


**Область применения**: Access 2013, Office 2013

Указывает поведение метода [CopyRecord.](copyrecord-method-ado.md)

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
<td><p>4 </p></td>
<td><p>Указывает, что <em></em> поставщик исходных данных пытается смоделировать копию с помощью операций загрузки и загрузки, если этот метод не удается из-за того, что <em>Destination</em> находится на другом сервере или находится на службе у другого поставщика, чем <em>Source</em>. Обратите внимание, что различные возможности поставщика могут препятствовать производительности или терять данные.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCopyNonRecursive</strong></p></td>
<td><p>2</p></td>
<td><p>Копирует текущий каталог, но ни один из его поднаправлений в пункт назначения. Операция копирования не является повторяемой.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCopyOverWrite</strong></p></td>
<td><p>1</p></td>
<td><p>Переоценка файла или каталога, если <em>пункт Назначения</em> указывает на существующий файл или каталог.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCopyUnspecified</strong></p></td>
<td><p>–1</p></td>
<td><p>Значение, используемое по умолчанию. Выполняет операцию копирования по умолчанию: операция сбой, если файл назначения или каталог уже существует, и операция копирует повторно.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы не имеют эквивалентов ADO/WFC.

