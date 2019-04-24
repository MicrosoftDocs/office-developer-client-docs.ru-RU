---
title: PropertyAttributesEnum
TOCTitle: PropertyAttributesEnum
ms:assetid: cbe93f65-a3ee-4741-1ac7-1c98ac53cdde
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250012(v=office.15)
ms:contentKeyID: 48547726
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c929bcf5dc7f5267c2e7d3a8dac5ed6bfb55b20b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302879"
---
# <a name="propertyattributesenum"></a>PropertyAttributesEnum


**Область применения**: Access 2013, Office 2013

Задает атрибуты объекта [Property](property-object-ado.md) .

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
<td><p><strong>Адпропнотсуппортед</strong></p></td>
<td><p>нуль</p></td>
<td><p>Указывает, что свойство не поддерживается поставщиком.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адпропрекуиред</strong></p></td>
<td><p>1,1</p></td>
<td><p>Указывает, что пользователь должен указать значение для этого свойства перед инициализацией источника данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адпропоптионал</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает, что пользователю не нужно указывать значение этого свойства перед инициализацией источника данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адпропреад</strong></p></td>
<td><p>512</p></td>
<td><p>Указывает, что пользователь может прочитать свойство.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адпропврите</strong></p></td>
<td><p>1024</p></td>
<td><p>Указывает, что пользователь может задать свойство.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com. MS. WFC. Data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Адоенумс. Пропертяттрибутес. NOTSUPPORTED</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Пропертяттрибутес. REQUIRED</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Пропертяттрибутес. OPTIONAL</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Пропертяттрибутес. READ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Пропертяттрибутес. WRITE</p></td>
</tr>
</tbody>
</table>

