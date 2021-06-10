---
title: FieldAttributeEnum (Ссылка на настольные базы данных)
TOCTitle: FieldAttributeEnum
ms:assetid: 2d3a541e-a437-6108-ab0e-90c7884b3df7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249071(v=office.15)
ms:contentKeyID: 48543967
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 079c79af3d15a6a5864a7db7f8334393258cfd42
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292603"
---
# <a name="fieldattributeenum"></a>FieldAttributeEnum

**Область применения**: Access 2013, Office 2013

Указывает один или несколько атрибутов объекта [Field.](field-object-ado.md)

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
<td><p><strong>adFldCacheDeferred</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Указывает, что поставщик кэша значений поля и последующих считывалось из кэша.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldFixed</strong></p></td>
<td><p>0x10</p></td>
<td><p>Указывает, что поле содержит данные фиксированной длины.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsChapter</strong></p></td>
<td><p>0x2000</p></td>
<td><p>Указывает, что поле содержит значение главы, которое указывает определенный набор записей ребенка, связанный с этим родительским полем. Обычно поля глав используются при формировании данных или фильтрах.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldIsCollection</strong></p></td>
<td><p>0x40000</p></td>
<td><p>Указывает, что поле указывает, что ресурс, представленный записью, представляет собой коллекцию других ресурсов, таких как папка, а не простой ресурс, например текстовый файл.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsDefaultStream</strong></p></td>
<td><p>0x20000</p></td>
<td><p>Указывает, что поле содержит поток по умолчанию для ресурса, представленного записью. Например, поток по умолчанию может быть HTML-контентом корневой папки на веб-сайте, который автоматически подается при указании корневого URL-адреса.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldIsNullable</strong></p></td>
<td><p>0x20</p></td>
<td><p>Указывает, что поле принимает значения null.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsRowURL</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Указывает, что поле содержит URL-адрес, который называет ресурс из магазина данных, представленного записью.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldLong</strong></p></td>
<td><p>0x80</p></td>
<td><p>Указывает, что поле — это длинное двоичное поле. Также указывает, что можно использовать методы <a href="appendchunk-method-ado.md">AppendChunk</a> и <a href="getchunk-method-ado.md">GetChunk.</a></p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldMayBeNull</strong></p></td>
<td><p>0x40</p></td>
<td><p>Указывает, что вы можете читать значения null из поля.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldMayDefer</strong></p></td>
<td><p>0x2</p></td>
<td><p>Указывает, что поле отложено, то есть значения поля извлекаются не из источника данных со всей записью, а только при явном доступе к ним.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldNegativeScale</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Указывает, что поле представляет числовую величину столбца, поддерживают отрицательные значения масштабирования. Масштаб указывается <a href="numericscale-property-ado.md">свойством NumericScale.</a></p></td>
</tr>
<tr class="even">
<td><p><strong>adFldRowID</strong></p></td>
<td><p>0x100</p></td>
<td><p>Указывает, что поле содержит постоянный идентификатор строки, который не может быть написан и не имеет значимого значения, кроме как определить строку (например, номер записи, уникальный идентификатор и так далее).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldRowVersion</strong></p></td>
<td><p>0x200</p></td>
<td><p>Указывает, что поле содержит какой-то штамп времени или даты, используемый для отслеживания обновлений.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldUnknownUpdatable</strong></p></td>
<td><p>0x8</p></td>
<td><p>Указывает, что поставщик не может определить, можно ли написать в поле.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldUnspecified</strong></p></td>
<td><p>–1<br />
0xFFFFFFFF</p></td>
<td><p>Указывает, что поставщик не указывает атрибуты поля.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldUpdatable</strong></p></td>
<td><p>0x4</p></td>
<td><p>Указывает, что вы можете написать в поле.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com.ms.wfc.data**

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

