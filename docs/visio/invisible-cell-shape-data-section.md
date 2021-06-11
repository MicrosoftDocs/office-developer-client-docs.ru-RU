---
title: Invisible Cell (Shape Data Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251341
localization_priority: Normal
ms.assetid: 5f368c2e-2a40-38ee-3568-ed5c57633345
description: Указывает, виден ли элемент данных фигуры в окне Shape Data.
ms.openlocfilehash: 8671fcc249b7ca81c011f697721093e7842c1558
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405319"
---
# <a name="invisible-cell-shape-data-section"></a><span data-ttu-id="520d3-103">Invisible Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="520d3-103">Invisible Cell (Shape Data Section)</span></span>

<span data-ttu-id="520d3-104">Указывает, виден ли элемент данных фигуры в **окне Shape Data.**</span><span class="sxs-lookup"><span data-stu-id="520d3-104">Specifies whether the shape data item is visible in the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="520d3-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="520d3-105">**Value**</span></span>|<span data-ttu-id="520d3-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="520d3-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="520d3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="520d3-107">TRUE</span></span>  <br/> | <span data-ttu-id="520d3-108">Элемент фигуры данных не виден.</span><span class="sxs-lookup"><span data-stu-id="520d3-108">Shape data item is not visible.</span></span>  <br/> |
| <span data-ttu-id="520d3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="520d3-109">FALSE</span></span>  <br/> | <span data-ttu-id="520d3-110">Видна фигура элемента данных.</span><span class="sxs-lookup"><span data-stu-id="520d3-110">Shape data item is visible.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="520d3-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="520d3-111">Remarks</span></span>

<span data-ttu-id="520d3-112">Значение в этой ячейке  соответствует скрытому чековом окну в диалоговом окне **Define Shape Data** (щелкните правой кнопкой мыши фигуру, указать на **данные,** а затем нажмите кнопку **Определить данные фигуры).**</span><span class="sxs-lookup"><span data-stu-id="520d3-112">The value in this cell corresponds to the **Hidden** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="520d3-113">Чтобы получить ссылку на невидимую ячейку по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="520d3-113">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="520d3-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="520d3-114">Cell name:</span></span>  <br/> | <span data-ttu-id="520d3-115">Prop.  *имя*  . Невидимый, где Prop.  *имя*  — это имя строки</span><span class="sxs-lookup"><span data-stu-id="520d3-115">Prop.  *name*  .Invisible where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="520d3-116">Чтобы получить ссылку на невидимую ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="520d3-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="520d3-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="520d3-117">Section index:</span></span>  <br/> |<span data-ttu-id="520d3-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="520d3-118">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="520d3-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="520d3-119">Row index:</span></span>  <br/> |<span data-ttu-id="520d3-120">**visRowProp**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="520d3-120">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="520d3-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="520d3-121">Cell index:</span></span>  <br/> |<span data-ttu-id="520d3-122">**visCustPropsInvis**</span><span class="sxs-lookup"><span data-stu-id="520d3-122">**visCustPropsInvis**</span></span> <br/> |
   

