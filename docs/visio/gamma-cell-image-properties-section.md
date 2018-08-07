---
title: Ячейка Gamma (раздел "Свойства изображения")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm410
localization_priority: Normal
ms.assetid: 3dcaee26-391c-0494-4380-890ee825dc47
description: Настраивает или корректирует насыщенность изображения для определенного выходное устройство, например монитор или средства поиска вирусов. Значение по умолчанию — 1 (корректировка отсутствует).
ms.openlocfilehash: 060cb02aa8fd33e5a6c70a2c0236f16b9552aea0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813833"
---
# <a name="gamma-cell-image-properties-section"></a><span data-ttu-id="811a0-104">Ячейка Gamma (раздел "Свойства изображения")</span><span class="sxs-lookup"><span data-stu-id="811a0-104">Gamma Cell (Image Properties Section)</span></span>

<span data-ttu-id="811a0-105">Настраивает или корректирует насыщенность изображения для определенного выходное устройство, например монитор или средства поиска вирусов.</span><span class="sxs-lookup"><span data-stu-id="811a0-105">Adjusts or corrects the intensity of an image for a particular output device, such as a monitor or scanner.</span></span> <span data-ttu-id="811a0-106">Значение по умолчанию — 1 (корректировка отсутствует).</span><span class="sxs-lookup"><span data-stu-id="811a0-106">The default value is 1 (no correction).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="811a0-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="811a0-107">Remarks</span></span>

<span data-ttu-id="811a0-108">Чтобы получить ссылку на ячейку гамма по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="811a0-108">To get a reference to the Gamma cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="811a0-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="811a0-109">Cell name:</span></span>  <br/> | <span data-ttu-id="811a0-110">Гамма</span><span class="sxs-lookup"><span data-stu-id="811a0-110">Gamma</span></span>  <br/> |
   
<span data-ttu-id="811a0-111">Для получения ссылки на ячейки гамма по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="811a0-111">To get a reference to the Gamma cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="811a0-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="811a0-112">Section index:</span></span>  <br/> |<span data-ttu-id="811a0-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="811a0-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="811a0-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="811a0-114">Row index:</span></span>  <br/> |<span data-ttu-id="811a0-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="811a0-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="811a0-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="811a0-116">Cell index:</span></span>  <br/> |<span data-ttu-id="811a0-117">**visImageGamma**</span><span class="sxs-lookup"><span data-stu-id="811a0-117">**visImageGamma**</span></span> <br/> |
   

