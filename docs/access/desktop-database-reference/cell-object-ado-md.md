---
title: Cell Object (ADO MD)
TOCTitle: Cell Object (ADO MD)
ms:assetid: b9d00b71-1f40-5bd1-4b89-fbdb59c552ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249892(v=office.15)
ms:contentKeyID: 48547356
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f38de1adc48e7d63a3b67e45f242a8cc884633ac
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482262"
---
# <a name="cell-object-ado-md"></a>Cell Object (ADO MD)


**Применимо к**: Access 2013 | Office 2013

Представляет данные на пересечении ось координат, содержащаяся в набор ячеек.

## <a name="remarks"></a>Замечания

Объект **Cell** возвращается свойством [Item](item-property-ado-md-cellset.md) объекта [ячеек](cellset-object-ado-md.md) .

Со свойствами объекта **ячейки** и семейств сайтов выполните следующее:

  - Возвращает данные в **ячейку** с помощью свойства [Value](value-property-ado-md.md) .

  - Возвращает строку, представляющую форматированное отображаемое **значение** свойства со свойством [FormattedValue](formattedvalue-property-ado-md.md) .

  - Возвращает порядковый номер **ячейки** в наборе **ячеек** с помощью свойства [порядковый номер](ordinal-property-ado-md-cell.md) .

  - Определите позицию **ячейки** в [CubeDef](cubedef-object-ado-md.md) с коллекцией [положения](positions-collection-ado-md.md) .

  - Получение других сведений о **ячейку** с помощью стандартных ADO [Свойства](properties-collection-ado.md) коллекции.

Коллекции **свойств** содержит свойства, предоставленных поставщиком. В следующей таблице перечислены свойства, которые могут быть недоступны. Список свойств фактический может различаться в зависимости от реализации поставщика. Обратитесь к документации вашего поставщика для получения более полного списка доступных свойств.

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
<td><p>Цвет фона</p></td>
<td><p>Цвет фона, используемый при отображении ячейки.</p></td>
</tr>
<tr class="even">
<td><p>FontFlags</p></td>
<td><p>Битовая шрифта.</p></td>
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
<td><p>Цвет текста</p></td>
<td><p>Цвет переднего плана, используемый при отображении ячейки.</p></td>
</tr>
<tr class="even">
<td><p>FormatString</p></td>
<td><p>Значение в формате строки.</p></td>
</tr>
</tbody>
</table>

