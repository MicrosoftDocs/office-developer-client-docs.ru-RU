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
# <a name="cell-object-ado-md"></a><span data-ttu-id="fedad-102">Объект Cell (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="fedad-102">Cell object (ADO MD)</span></span>


<span data-ttu-id="fedad-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fedad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fedad-104">Представляет данные на пересечении координат оси, содержащегося в наборе ячеек.</span><span class="sxs-lookup"><span data-stu-id="fedad-104">Represents the data at the intersection of axis coordinates contained in a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="fedad-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="fedad-105">Remarks</span></span>

<span data-ttu-id="fedad-106">Объект **Cell** возвращается свойством [Item](item-property-ado-md-cellset.md) объекта набора [ячеек](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="fedad-106">A **Cell** object is returned by the [Item](item-property-ado-md-cellset.md) property of a [Cellset](cellset-object-ado-md.md) object.</span></span>

<span data-ttu-id="fedad-107">С помощью коллекций и свойств объекта **Cell** можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="fedad-107">With the collections and properties of a **Cell** object, you can do the following:</span></span>

- <span data-ttu-id="fedad-108">Возвращает данные в **ячейке** со свойством [value](value-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="fedad-108">Return the data in the **Cell** with the [Value](value-property-ado-md.md) property.</span></span>

- <span data-ttu-id="fedad-109">Возвращает строку, представляющую отформатированное отображение свойства **value** со свойством [FormattedValue](formattedvalue-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="fedad-109">Return the string representing the formatted display of the **Value** property with the [FormattedValue](formattedvalue-property-ado-md.md) property.</span></span>

- <span data-ttu-id="fedad-110">Возвращает порядковый номер **ячейки** в наборе **ячеек** с помощью свойства [Ordinal](ordinal-property-ado-md-cell.md) .</span><span class="sxs-lookup"><span data-stu-id="fedad-110">Return the ordinal value of the **Cell** within the **Cellset** with the [Ordinal](ordinal-property-ado-md-cell.md) property.</span></span>

- <span data-ttu-id="fedad-111">Определите положение **ячейки** в [CubeDef](cubedef-object-ado-md.md) с помощью коллекции [Positions](positions-collection-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="fedad-111">Determine the position of the **Cell** within the [CubeDef](cubedef-object-ado-md.md) with the [Positions](positions-collection-ado-md.md) collection.</span></span>

- <span data-ttu-id="fedad-112">Получение других сведений о **ячейке** с помощью стандартной коллекции [свойств](properties-collection-ado.md) ADO.</span><span class="sxs-lookup"><span data-stu-id="fedad-112">Retrieve other information about the **Cell** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="fedad-113">Коллекция **Properties** содержит свойства, предоставляемые поставщиком.</span><span class="sxs-lookup"><span data-stu-id="fedad-113">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="fedad-114">В следующей таблице перечислены свойства, которые могут быть доступны.</span><span class="sxs-lookup"><span data-stu-id="fedad-114">The following table lists properties that might be available.</span></span> <span data-ttu-id="fedad-115">Фактический список свойств может различаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="fedad-115">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="fedad-116">Просмотрите документацию для своего поставщика, чтобы получить полный список доступных свойств.</span><span class="sxs-lookup"><span data-stu-id="fedad-116">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fedad-117">Имя</span><span class="sxs-lookup"><span data-stu-id="fedad-117">Name</span></span></p></th>
<th><p><span data-ttu-id="fedad-118">Описание</span><span class="sxs-lookup"><span data-stu-id="fedad-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fedad-119">BackColor</span><span class="sxs-lookup"><span data-stu-id="fedad-119">BackColor</span></span></p></td>
<td><p><span data-ttu-id="fedad-120">Цвет фона, используемый при отображении ячейки.</span><span class="sxs-lookup"><span data-stu-id="fedad-120">Background color used when displaying the cell.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fedad-121">фонтфлагс</span><span class="sxs-lookup"><span data-stu-id="fedad-121">FontFlags</span></span></p></td>
<td><p><span data-ttu-id="fedad-122">Битовая анимация на шрифте.</span><span class="sxs-lookup"><span data-stu-id="fedad-122">Bitmask detailing effects on the font.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fedad-123">FontName</span><span class="sxs-lookup"><span data-stu-id="fedad-123">FontName</span></span></p></td>
<td><p><span data-ttu-id="fedad-124">Шрифт, используемый для отображения значения ячейки.</span><span class="sxs-lookup"><span data-stu-id="fedad-124">Font used to display the cell value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fedad-125">FontSize</span><span class="sxs-lookup"><span data-stu-id="fedad-125">FontSize</span></span></p></td>
<td><p><span data-ttu-id="fedad-126">Размер шрифта, используемого для отображения значения ячейки.</span><span class="sxs-lookup"><span data-stu-id="fedad-126">Font size used to display the cell value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fedad-127">ForeColor</span><span class="sxs-lookup"><span data-stu-id="fedad-127">ForeColor</span></span></p></td>
<td><p><span data-ttu-id="fedad-128">Цвет переднего плана, используемый при отображении ячейки.</span><span class="sxs-lookup"><span data-stu-id="fedad-128">Foreground color used when displaying the cell.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fedad-129">FormatString</span><span class="sxs-lookup"><span data-stu-id="fedad-129">FormatString</span></span></p></td>
<td><p><span data-ttu-id="fedad-130">Значение в форматированной строке.</span><span class="sxs-lookup"><span data-stu-id="fedad-130">Value in a formatted string.</span></span></p></td>
</tr>
</tbody>
</table>

