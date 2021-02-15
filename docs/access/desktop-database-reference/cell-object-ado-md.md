---
title: Cell object (ADO MD)
TOCTitle: Cell object (ADO MD)
ms:assetid: b9d00b71-1f40-5bd1-4b89-fbdb59c552ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249892(v=office.15)
ms:contentKeyID: 48547356
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7bb2a479789a8c5bd1825b6cb04e602e0b829dfb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296551"
---
# <a name="cell-object-ado-md"></a>Cell object (ADO MD)


**Область применения**: Access 2013, Office 2013

Представляет данные на пересечении координат оси, содержащихся в ячейках.

## <a name="remarks"></a>Заметки

Объект **Cell** возвращается [свойством Item](item-property-ado-md-cellset.md) объекта [Cellset.](cellset-object-ado-md.md)

С помощью коллекций и свойств объекта **Cell** можно сделать следующее:

- Возвращает данные в **ячейке со** [свойством Value.](value-property-ado-md.md)

- Возвращает строку, представляющую отформатированный дисплей свойства **Value** со [свойством FormattedValue.](formattedvalue-property-ado-md.md)

- Возвращает порядковые значения ячейки **в** ячейках **с** помощью [свойства Ordinal.](ordinal-property-ado-md-cell.md)

- Определите положение **ячейки** в [CubeDef](cubedef-object-ado-md.md) с помощью коллекции [Positions.](positions-collection-ado-md.md)

- Получить другие сведения о **ячейке** со стандартной коллекцией [свойств](properties-collection-ado.md) ADO.

Коллекция **Properties** содержит свойства, предоставленные поставщиком. В следующей таблице перечислены свойства, которые могут быть доступны. Фактический список свойств может отличаться в зависимости от реализации поставщика. Более полный список доступных свойств см. в документации к поставщику.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BackColor</p></td>
<td><p>Цвет фона, используемый для отображения ячейки.</p></td>
</tr>
<tr class="even">
<td><p>FontFlags</p></td>
<td><p>Битоваяmas detailing effects on the font.</p></td>
</tr>
<tr class="odd">
<td><p>FontName</p></td>
<td><p>Шрифт, используемый для отображения значения ячейки.</p></td>
</tr>
<tr class="even">
<td><p>FontSize</p></td>
<td><p>Размер шрифта, используемый для отображения значения ячейки.</p></td>
</tr>
<tr class="odd">
<td><p>ForeColor</p></td>
<td><p>Цвет переднего плана, используемый при отобраке ячейки.</p></td>
</tr>
<tr class="even">
<td><p>FormatString</p></td>
<td><p>Значение в форматированной строке.</p></td>
</tr>
</tbody>
</table>

