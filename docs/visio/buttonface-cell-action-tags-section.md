---
title: Ячейка ButtonFace (раздел "Теги действий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60026
localization_priority: Normal
ms.assetid: 26f370e1-5193-f47d-7b60-3597975be650
description: Содержит идентификатор изображения кнопки, которое отображается на кнопке тега действия.
ms.openlocfilehash: e74b3281d894cebd8491112181198d427f0d337f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385482"
---
# <a name="buttonface-cell-action-tags-section"></a><span data-ttu-id="b79ea-103">Ячейка ButtonFace (раздел "Теги действий")</span><span class="sxs-lookup"><span data-stu-id="b79ea-103">ButtonFace Cell (Action Tags Section)</span></span>

<span data-ttu-id="b79ea-104">Содержит идентификатор изображения кнопки, которое отображается на кнопке тега действия.</span><span class="sxs-lookup"><span data-stu-id="b79ea-104">Contains the ID of the button face image that appears on the action tag button.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b79ea-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="b79ea-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b79ea-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="b79ea-106">Remarks</span></span>

<span data-ttu-id="b79ea-107">Строка, содержащихся в ячейке ButtonFace представляет идентификатор изображения кнопки Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="b79ea-107">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image.</span></span> <span data-ttu-id="b79ea-108">Значение нуль (0) или пустые значения по умолчанию для кнопки стандартного действия тег «я» info</span><span class="sxs-lookup"><span data-stu-id="b79ea-108">A value of 0 (zero) or blank defaults to the standard action tag "i" info button</span></span> ![Кнопки info тега «я» Standard действия](media/InfoPS_ZA10180114.gif)<span data-ttu-id="b79ea-110">.</span><span class="sxs-lookup"><span data-stu-id="b79ea-110"></span></span>
  
<span data-ttu-id="b79ea-111">Идентификаторы, которые могут использоваться в ячейке ButtonFace такие же, как идентификаторы, используется совместно со свойством **FaceID** **CommandBarButton** объекта.</span><span class="sxs-lookup"><span data-stu-id="b79ea-111">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="b79ea-112">Для получения дополнительных сведений об этих кодов поиск «работа с изображениями кнопки панели команд» на сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="b79ea-112">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="b79ea-113">Для получения ссылки на ячейки ButtonFace по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="b79ea-113">To get a reference to the ButtonFace cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b79ea-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b79ea-114">Cell name:</span></span>  <br/> | <span data-ttu-id="b79ea-115">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="b79ea-115">SmartTags.</span></span>  <span data-ttu-id="b79ea-116">*имя* . ButtonFace где смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="b79ea-116">*name*  .ButtonFace           where SmartTags.</span></span> <span data-ttu-id="b79ea-117">*имя* — название строки тегов действий.</span><span class="sxs-lookup"><span data-stu-id="b79ea-117">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="b79ea-118">Для получения ссылки на ячейки ButtonFace по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="b79ea-118">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b79ea-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b79ea-119">Section index:</span></span>  <br/> |<span data-ttu-id="b79ea-120">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="b79ea-120">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="b79ea-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b79ea-121">Row index:</span></span>  <br/> |<span data-ttu-id="b79ea-122">**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="b79ea-122">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b79ea-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b79ea-123">Cell index:</span></span>  <br/> |<span data-ttu-id="b79ea-124">**visSmartTagButtonFace**</span><span class="sxs-lookup"><span data-stu-id="b79ea-124">**visSmartTagButtonFace**</span></span> <br/> |
   

