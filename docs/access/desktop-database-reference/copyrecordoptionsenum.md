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
<td><p><strong>Адкопялловемулатион</strong></p></td>
<td><p>SP4</p></td>
<td><p>Указывает, что поставщик <em>источника</em> пытается имитировать копию с помощью операций скачивания и отправки, если происходит сбой этого метода из-за того, что <em>целевой объект</em> находится на другом сервере или обрабатывается поставщиком, отличным от <em>источника</em>. Обратите внимание, что различные возможности поставщика могут препятствовать снижению производительности или потере данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адкопинонрекурсиве</strong></p></td>
<td><p>2</p></td>
<td><p>Копирует текущий каталог, но не все его подкаталоги в назначение. Операция копирования не является рекурсивной.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адкопйоверврите</strong></p></td>
<td><p>1,1</p></td>
<td><p>Перезаписывает файл или каталог, если <em>целевой</em> объект указывает на существующий файл или каталог.</p></td>
</tr>
<tr class="even">
<td><p><strong>АдкопюнспеЦифиед</strong></p></td>
<td><p>–1</p></td>
<td><p>Значение, используемое по умолчанию. Выполняет операцию копирования по умолчанию: операция завершается с ошибкой, если конечный файл или каталог уже существует, а операция рекурсивно копируется.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы не имеют эквивалентов ADO/WFC.

