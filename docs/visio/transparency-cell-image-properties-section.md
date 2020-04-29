---
title: Transparency Cell (Image Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51095
localization_priority: Normal
ms.assetid: 5b265356-1602-4241-fbe1-4d5a55392a52
description: Определяет уровень прозрачности для цвета слоя.
ms.openlocfilehash: defe5307e57c433fcf85a4132939d08cb1ddec77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405837"
---
# <a name="transparency-cell-image-properties-section"></a><span data-ttu-id="a0726-103">Transparency Cell (Image Properties Section)</span><span class="sxs-lookup"><span data-stu-id="a0726-103">Transparency Cell (Image Properties Section)</span></span>

<span data-ttu-id="a0726-104">Определяет уровень прозрачности для цвета слоя.</span><span class="sxs-lookup"><span data-stu-id="a0726-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="a0726-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a0726-105">**Value**</span></span>|<span data-ttu-id="a0726-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a0726-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a0726-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="a0726-107">0 - 100</span></span>  <br/> |<span data-ttu-id="a0726-108">Представляет процент прозрачности.</span><span class="sxs-lookup"><span data-stu-id="a0726-108">Represents the percentage of transparency.</span></span> <span data-ttu-id="a0726-109">Значение по умолчанию: 0% (полностью непрозрачно).</span><span class="sxs-lookup"><span data-stu-id="a0726-109">The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0726-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="a0726-110">Remarks</span></span>

<span data-ttu-id="a0726-111">Значения округляются до ближайшей половины процентов.</span><span class="sxs-lookup"><span data-stu-id="a0726-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="a0726-112">Значение 100% полностью прозрачно.</span><span class="sxs-lookup"><span data-stu-id="a0726-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="a0726-113">Несмотря на то, что слой с полностью прозрачным цветом отображается на странице документа как слой без цвета, он взаимодействует с другими объектами на странице так же, как если бы его прозрачность была равна 0%.</span><span class="sxs-lookup"><span data-stu-id="a0726-113">Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span> <span data-ttu-id="a0726-114">Это значение можно также задать с помощью ползунка в диалоговом окне **Свойства слоя** (на вкладке **Главная** , в группе **Правка** щелкните **слои**, а затем выберите **Свойства слоя**).</span><span class="sxs-lookup"><span data-stu-id="a0726-114">You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="a0726-115">Чтобы получить ссылку на ячейку прозрачности по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="a0726-115">To get a reference to the Transparency cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0726-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="a0726-116">Cell name:</span></span>  <br/> |<span data-ttu-id="a0726-117">Прозрачность</span><span class="sxs-lookup"><span data-stu-id="a0726-117">Transparency</span></span>  <br/> |
   
<span data-ttu-id="a0726-118">Чтобы получить ссылку на ячейку "прозрачность" по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="a0726-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0726-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a0726-119">Section index:</span></span>  <br/> |<span data-ttu-id="a0726-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a0726-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a0726-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a0726-121">Row index:</span></span>  <br/> |<span data-ttu-id="a0726-122">**висровимаже**</span><span class="sxs-lookup"><span data-stu-id="a0726-122">**visRowImage**</span></span> <br/> |
|<span data-ttu-id="a0726-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a0726-123">Cell index:</span></span>  <br/> |<span data-ttu-id="a0726-124">**висимажетранспаренци**</span><span class="sxs-lookup"><span data-stu-id="a0726-124">**visImageTransparency**</span></span> <br/> |
   

