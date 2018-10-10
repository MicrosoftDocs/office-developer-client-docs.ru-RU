---
title: FieldAttributeEnum (Справочник по для настольных баз данных Access)
TOCTitle: FieldAttributeEnum
ms:assetid: 2d3a541e-a437-6108-ab0e-90c7884b3df7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249071(v=office.15)
ms:contentKeyID: 48543967
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 75644308b1af0dd4c6e3b40b2bd6b1c7461f928f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482614"
---
# <a name="fieldattributeenum"></a>FieldAttributeEnum


**Применимо к**: Access 2013 | Office 2013

Задает один или несколько атрибутов объекта [поля](field-object-ado.md) .

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
<td><p><strong>adFldCacheDeferred</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Указывает, что поставщик кэширует значения полей и что последующих операций чтения выполняются из кэша.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldFixed</strong></p></td>
<td><p>0x10</p></td>
<td><p>Указывает, что поле содержит данные фиксированной длины.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsChapter</strong></p></td>
<td><p>0x2000</p></td>
<td><p>Указывает, что поле содержит значение главы, которое указывает набор дочерних записей, связанного с данным полем родительского. Обычно поля главы используются с формирования данных или фильтры.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldIsCollection</strong></p></td>
<td><p>0x40000</p></td>
<td><p>Означает, что это поле указывает, что представленный запись ресурса представляет собой коллекцию другие ресурсы, например, в папке, а не простой ресурсов, таких как текстовый файл.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsDefaultStream</strong></p></td>
<td><p>0x20000</p></td>
<td><p>Указывает, что поле содержит поток по умолчанию для ресурса, представленное эту запись. Например поток по умолчанию может быть HTML-содержимое в корневой папке на веб-сайт, который автоматически выдается, когда он указан корневой URL-адрес.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldIsNullable</strong></p></td>
<td><p>0x20</p></td>
<td><p>Указывает, что поле может принимать значения null.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsRowURL</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Указывает, что поле содержит URL-адрес, имена ресурсов из хранилища данных, представленного эту запись.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldLong</strong></p></td>
<td><p>0x80</p></td>
<td><p>Указывает, что поле двоичные поля. Также указывается, что можно использовать методы <a href="appendchunk-method-ado.md">AppendChunk</a> и <a href="getchunk-method-ado.md">GetChunk</a> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldMayBeNull</strong></p></td>
<td><p>0x40</p></td>
<td><p>Указывает, что значения null могут читать из поля.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldMayDefer</strong></p></td>
<td><p>0x2</p></td>
<td><p>Указывает, что поле откладывается, то есть, значения полей не извлекаются из источника данных с помощью всей записи, но только в том случае, если вы явно к ним доступ.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldNegativeScale</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Указывает, что поле представляет числовое значение из столбца, поддерживающего масштаба отрицательные значения. Масштаб, задаваемое свойству <a href="numericscale-property-ado.md">NumericScale</a> .</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldRowID</strong></p></td>
<td><p>0x100</p></td>
<td><p>Указывает, что поле содержит постоянный идентификатор строки, который невозможно записать и не имеет смысл значения кроме идентификации строки (например, запишите номер, уникальный идентификатор и т. д.).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldRowVersion</strong></p></td>
<td><p>0x200</p></td>
<td><p>Указывает, что поле содержит каких-либо штамп даты и времени для отслеживания обновлений.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldUnknownUpdatable</strong></p></td>
<td><p>0x8</p></td>
<td><p>Указывает, что поставщик не может определить, если можно создать в поле.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldUnspecified</strong></p></td>
<td><p>-1<br />
0xFFFFFFFF</p></td>
<td><p>Указывает, что поставщик не определяет атрибуты поля.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldUpdatable</strong></p></td>
<td><p>0x4</p></td>
<td><p>Указывает, что можно написать в поле.</p></td>
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
<td><p>AdoEnums.FieldAttribute.CACHEDEFERRED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FieldAttribute.FIXED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FieldAttribute.ISNULLABLE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FieldAttribute.LONG</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FieldAttribute.MAYBENULL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FieldAttribute.MAYDEFER</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FieldAttribute.NEGATIVESCALE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FieldAttribute.ROWID</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FieldAttribute.ROWVERSION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FieldAttribute.UNSPECIFIED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FieldAttribute.UPDATABLE</p></td>
</tr>
</tbody>
</table>

