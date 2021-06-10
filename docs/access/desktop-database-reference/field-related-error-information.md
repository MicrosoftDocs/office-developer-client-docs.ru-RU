---
title: Сведения об ошибках, связанных с полями
TOCTitle: Field-related error information
ms:assetid: 81a2c5a4-ab09-53d8-b270-e889b00a0c1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249559(v=office.15)
ms:contentKeyID: 48545958
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a0d0362b8f0ff9570a92a3c1c364061d1f9a584
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292974"
---
# <a name="field-related-error-information"></a>Сведения об ошибках, связанных с полями


**Область применения**: Access 2013, Office 2013

Если ошибка напрямую связана с полем , например, если данные отсутствуют или это неправильный тип для поля, вы можете получить дополнительные сведения о причине проблемы, изучив свойство **Status** объекта **Field.** Это свойство было расширено, чтобы предоставить конкретные сведения о проблеме. Например, при срабатывке вызова **в UpdateBatch** можно определить причину проблемы, изучив  свойство **Status** полей в каждой из эффектных записей. Свойство будет содержать одно из значений константы **FieldStatusEnum.** В следующей таблице содержатся значения, которые имеют особый интерес при ошибке.

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
<td><p><strong>adFieldCantConvertValue</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает, что поле не может быть извлечено или сохранено без потери данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldDataOverflow</strong></p></td>
<td><p>6 </p></td>
<td><p>Указывает, что данные, возвращающиеся от поставщика, переполнили тип данных поля.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>Указывает, что значение по умолчанию для поля использовалось при настройке данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIgnore</strong></p></td>
<td><p>15</p></td>
<td><p>Указывает, что это поле было пропущено при настройке значений данных в источнике. Поставщик не установил значение.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIntegrityViolation</strong></p></td>
<td><p>10 </p></td>
<td><p>Указывает, что поле не может быть изменено, так как это вычисляемая или полученная сущность.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIsNull</strong></p></td>
<td><p>3</p></td>
<td><p>Указывает, что поставщик вернул значение null.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldOutOfSpace</strong></p></td>
<td><p>22</p></td>
<td><p>Указывает, что поставщик не может получить достаточно места для хранения для выполнения операции перемещения или копирования.</p></td>
</tr>
</tbody>
</table>

