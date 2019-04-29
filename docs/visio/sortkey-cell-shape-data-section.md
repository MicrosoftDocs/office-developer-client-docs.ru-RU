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
description: Оценивается как строка, которая влияет на порядок, в котором отображаются элементы в окне "данные фигуры".
ms.openlocfilehash: d166ea18a36f6a4101b8933fce804be2243954bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417856"
---
# <a name="sortkey-cell-shape-data-section"></a><span data-ttu-id="61ea0-103">SortKey Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="61ea0-103">SortKey Cell (Shape Data Section)</span></span>

<span data-ttu-id="61ea0-104">Оценивается как строка, которая влияет на порядок, в котором отображаются элементы в окне " **данные фигуры** ".</span><span class="sxs-lookup"><span data-stu-id="61ea0-104">Evaluates to a string that influences the order in which items in the **Shape Data** window are listed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="61ea0-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="61ea0-105">Remarks</span></span>

<span data-ttu-id="61ea0-106">Вычисление, используемое для сравнения значений SortKey, зависит от языкового стандарта и без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="61ea0-106">The calculation used to compare SortKey values is locale-specific and case insensitive.</span></span> <span data-ttu-id="61ea0-107">Если значения SortKey совпадают, данные фигуры отображаются в порядке строк.</span><span class="sxs-lookup"><span data-stu-id="61ea0-107">If SortKey values are equal, the shape data is listed in row order.</span></span> <span data-ttu-id="61ea0-108">Данные фигуры, у которых нет ключа сортировки, указаны после данных фигуры, содержащих ключ сортировки.</span><span class="sxs-lookup"><span data-stu-id="61ea0-108">Shape data that have no sort key are listed after shape data that contain a sort key.</span></span>
  
<span data-ttu-id="61ea0-109">Ниже приведен пример использования ключей сортировки для отображения данных фигуры в окне " **данные фигуры** " в порядке: "номер товара", "количество", "цена".</span><span class="sxs-lookup"><span data-stu-id="61ea0-109">Following is an example of using sort keys to display the shape data in the **Shape Data** window in the order: Item Number, Quantity, Price.</span></span> 
  
 <span data-ttu-id="61ea0-110">*Строка, подпись* и *SortKey* ссылаются на ячейки в строке данных фигуры.</span><span class="sxs-lookup"><span data-stu-id="61ea0-110">*Row, Label,*  and  *SortKey*  refer to cells in the shape data row.</span></span> <span data-ttu-id="61ea0-111">В этом случае были именованы строки данных фигуры.</span><span class="sxs-lookup"><span data-stu-id="61ea0-111">In this case, the shape data rows have been named.</span></span> 
  
|<span data-ttu-id="61ea0-112">**Row**</span><span class="sxs-lookup"><span data-stu-id="61ea0-112">**Row**</span></span>|<span data-ttu-id="61ea0-113">**Label**</span><span class="sxs-lookup"><span data-stu-id="61ea0-113">**Label**</span></span>|<span data-ttu-id="61ea0-114">**SortKey**</span><span class="sxs-lookup"><span data-stu-id="61ea0-114">**SortKey**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="61ea0-115">Prop. Item</span><span class="sxs-lookup"><span data-stu-id="61ea0-115">Prop.Item</span></span>  <br/> | <span data-ttu-id="61ea0-116">Номер элемента</span><span class="sxs-lookup"><span data-stu-id="61ea0-116">Item Number</span></span>  <br/> | <span data-ttu-id="61ea0-117">1,1</span><span class="sxs-lookup"><span data-stu-id="61ea0-117">1</span></span>  <br/> |
| <span data-ttu-id="61ea0-118">Prop. Price</span><span class="sxs-lookup"><span data-stu-id="61ea0-118">Prop.Price</span></span>  <br/> | <span data-ttu-id="61ea0-119">ЦЕНА</span><span class="sxs-lookup"><span data-stu-id="61ea0-119">Price</span></span>  <br/> | <span data-ttu-id="61ea0-120">4</span><span class="sxs-lookup"><span data-stu-id="61ea0-120">3</span></span>  <br/> |
| <span data-ttu-id="61ea0-121">Prop. Куан</span><span class="sxs-lookup"><span data-stu-id="61ea0-121">Prop.Quan</span></span>  <br/> | <span data-ttu-id="61ea0-122">Количество</span><span class="sxs-lookup"><span data-stu-id="61ea0-122">Quantity</span></span>  <br/> | <span data-ttu-id="61ea0-123">2</span><span class="sxs-lookup"><span data-stu-id="61ea0-123">2</span></span>  <br/> |
   
<span data-ttu-id="61ea0-124">Чтобы получить ссылку на ячейку SortKey по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="61ea0-124">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="61ea0-125">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="61ea0-125">Cell name:</span></span>  <br/> | <span data-ttu-id="61ea0-126">Установите.  *Name (имя* ). SortKey, где prop.  *Name* — имя строки настраиваемого свойства</span><span class="sxs-lookup"><span data-stu-id="61ea0-126">Prop.  *Name*  .SortKey where Prop.  *Name*  is the name of the custom property row</span></span>  <br/> |
   
<span data-ttu-id="61ea0-127">Чтобы получить ссылку на ячейку SortKey по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="61ea0-127">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="61ea0-128">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="61ea0-128">Section index:</span></span>  <br/> |<span data-ttu-id="61ea0-129">**Виссектионпроп**</span><span class="sxs-lookup"><span data-stu-id="61ea0-129">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="61ea0-130">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="61ea0-130">Row index:</span></span>  <br/> |<span data-ttu-id="61ea0-131">**висровпроп** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="61ea0-131">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="61ea0-132">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="61ea0-132">Cell index:</span></span>  <br/> |<span data-ttu-id="61ea0-133">**Вискустпропссорткэй**</span><span class="sxs-lookup"><span data-stu-id="61ea0-133">**visCustPropsSortKey**</span></span> <br/> |
   

