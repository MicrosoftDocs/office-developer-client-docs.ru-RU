---
title: PropertyAttributesEnum
TOCTitle: PropertyAttributesEnum
ms:assetid: cbe93f65-a3ee-4741-1ac7-1c98ac53cdde
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250012(v=office.15)
ms:contentKeyID: 48547726
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8f01efcc98ed12858712c28f080fb066d3dc1b41
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481050"
---
# <a name="propertyattributesenum"></a>PropertyAttributesEnum


**Применимо к**: Access 2013 | Office 2013

Указывает атрибуты [Свойства](property-object-ado.md) объекта.

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
<td><p><strong>adPropNotSupported</strong></p></td>
<td><p>0</p></td>
<td><p>Указывает, что свойство не поддерживается поставщиком.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPropRequired</strong></p></td>
<td><p>1</p></td>
<td><p>Указывает, что пользователь должен указать значение для этого свойства перед инициализацией источника данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPropOptional</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает, что пользователю необходимо указать значение для этого свойства перед инициализацией источника данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPropRead</strong></p></td>
<td><p>512</p></td>
<td><p>Указывает, что пользователи могут читать свойства.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPropWrite</strong></p></td>
<td><p>1024</p></td>
<td><p>Указывает, что пользователь может задать свойства.</p></td>
</tr>
</tbody>
</table>


**Эквивалент ADO/WFC**

Пакет: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.PropertyAttributes.NOTSUPPORTED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.PropertyAttributes.REQUIRED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.PropertyAttributes.OPTIONAL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.PropertyAttributes.READ</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.PropertyAttributes.WRITE</p></td>
</tr>
</tbody>
</table>
