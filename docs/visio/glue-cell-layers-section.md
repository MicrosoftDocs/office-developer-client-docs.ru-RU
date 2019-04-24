---
title: Glue Cell (Layers Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm415
localization_priority: Normal
ms.assetid: 75f2ea45-52ac-ddfa-14ea-402933ae2449
description: Указывает, можно ли склеить фигуры, принадлежащие слою.
ms.openlocfilehash: 55886a7e96bd2c08966cb85f5edad6a7174e30cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332811"
---
# <a name="glue-cell-layers-section"></a><span data-ttu-id="d46c4-103">Glue Cell (Layers Section)</span><span class="sxs-lookup"><span data-stu-id="d46c4-103">Glue Cell (Layers Section)</span></span>

<span data-ttu-id="d46c4-104">Указывает, можно ли склеить фигуры, принадлежащие слою.</span><span class="sxs-lookup"><span data-stu-id="d46c4-104">Specifies whether shapes belonging to the layer can be glued.</span></span>
  
|<span data-ttu-id="d46c4-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="d46c4-105">**Value**</span></span>|<span data-ttu-id="d46c4-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d46c4-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d46c4-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d46c4-107">TRUE</span></span>  <br/> |<span data-ttu-id="d46c4-108">Включена функция приклеивание.</span><span class="sxs-lookup"><span data-stu-id="d46c4-108">Glue is enabled.</span></span>  <br/> |
|<span data-ttu-id="d46c4-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d46c4-109">FALSE</span></span>  <br/> |<span data-ttu-id="d46c4-110">Приклеивание отключена.</span><span class="sxs-lookup"><span data-stu-id="d46c4-110">Glue is disabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d46c4-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d46c4-111">Remarks</span></span>

<span data-ttu-id="d46c4-112">Эта ячейка соответствует параметру "приКлеить" в диалоговом окне **Свойства слоя** (на вкладке **Главная** , в группе **Правка** щелкните **слои**, а затем выберите **Свойства слоя** ). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d46c4-112">This cell corresponds to the **Glue** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="d46c4-113">Чтобы получить ссылку на ячейку с приКреплением по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="d46c4-113">To get a reference to the Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d46c4-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d46c4-114">Cell name:</span></span>  <br/> |<span data-ttu-id="d46c4-115">Layers. приклеивание [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d46c4-115">Layers.Glue[  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d46c4-116">Чтобы получить ссылку на ячейку с приКреплением по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d46c4-116">To get a reference to the Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d46c4-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d46c4-117">Section index:</span></span>  <br/> |<span data-ttu-id="d46c4-118">**Виссектионлайер**</span><span class="sxs-lookup"><span data-stu-id="d46c4-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="d46c4-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d46c4-119">Row index:</span></span>  <br/> |<span data-ttu-id="d46c4-120">**висровлайер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d46c4-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d46c4-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d46c4-121">Cell index:</span></span>  <br/> |<span data-ttu-id="d46c4-122">**Вислайерглуе**</span><span class="sxs-lookup"><span data-stu-id="d46c4-122">**visLayerGlue**</span></span> <br/> |
   

