---
title: Ячейка Disabled (раздел "Теги действий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60038
localization_priority: Normal
ms.assetid: bf0a80c9-0fdb-e2cf-3ab0-74cb6338fdce
description: Указывает, отображается ли тег действия в окне документа.
ms.openlocfilehash: 409327365f3daf78dba20b1874be5911a517df0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813603"
---
# <a name="disabled-cell-action-tags-section"></a><span data-ttu-id="8b2ed-103">Ячейка Disabled (раздел "Теги действий")</span><span class="sxs-lookup"><span data-stu-id="8b2ed-103">Disabled Cell (Action Tags Section)</span></span>

<span data-ttu-id="8b2ed-104">Указывает, отображается ли тег действия в окне документа.</span><span class="sxs-lookup"><span data-stu-id="8b2ed-104">Indicates whether the action tag appears in the drawing window.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8b2ed-105">В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="8b2ed-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="8b2ed-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8b2ed-106">**Value**</span></span>|<span data-ttu-id="8b2ed-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8b2ed-107">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8b2ed-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="8b2ed-108">TRUE</span></span>  <br/> | <span data-ttu-id="8b2ed-109">Тег действия отключено.</span><span class="sxs-lookup"><span data-stu-id="8b2ed-109">The action tag is disabled.</span></span>  <br/> |
| <span data-ttu-id="8b2ed-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="8b2ed-110">FALSE</span></span>  <br/> | <span data-ttu-id="8b2ed-111">Тег действия включена (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="8b2ed-111">The action tag is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b2ed-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="8b2ed-112">Remarks</span></span>

<span data-ttu-id="8b2ed-113">При отключении тег действие он отображался на всех до он перезапускается.</span><span class="sxs-lookup"><span data-stu-id="8b2ed-113">When an action tag is disabled, it does not appear at all until it is re-enabled.</span></span> 
  
<span data-ttu-id="8b2ed-114">Чтобы получить ссылку на ячейку отключено по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="8b2ed-114">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8b2ed-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="8b2ed-115">Cell name:</span></span>  <br/> | <span data-ttu-id="8b2ed-116">Смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="8b2ed-116">SmartTags.</span></span>  <span data-ttu-id="8b2ed-117">*имя* . Этот параметр отключен где смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="8b2ed-117">*name*  .Disabled           where SmartTags.</span></span> <span data-ttu-id="8b2ed-118">*имя* — это имя строки тега действия</span><span class="sxs-lookup"><span data-stu-id="8b2ed-118">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="8b2ed-119">Для получения ссылки на ячейки отключено по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="8b2ed-119">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8b2ed-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8b2ed-120">Section index:</span></span>  <br/> |<span data-ttu-id="8b2ed-121">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="8b2ed-121">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="8b2ed-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8b2ed-122">Row index:</span></span>  <br/> |<span data-ttu-id="8b2ed-123">**visRowSmartTag** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8b2ed-123">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8b2ed-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8b2ed-124">Cell index:</span></span>  <br/> |<span data-ttu-id="8b2ed-125">**visSmartTagDisabled**</span><span class="sxs-lookup"><span data-stu-id="8b2ed-125">**visSmartTagDisabled**</span></span> <br/> |
   

