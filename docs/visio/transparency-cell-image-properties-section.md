---
title: Прозрачность ячейки (раздел Свойства изображения)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51095
localization_priority: Normal
ms.assetid: 5b265356-1602-4241-fbe1-4d5a55392a52
description: Определяет уровень прозрачности цвета слоя.
ms.openlocfilehash: 5537cbdcd49c66f3bc28a58051f6e2888a290cd3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815053"
---
# <a name="transparency-cell-image-properties-section"></a><span data-ttu-id="8b15e-103">Прозрачность ячейки (раздел Свойства изображения)</span><span class="sxs-lookup"><span data-stu-id="8b15e-103">Transparency Cell (Image Properties Section)</span></span>

<span data-ttu-id="8b15e-104">Определяет уровень прозрачности цвета слоя.</span><span class="sxs-lookup"><span data-stu-id="8b15e-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="8b15e-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8b15e-105">**Value**</span></span>|<span data-ttu-id="8b15e-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8b15e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8b15e-107">0 — 100</span><span class="sxs-lookup"><span data-stu-id="8b15e-107">0 - 100</span></span>  <br/> |<span data-ttu-id="8b15e-108">Представляет собой процентную долю прозрачность.</span><span class="sxs-lookup"><span data-stu-id="8b15e-108">Represents the percentage of transparency.</span></span> <span data-ttu-id="8b15e-109">Значение по умолчанию — 0% (полностью непрозрачный).</span><span class="sxs-lookup"><span data-stu-id="8b15e-109">The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b15e-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="8b15e-110">Remarks</span></span>

<span data-ttu-id="8b15e-111">Значения округляются до ближайшего большего половины процентов.</span><span class="sxs-lookup"><span data-stu-id="8b15e-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="8b15e-112">Значение 100% является полностью прозрачным.</span><span class="sxs-lookup"><span data-stu-id="8b15e-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="8b15e-113">Несмотря на то, что уровень полностью прозрачным цвета появится на странице документа как уровень не цвета, взаимодействия с других объектов на странице так же, как как если бы его прозрачность 0%.</span><span class="sxs-lookup"><span data-stu-id="8b15e-113">Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span> <span data-ttu-id="8b15e-114">Также можно задать это значение с помощью элемента управления ползунок в диалоговом окне **Свойства слоя** (на вкладке **Главная** в группе **Редактирование** щелкните **слои**и выберите пункт **Свойства Layer**).</span><span class="sxs-lookup"><span data-stu-id="8b15e-114">You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="8b15e-115">Для получения ссылки на ячейки прозрачность по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="8b15e-115">To get a reference to the Transparency cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b15e-116">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="8b15e-116">Cell name:</span></span>  <br/> |<span data-ttu-id="8b15e-117">Прозрачность</span><span class="sxs-lookup"><span data-stu-id="8b15e-117">Transparency</span></span>  <br/> |
   
<span data-ttu-id="8b15e-118">Для получения ссылки на ячейки прозрачность по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="8b15e-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b15e-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8b15e-119">Section index:</span></span>  <br/> |<span data-ttu-id="8b15e-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8b15e-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8b15e-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8b15e-121">Row index:</span></span>  <br/> |<span data-ttu-id="8b15e-122">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="8b15e-122">**visRowImage**</span></span> <br/> |
|<span data-ttu-id="8b15e-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8b15e-123">Cell index:</span></span>  <br/> |<span data-ttu-id="8b15e-124">**visImageTransparency**</span><span class="sxs-lookup"><span data-stu-id="8b15e-124">**visImageTransparency**</span></span> <br/> |
   

