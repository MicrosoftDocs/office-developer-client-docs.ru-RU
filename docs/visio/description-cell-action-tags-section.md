---
title: Ячейка Description (раздел "Теги действий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
localization_priority: Normal
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: Содержит строку, описывающую тег действия, которая отображается в виде подсказки при пользователей поместить их указатель мыши на тег.
ms.openlocfilehash: 3c365d24170f912624a2abdeeadd75140bea9a85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813600"
---
# <a name="description-cell-action-tags-section"></a><span data-ttu-id="aec4b-103">Ячейка Description (раздел "Теги действий")</span><span class="sxs-lookup"><span data-stu-id="aec4b-103">Description Cell (Action Tags Section)</span></span>

<span data-ttu-id="aec4b-104">Содержит строку, описывающую тег действия, которая отображается в виде подсказки при пользователей поместить их указатель мыши на тег.</span><span class="sxs-lookup"><span data-stu-id="aec4b-104">Contains a string that describes the action tag, which appears as a tool tip when users place their pointer over the tag.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aec4b-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="aec4b-105">Remarks</span></span>

<span data-ttu-id="aec4b-106">Для получения ссылки на ячейки описание по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="aec4b-106">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aec4b-107">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="aec4b-107">Cell name:</span></span>  <br/> | <span data-ttu-id="aec4b-108">Смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="aec4b-108">SmartTags.</span></span>  <span data-ttu-id="aec4b-109">*имя* . Описание где смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="aec4b-109">*name*  .Description           where SmartTags.</span></span> <span data-ttu-id="aec4b-110">*имя* — это имя строки тега действия</span><span class="sxs-lookup"><span data-stu-id="aec4b-110">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="aec4b-111">Для получения ссылки на ячейки описание по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="aec4b-111">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aec4b-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="aec4b-112">Section index:</span></span>  <br/> |<span data-ttu-id="aec4b-113">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="aec4b-113">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="aec4b-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="aec4b-114">Row index:</span></span>  <br/> |<span data-ttu-id="aec4b-115">**visRowSmartTag** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="aec4b-115">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="aec4b-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="aec4b-116">Cell index:</span></span>  <br/> |<span data-ttu-id="aec4b-117">**visSmartTagDescription**</span><span class="sxs-lookup"><span data-stu-id="aec4b-117">**visSmartTagDescription**</span></span> <br/> |
   

