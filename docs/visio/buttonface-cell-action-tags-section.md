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
ms.openlocfilehash: ca6be0a95b33e173219f4bdc1ba042c7162941b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813315"
---
# <a name="buttonface-cell-action-tags-section"></a><span data-ttu-id="e932b-103">Ячейка ButtonFace (раздел "Теги действий")</span><span class="sxs-lookup"><span data-stu-id="e932b-103">ButtonFace Cell (Action Tags Section)</span></span>

<span data-ttu-id="e932b-104">Содержит идентификатор изображения кнопки, которое отображается на кнопке тега действия.</span><span class="sxs-lookup"><span data-stu-id="e932b-104">Contains the ID of the button face image that appears on the action tag button.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e932b-105">В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="e932b-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e932b-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="e932b-106">Remarks</span></span>

<span data-ttu-id="e932b-107">Строка, содержащихся в ячейке ButtonFace представляет идентификатор изображения кнопки Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="e932b-107">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image.</span></span> <span data-ttu-id="e932b-108">Значение нуль (0) или пустые значения по умолчанию для кнопки стандартного действия тег «я» сведения о ![](media/InfoPS_ZA10180114.gif).</span><span class="sxs-lookup"><span data-stu-id="e932b-108">A value of 0 (zero) or blank defaults to the standard action tag "i" info button ![](media/InfoPS_ZA10180114.gif).</span></span>
  
<span data-ttu-id="e932b-109">Идентификаторы, которые могут использоваться в ячейке ButtonFace такие же, как идентификаторы, используется совместно со свойством **FaceID** **CommandBarButton** объекта.</span><span class="sxs-lookup"><span data-stu-id="e932b-109">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="e932b-110">Для получения дополнительных сведений об этих кодов поиск «работа с изображениями кнопки панели команд» на сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="e932b-110">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="e932b-111">Для получения ссылки на ячейки ButtonFace по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e932b-111">To get a reference to the ButtonFace cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e932b-112">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="e932b-112">Cell name:</span></span>  <br/> | <span data-ttu-id="e932b-113">Смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="e932b-113">SmartTags.</span></span>  <span data-ttu-id="e932b-114">*имя* . ButtonFace где смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="e932b-114">*name*  .ButtonFace           where SmartTags.</span></span> <span data-ttu-id="e932b-115">*имя* — это имя строки тега действия</span><span class="sxs-lookup"><span data-stu-id="e932b-115">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="e932b-116">Для получения ссылки на ячейки ButtonFace по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="e932b-116">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e932b-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e932b-117">Section index:</span></span>  <br/> |<span data-ttu-id="e932b-118">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="e932b-118">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="e932b-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e932b-119">Row index:</span></span>  <br/> |<span data-ttu-id="e932b-120">**visRowSmartTag** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e932b-120">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e932b-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e932b-121">Cell index:</span></span>  <br/> |<span data-ttu-id="e932b-122">**visSmartTagButtonFace**</span><span class="sxs-lookup"><span data-stu-id="e932b-122">**visSmartTagButtonFace**</span></span> <br/> |
   

