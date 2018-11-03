---
title: Сведения об ошибках, связанных с полями
TOCTitle: Field-related error information
ms:assetid: 81a2c5a4-ab09-53d8-b270-e889b00a0c1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249559(v=office.15)
ms:contentKeyID: 48545958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e853c45e4ee0de9a958ccc791bac3afcd305a23
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943565"
---
# <a name="field-related-error-information"></a>Сведения об ошибках, связанных с полями


**Применимо к**: Access 2013, Office 2013

Если ошибка, непосредственно связан с полем — например, если отсутствуют данные или имеет неверный тип поля — можно получить дополнительные сведения о причине проблемы, проверив свойство **состояние** объекта **поля** . Это свойство улучшена для предоставления конкретной информации о проблеме. Таким образом например, при сбое вызова **UpdateBatch** причины проблемы можно определить путем проверки свойство **Status** **полей** в каждой записи задействованных базах. Это свойство будет содержать одно из значений в **FieldStatusEnum** константу. В следующей таблице представлены эти значения, которые могут представлять интерес при возникновении ошибки.

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
<td><p>Указывает поля извлекается или хранятся без потери данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldDataOverflow</strong></p></td>
<td><p>6</p></td>
<td><p>Указывает, что данные, возвращаемые от поставщика переполнена тип данных поля.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>Указывает, что значение по умолчанию для поля было использовано при задании данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIgnore</strong></p></td>
<td><p>15</p></td>
<td><p>Указывает, что это поле была пропущена при значения параметра данных в источнике. Значение не было установлено поставщиком.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIntegrityViolation</strong></p></td>
<td><p>10</p></td>
<td><p>Указывает, что поле нельзя изменить, так как они вычисляемые или производные сущности.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIsNull</strong></p></td>
<td><p>3</p></td>
<td><p>Указывает, что поставщик возвращается значение null.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldOutOfSpace</strong></p></td>
<td><p>22</p></td>
<td><p>Указывает, что поставщик не удается получить достаточно дискового пространства для выполнения перемещения или копирования операции.</p></td>
</tr>
</tbody>
</table>

