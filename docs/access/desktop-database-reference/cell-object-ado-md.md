---
title: Объект Cell (ADO MD)
TOCTitle: Cell object (ADO MD)
ms:assetid: b9d00b71-1f40-5bd1-4b89-fbdb59c552ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249892(v=office.15)
ms:contentKeyID: 48547356
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2e119600567c8d3c6cd23348d9b9560011e27a87
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924612"
---
# <a name="cell-object-ado-md"></a><span data-ttu-id="8ebe2-102">Объект Cell (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="8ebe2-102">Cell object (ADO MD)</span></span>


<span data-ttu-id="8ebe2-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ebe2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ebe2-104">Представляет данные на пересечении ось координат, содержащаяся в набор ячеек.</span><span class="sxs-lookup"><span data-stu-id="8ebe2-104">Represents the data at the intersection of axis coordinates contained in a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ebe2-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ebe2-105">Remarks</span></span>

<span data-ttu-id="8ebe2-106">Объект **Cell** возвращается свойством [Item](item-property-ado-md-cellset.md) объекта [ячеек](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="8ebe2-106">A **Cell** object is returned by the [Item](item-property-ado-md-cellset.md) property of a [Cellset](cellset-object-ado-md.md) object.</span></span>

<span data-ttu-id="8ebe2-107">Со свойствами объекта **ячейки** и семейств сайтов выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="8ebe2-107">With the collections and properties of a **Cell** object, you can do the following:</span></span>

  - <span data-ttu-id="8ebe2-108">Возвращает данные в **ячейку** с помощью свойства [Value](value-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="8ebe2-108">Return the data in the **Cell** with the [Value](value-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="8ebe2-109">Возвращает строку, представляющую форматированное отображаемое **значение** свойства со свойством [FormattedValue](formattedvalue-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="8ebe2-109">Return the string representing the formatted display of the **Value** property with the [FormattedValue](formattedvalue-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="8ebe2-110">Возвращает порядковый номер **ячейки** в наборе **ячеек** с помощью свойства [порядковый номер](ordinal-property-ado-md-cell.md) .</span><span class="sxs-lookup"><span data-stu-id="8ebe2-110">Return the ordinal value of the **Cell** within the **Cellset** with the [Ordinal](ordinal-property-ado-md-cell.md) property.</span></span>

  - <span data-ttu-id="8ebe2-111">Определите позицию **ячейки** в [CubeDef](cubedef-object-ado-md.md) с коллекцией [положения](positions-collection-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="8ebe2-111">Determine the position of the **Cell** within the [CubeDef](cubedef-object-ado-md.md) with the [Positions](positions-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="8ebe2-112">Получение других сведений о **ячейку** с помощью стандартных ADO [Свойства](properties-collection-ado.md) коллекции.</span><span class="sxs-lookup"><span data-stu-id="8ebe2-112">Retrieve other information about the **Cell** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="8ebe2-113">Коллекции **свойств** содержит свойства, предоставленных поставщиком.</span><span class="sxs-lookup"><span data-stu-id="8ebe2-113">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="8ebe2-114">В следующей таблице перечислены свойства, которые могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="8ebe2-114">The following table lists properties that might be available.</span></span> <span data-ttu-id="8ebe2-115">Список свойств фактический может различаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="8ebe2-115">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="8ebe2-116">Обратитесь к документации вашего поставщика для получения более полного списка доступных свойств.</span><span class="sxs-lookup"><span data-stu-id="8ebe2-116">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8ebe2-117">Имя</span><span class="sxs-lookup"><span data-stu-id="8ebe2-117">Name</span></span></p></th>
<th><p><span data-ttu-id="8ebe2-118">Описание</span><span class="sxs-lookup"><span data-stu-id="8ebe2-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ebe2-119">Цвет фона</span><span class="sxs-lookup"><span data-stu-id="8ebe2-119">BackColor</span></span></p></td>
<td><p><span data-ttu-id="8ebe2-120">Цвет фона, используемый при отображении ячейки.</span><span class="sxs-lookup"><span data-stu-id="8ebe2-120">Background color used when displaying the cell.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ebe2-121">FontFlags</span><span class="sxs-lookup"><span data-stu-id="8ebe2-121">FontFlags</span></span></p></td>
<td><p><span data-ttu-id="8ebe2-122">Битовая шрифта.</span><span class="sxs-lookup"><span data-stu-id="8ebe2-122">Bitmask detailing effects on the font.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ebe2-123">FontName</span><span class="sxs-lookup"><span data-stu-id="8ebe2-123">FontName</span></span></p></td>
<td><p><span data-ttu-id="8ebe2-124">Шрифт, используемый для отображения значения ячейки.</span><span class="sxs-lookup"><span data-stu-id="8ebe2-124">Font used to display the cell value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ebe2-125">FontSize</span><span class="sxs-lookup"><span data-stu-id="8ebe2-125">FontSize</span></span></p></td>
<td><p><span data-ttu-id="8ebe2-126">Размер шрифта, используемый для отображения значения ячейки.</span><span class="sxs-lookup"><span data-stu-id="8ebe2-126">Font size used to display the cell value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ebe2-127">Цвет текста</span><span class="sxs-lookup"><span data-stu-id="8ebe2-127">ForeColor</span></span></p></td>
<td><p><span data-ttu-id="8ebe2-128">Цвет переднего плана, используемый при отображении ячейки.</span><span class="sxs-lookup"><span data-stu-id="8ebe2-128">Foreground color used when displaying the cell.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ebe2-129">FormatString</span><span class="sxs-lookup"><span data-stu-id="8ebe2-129">FormatString</span></span></p></td>
<td><p><span data-ttu-id="8ebe2-130">Значение в формате строки.</span><span class="sxs-lookup"><span data-stu-id="8ebe2-130">Value in a formatted string.</span></span></p></td>
</tr>
</tbody>
</table>

