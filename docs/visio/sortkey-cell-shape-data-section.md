---
title: Ячейка SortKey (раздел "Данные фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251345
localization_priority: Normal
ms.assetid: 67fa5389-f0b9-a9db-8d19-9b16e256dfa3
description: Представляет собой строку, которая влияет на порядок, в котором перечислены элементы в окне данных фигуры.
ms.openlocfilehash: 1dbc093f2cee509531b8148563fbdb1a777a349f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814928"
---
# <a name="sortkey-cell-shape-data-section"></a><span data-ttu-id="d4846-103">Ячейка SortKey (раздел "Данные фигуры")</span><span class="sxs-lookup"><span data-stu-id="d4846-103">SortKey Cell (Shape Data Section)</span></span>

<span data-ttu-id="d4846-104">Представляет собой строку, которая влияет на порядок, в котором перечислены элементы в окне **Данных фигуры** .</span><span class="sxs-lookup"><span data-stu-id="d4846-104">Evaluates to a string that influences the order in which items in the **Shape Data** window are listed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d4846-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="d4846-105">Remarks</span></span>

<span data-ttu-id="d4846-106">Вычисления, используется для сравнения значения SortKey языкового стандарта и без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="d4846-106">The calculation used to compare SortKey values is locale-specific and case insensitive.</span></span> <span data-ttu-id="d4846-107">Если значения SortKey равны, данные фигуры указано в порядок строк.</span><span class="sxs-lookup"><span data-stu-id="d4846-107">If SortKey values are equal, the shape data is listed in row order.</span></span> <span data-ttu-id="d4846-108">Данные фигуры, которые имеют ключ не сортировки перечислены после данных фигуры, которая содержит ключ сортировки.</span><span class="sxs-lookup"><span data-stu-id="d4846-108">Shape data that have no sort key are listed after shape data that contain a sort key.</span></span>
  
<span data-ttu-id="d4846-109">Ниже приведен пример использования ключей сортировки для отображения данных фигуры в окне **Данных фигуры** в порядке: номер товара, количество, цена.</span><span class="sxs-lookup"><span data-stu-id="d4846-109">Following is an example of using sort keys to display the shape data in the **Shape Data** window in the order: Item Number, Quantity, Price.</span></span> 
  
 <span data-ttu-id="d4846-110">*Строки, метки* и *SortKey* обращение к ячейкам в строке данных фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4846-110">*Row, Label,*  and  *SortKey*  refer to cells in the shape data row.</span></span> <span data-ttu-id="d4846-111">В этом случае имя строк данных фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4846-111">In this case, the shape data rows have been named.</span></span> 
  
|<span data-ttu-id="d4846-112">**Row**</span><span class="sxs-lookup"><span data-stu-id="d4846-112">**Row**</span></span>|<span data-ttu-id="d4846-113">**Подпись**</span><span class="sxs-lookup"><span data-stu-id="d4846-113">**Label**</span></span>|<span data-ttu-id="d4846-114">**SortKey**</span><span class="sxs-lookup"><span data-stu-id="d4846-114">**SortKey**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="d4846-115">Prop.Item</span><span class="sxs-lookup"><span data-stu-id="d4846-115">Prop.Item</span></span>  <br/> | <span data-ttu-id="d4846-116">Номер элемента</span><span class="sxs-lookup"><span data-stu-id="d4846-116">Item Number</span></span>  <br/> | <span data-ttu-id="d4846-117">1</span><span class="sxs-lookup"><span data-stu-id="d4846-117">1</span></span>  <br/> |
| <span data-ttu-id="d4846-118">Prop.Price</span><span class="sxs-lookup"><span data-stu-id="d4846-118">Prop.Price</span></span>  <br/> | <span data-ttu-id="d4846-119">Цены</span><span class="sxs-lookup"><span data-stu-id="d4846-119">Price</span></span>  <br/> | <span data-ttu-id="d4846-120">3</span><span class="sxs-lookup"><span data-stu-id="d4846-120">3</span></span>  <br/> |
| <span data-ttu-id="d4846-121">Prop.Quan</span><span class="sxs-lookup"><span data-stu-id="d4846-121">Prop.Quan</span></span>  <br/> | <span data-ttu-id="d4846-122">"Quantity" (Количество)</span><span class="sxs-lookup"><span data-stu-id="d4846-122">Quantity</span></span>  <br/> | <span data-ttu-id="d4846-123">2</span><span class="sxs-lookup"><span data-stu-id="d4846-123">2</span></span>  <br/> |
   
<span data-ttu-id="d4846-124">Чтобы получить ссылку на ячейку SortKey по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d4846-124">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d4846-125">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="d4846-125">Cell name:</span></span>  <br/> | <span data-ttu-id="d4846-126">Свойства.  *Имя* . SortKey где свойств.  *Имя* — это имя настраиваемого свойства строки</span><span class="sxs-lookup"><span data-stu-id="d4846-126">Prop.  *Name*  .SortKey where Prop.  *Name*  is the name of the custom property row</span></span>  <br/> |
   
<span data-ttu-id="d4846-127">Для получения ссылки на ячейки SortKey по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="d4846-127">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d4846-128">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d4846-128">Section index:</span></span>  <br/> |<span data-ttu-id="d4846-129">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="d4846-129">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="d4846-130">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d4846-130">Row index:</span></span>  <br/> |<span data-ttu-id="d4846-131">**visRowProp** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d4846-131">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d4846-132">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d4846-132">Cell index:</span></span>  <br/> |<span data-ttu-id="d4846-133">**visCustPropsSortKey**</span><span class="sxs-lookup"><span data-stu-id="d4846-133">**visCustPropsSortKey**</span></span> <br/> |
   

