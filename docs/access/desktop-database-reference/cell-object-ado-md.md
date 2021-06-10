---
title: Объект Cell (ADO MD)
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
# <a name="cell-object-ado-md"></a><span data-ttu-id="28b9a-102">Объект Cell (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="28b9a-102">Cell object (ADO MD)</span></span>


<span data-ttu-id="28b9a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28b9a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28b9a-104">Представляет данные на пересечении координат оси, содержащихся в ячейке.</span><span class="sxs-lookup"><span data-stu-id="28b9a-104">Represents the data at the intersection of axis coordinates contained in a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="28b9a-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="28b9a-105">Remarks</span></span>

<span data-ttu-id="28b9a-106">Объект **Cell** возвращается [свойством Item](item-property-ado-md-cellset.md) объекта [Cellset.](cellset-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="28b9a-106">A **Cell** object is returned by the [Item](item-property-ado-md-cellset.md) property of a [Cellset](cellset-object-ado-md.md) object.</span></span>

<span data-ttu-id="28b9a-107">С коллекциями и свойствами объекта **Cell** можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="28b9a-107">With the collections and properties of a **Cell** object, you can do the following:</span></span>

- <span data-ttu-id="28b9a-108">Возвращаем данные в **ячейке** с [свойством Value.](value-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="28b9a-108">Return the data in the **Cell** with the [Value](value-property-ado-md.md) property.</span></span>

- <span data-ttu-id="28b9a-109">Верни строку, представляющую форматированный дисплей свойства **Value** с [свойством FormattedValue.](formattedvalue-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="28b9a-109">Return the string representing the formatted display of the **Value** property with the [FormattedValue](formattedvalue-property-ado-md.md) property.</span></span>

- <span data-ttu-id="28b9a-110">Возврат ordinal значения **ячейки** в **ячейках с** [свойством Ordinal.](ordinal-property-ado-md-cell.md)</span><span class="sxs-lookup"><span data-stu-id="28b9a-110">Return the ordinal value of the **Cell** within the **Cellset** with the [Ordinal](ordinal-property-ado-md-cell.md) property.</span></span>

- <span data-ttu-id="28b9a-111">Определите положение **ячейки** в [CubeDef](cubedef-object-ado-md.md) с коллекцией [Positions.](positions-collection-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="28b9a-111">Determine the position of the **Cell** within the [CubeDef](cubedef-object-ado-md.md) with the [Positions](positions-collection-ado-md.md) collection.</span></span>

- <span data-ttu-id="28b9a-112">Извлечение других сведений о **ячейке** с помощью стандартной коллекции свойств [ADO.](properties-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="28b9a-112">Retrieve other information about the **Cell** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="28b9a-113">Коллекция **свойств** содержит свойства, предоставленные поставщиком.</span><span class="sxs-lookup"><span data-stu-id="28b9a-113">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="28b9a-114">В следующей таблице перечислены свойства, которые могут быть доступны.</span><span class="sxs-lookup"><span data-stu-id="28b9a-114">The following table lists properties that might be available.</span></span> <span data-ttu-id="28b9a-115">Фактический список свойств может отличаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="28b9a-115">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="28b9a-116">Дополнительный список доступных свойств см. в документации для поставщика.</span><span class="sxs-lookup"><span data-stu-id="28b9a-116">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28b9a-117">Имя</span><span class="sxs-lookup"><span data-stu-id="28b9a-117">Name</span></span></p></th>
<th><p><span data-ttu-id="28b9a-118">Описание</span><span class="sxs-lookup"><span data-stu-id="28b9a-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28b9a-119">BackColor</span><span class="sxs-lookup"><span data-stu-id="28b9a-119">BackColor</span></span></p></td>
<td><p><span data-ttu-id="28b9a-120">Фоновый цвет, используемый при отобраии ячейки.</span><span class="sxs-lookup"><span data-stu-id="28b9a-120">Background color used when displaying the cell.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28b9a-121">FontFlags</span><span class="sxs-lookup"><span data-stu-id="28b9a-121">FontFlags</span></span></p></td>
<td><p><span data-ttu-id="28b9a-122">Bitmask подробное воздействие на шрифт.</span><span class="sxs-lookup"><span data-stu-id="28b9a-122">Bitmask detailing effects on the font.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28b9a-123">FontName</span><span class="sxs-lookup"><span data-stu-id="28b9a-123">FontName</span></span></p></td>
<td><p><span data-ttu-id="28b9a-124">Шрифт, используемый для отображения значения ячейки.</span><span class="sxs-lookup"><span data-stu-id="28b9a-124">Font used to display the cell value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28b9a-125">FontSize</span><span class="sxs-lookup"><span data-stu-id="28b9a-125">FontSize</span></span></p></td>
<td><p><span data-ttu-id="28b9a-126">Размер шрифта, используемый для отображения значения ячейки.</span><span class="sxs-lookup"><span data-stu-id="28b9a-126">Font size used to display the cell value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28b9a-127">ForeColor</span><span class="sxs-lookup"><span data-stu-id="28b9a-127">ForeColor</span></span></p></td>
<td><p><span data-ttu-id="28b9a-128">Цвет переднего плана, используемый при отображение ячейки.</span><span class="sxs-lookup"><span data-stu-id="28b9a-128">Foreground color used when displaying the cell.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28b9a-129">FormatString</span><span class="sxs-lookup"><span data-stu-id="28b9a-129">FormatString</span></span></p></td>
<td><p><span data-ttu-id="28b9a-130">Значение в отформатированной строке.</span><span class="sxs-lookup"><span data-stu-id="28b9a-130">Value in a formatted string.</span></span></p></td>
</tr>
</tbody>
</table>

