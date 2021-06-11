---
title: SortKey Cell (Shape Data Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251345
localization_priority: Normal
ms.assetid: 67fa5389-f0b9-a9db-8d19-9b16e256dfa3
description: Оценивает строку, которая влияет на порядок, в котором перечислены элементы в окне Shape Data.
ms.openlocfilehash: d166ea18a36f6a4101b8933fce804be2243954bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417856"
---
# <a name="sortkey-cell-shape-data-section"></a><span data-ttu-id="5d719-103">SortKey Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="5d719-103">SortKey Cell (Shape Data Section)</span></span>

<span data-ttu-id="5d719-104">Оценивает строку, которая влияет на порядок, в котором перечислены элементы в окне **Shape Data.**</span><span class="sxs-lookup"><span data-stu-id="5d719-104">Evaluates to a string that influences the order in which items in the **Shape Data** window are listed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5d719-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="5d719-105">Remarks</span></span>

<span data-ttu-id="5d719-106">Расчет, используемый для сравнения значений SortKey, является локальным и нечувствительным.</span><span class="sxs-lookup"><span data-stu-id="5d719-106">The calculation used to compare SortKey values is locale-specific and case insensitive.</span></span> <span data-ttu-id="5d719-107">Если значения SortKey равны, данные фигуры перечислены в порядке строки.</span><span class="sxs-lookup"><span data-stu-id="5d719-107">If SortKey values are equal, the shape data is listed in row order.</span></span> <span data-ttu-id="5d719-108">Фигуры данных, не содержащих ключ сортировки, перечислены после данных фигуры, содержащих ключ сортировки.</span><span class="sxs-lookup"><span data-stu-id="5d719-108">Shape data that have no sort key are listed after shape data that contain a sort key.</span></span>
  
<span data-ttu-id="5d719-109">Ниже приводится пример использования ключей сортировки для отображения данных фигуры в окне **Shape Data** в порядке: номер элемента, количество, цена.</span><span class="sxs-lookup"><span data-stu-id="5d719-109">Following is an example of using sort keys to display the shape data in the **Shape Data** window in the order: Item Number, Quantity, Price.</span></span> 
  
 <span data-ttu-id="5d719-110">*Строка, метка*  и  *SortKey*  относятся к ячейкам в строке данных фигуры.</span><span class="sxs-lookup"><span data-stu-id="5d719-110">*Row, Label,*  and  *SortKey*  refer to cells in the shape data row.</span></span> <span data-ttu-id="5d719-111">В этом случае строки данных фигуры были названы.</span><span class="sxs-lookup"><span data-stu-id="5d719-111">In this case, the shape data rows have been named.</span></span> 
  
|<span data-ttu-id="5d719-112">**Row**</span><span class="sxs-lookup"><span data-stu-id="5d719-112">**Row**</span></span>|<span data-ttu-id="5d719-113">**Label**</span><span class="sxs-lookup"><span data-stu-id="5d719-113">**Label**</span></span>|<span data-ttu-id="5d719-114">**SortKey**</span><span class="sxs-lookup"><span data-stu-id="5d719-114">**SortKey**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="5d719-115">Prop.Item</span><span class="sxs-lookup"><span data-stu-id="5d719-115">Prop.Item</span></span>  <br/> | <span data-ttu-id="5d719-116">Номер элемента</span><span class="sxs-lookup"><span data-stu-id="5d719-116">Item Number</span></span>  <br/> | <span data-ttu-id="5d719-117">1</span><span class="sxs-lookup"><span data-stu-id="5d719-117">1</span></span>  <br/> |
| <span data-ttu-id="5d719-118">Prop.Price</span><span class="sxs-lookup"><span data-stu-id="5d719-118">Prop.Price</span></span>  <br/> | <span data-ttu-id="5d719-119">ЦЕНА</span><span class="sxs-lookup"><span data-stu-id="5d719-119">Price</span></span>  <br/> | <span data-ttu-id="5d719-120">3</span><span class="sxs-lookup"><span data-stu-id="5d719-120">3</span></span>  <br/> |
| <span data-ttu-id="5d719-121">Prop.Quan</span><span class="sxs-lookup"><span data-stu-id="5d719-121">Prop.Quan</span></span>  <br/> | <span data-ttu-id="5d719-122">Количество</span><span class="sxs-lookup"><span data-stu-id="5d719-122">Quantity</span></span>  <br/> | <span data-ttu-id="5d719-123">2</span><span class="sxs-lookup"><span data-stu-id="5d719-123">2</span></span>  <br/> |
   
<span data-ttu-id="5d719-124">Чтобы получить ссылку на ячейку SortKey по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="5d719-124">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5d719-125">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="5d719-125">Cell name:</span></span>  <br/> | <span data-ttu-id="5d719-126">Prop.  *Имя*  . SortKey where Prop.  *Имя*  — это имя настраиваемой строки свойств</span><span class="sxs-lookup"><span data-stu-id="5d719-126">Prop.  *Name*  .SortKey where Prop.  *Name*  is the name of the custom property row</span></span>  <br/> |
   
<span data-ttu-id="5d719-127">Чтобы получить ссылку на ячейку SortKey по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="5d719-127">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5d719-128">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5d719-128">Section index:</span></span>  <br/> |<span data-ttu-id="5d719-129">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="5d719-129">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="5d719-130">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5d719-130">Row index:</span></span>  <br/> |<span data-ttu-id="5d719-131">**visRowProp**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="5d719-131">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5d719-132">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5d719-132">Cell index:</span></span>  <br/> |<span data-ttu-id="5d719-133">**visCustPropsSortKey**</span><span class="sxs-lookup"><span data-stu-id="5d719-133">**visCustPropsSortKey**</span></span> <br/> |
   

