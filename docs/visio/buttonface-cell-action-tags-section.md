---
title: ButtonFace Cell (Action Tags Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60026
localization_priority: Normal
ms.assetid: 26f370e1-5193-f47d-7b60-3597975be650
description: Содержит ИД изображения лица кнопки, которое отображается на кнопке тега действия.
ms.openlocfilehash: e74b3281d894cebd8491112181198d427f0d337f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337542"
---
# <a name="buttonface-cell-action-tags-section"></a><span data-ttu-id="acdc0-103">ButtonFace Cell (Action Tags Section)</span><span class="sxs-lookup"><span data-stu-id="acdc0-103">ButtonFace Cell (Action Tags Section)</span></span>

<span data-ttu-id="acdc0-104">Содержит ИД изображения лица кнопки, которое отображается на кнопке тега действия.</span><span class="sxs-lookup"><span data-stu-id="acdc0-104">Contains the ID of the button face image that appears on the action tag button.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="acdc0-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="acdc0-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="acdc0-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="acdc0-106">Remarks</span></span>

<span data-ttu-id="acdc0-107">Строка, содержаная в ячейке ButtonFace, представляет ИД Microsoft Office кнопок.</span><span class="sxs-lookup"><span data-stu-id="acdc0-107">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image.</span></span> <span data-ttu-id="acdc0-108">Значение 0 (ноль) или пустое значение по умолчанию для стандартной кнопки информации тега действия "i"</span><span class="sxs-lookup"><span data-stu-id="acdc0-108">A value of 0 (zero) or blank defaults to the standard action tag "i" info button</span></span> ![Стандартная кнопка с тегом действия "i"](media/InfoPS_ZA10180114.gif)<span data-ttu-id="acdc0-110">.</span><span class="sxs-lookup"><span data-stu-id="acdc0-110">.</span></span>
  
<span data-ttu-id="acdc0-111">ИД, которые можно использовать в ячейке ButtonFace, такие же, как и для свойств **FaceID** объекта **CommandBarButton.**</span><span class="sxs-lookup"><span data-stu-id="acdc0-111">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="acdc0-112">Для получения дополнительных сведений об этих ИД на сайте MSDN найди поиск по запросу "Работа с изображениями кнопок панели команд".</span><span class="sxs-lookup"><span data-stu-id="acdc0-112">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="acdc0-113">Чтобы получить ссылку на ячейку ButtonFace по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="acdc0-113">To get a reference to the ButtonFace cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="acdc0-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="acdc0-114">Cell name:</span></span>  <br/> | <span data-ttu-id="acdc0-115">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="acdc0-115">SmartTags.</span></span>  <span data-ttu-id="acdc0-116">*name*  . ButtonFace, где SmartTags.</span><span class="sxs-lookup"><span data-stu-id="acdc0-116">*name*  .ButtonFace           where SmartTags.</span></span> <span data-ttu-id="acdc0-117">*имя* — название строки тегов действий.</span><span class="sxs-lookup"><span data-stu-id="acdc0-117">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="acdc0-118">Чтобы получить ссылку на ячейку ButtonFace по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="acdc0-118">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="acdc0-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="acdc0-119">Section index:</span></span>  <br/> |<span data-ttu-id="acdc0-120">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="acdc0-120">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="acdc0-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="acdc0-121">Row index:</span></span>  <br/> |<span data-ttu-id="acdc0-122">**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="acdc0-122">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="acdc0-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="acdc0-123">Cell index:</span></span>  <br/> |<span data-ttu-id="acdc0-124">**visSmartTagButtonFace**</span><span class="sxs-lookup"><span data-stu-id="acdc0-124">**visSmartTagButtonFace**</span></span> <br/> |
   

