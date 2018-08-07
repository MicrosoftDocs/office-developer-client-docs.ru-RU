---
title: Ячейка Invisible (раздел "Данные фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251341
localization_priority: Normal
ms.assetid: 5f368c2e-2a40-38ee-3568-ed5c57633345
description: Указывает, видима ли данные фигуры в окне данных фигуры.
ms.openlocfilehash: 2cd3fcad5db7b1752c55055354f1ec842bff4899
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813969"
---
# <a name="invisible-cell-shape-data-section"></a><span data-ttu-id="c6e68-103">Ячейка Invisible (раздел "Данные фигуры")</span><span class="sxs-lookup"><span data-stu-id="c6e68-103">Invisible Cell (Shape Data Section)</span></span>

<span data-ttu-id="c6e68-104">Указывает, видима ли данные фигуры в окне **Данных фигуры** .</span><span class="sxs-lookup"><span data-stu-id="c6e68-104">Specifies whether the shape data item is visible in the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="c6e68-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c6e68-105">**Value**</span></span>|<span data-ttu-id="c6e68-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c6e68-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c6e68-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c6e68-107">TRUE</span></span>  <br/> | <span data-ttu-id="c6e68-108">Данные фигуры не отображается.</span><span class="sxs-lookup"><span data-stu-id="c6e68-108">Shape data item is not visible.</span></span>  <br/> |
| <span data-ttu-id="c6e68-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c6e68-109">FALSE</span></span>  <br/> | <span data-ttu-id="c6e68-110">Данные фигуры является видимым.</span><span class="sxs-lookup"><span data-stu-id="c6e68-110">Shape data item is visible.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6e68-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="c6e68-111">Remarks</span></span>

<span data-ttu-id="c6e68-112">Значение в этой ячейке соответствующий флажок **скрытый** в диалоговом окне **Определение данных фигуры** (щелкните правой кнопкой мыши фигуру, выберите пункт **данные**и выберите **Определение данных фигуры**).</span><span class="sxs-lookup"><span data-stu-id="c6e68-112">The value in this cell corresponds to the **Hidden** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="c6e68-113">Для получения ссылки на ячейки невидимой по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="c6e68-113">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c6e68-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="c6e68-114">Cell name:</span></span>  <br/> | <span data-ttu-id="c6e68-115">Свойства.  *имя* . Невидимое where свойств.  *имя* — это имя строки</span><span class="sxs-lookup"><span data-stu-id="c6e68-115">Prop.  *name*  .Invisible where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="c6e68-116">Для получения ссылки на ячейки невидимой по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="c6e68-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c6e68-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c6e68-117">Section index:</span></span>  <br/> |<span data-ttu-id="c6e68-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="c6e68-118">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="c6e68-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c6e68-119">Row index:</span></span>  <br/> |<span data-ttu-id="c6e68-120">**visRowProp** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c6e68-120">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c6e68-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c6e68-121">Cell index:</span></span>  <br/> |<span data-ttu-id="c6e68-122">**visCustPropsInvis**</span><span class="sxs-lookup"><span data-stu-id="c6e68-122">**visCustPropsInvis**</span></span> <br/> |
   

