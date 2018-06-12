---
title: Ячейка LocalizeMerge (раздел Разное)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033773
localization_priority: Normal
ms.assetid: 734d4415-05dd-4c4d-763e-e035fa56dcec
description: Определяет локализованных фигуры при копировании в документы.
ms.openlocfilehash: 47593802e412c1871685f7218dd2a810bc2bc469
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814107"
---
# <a name="localizemerge-cell-miscellaneous-section"></a><span data-ttu-id="99c94-103">Ячейка LocalizeMerge (раздел Разное)</span><span class="sxs-lookup"><span data-stu-id="99c94-103">LocalizeMerge Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="99c94-104">Определяет локализованных фигуры при копировании в документы.</span><span class="sxs-lookup"><span data-stu-id="99c94-104">Determines whether shapes are localized when copied between documents.</span></span>
  
|<span data-ttu-id="99c94-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="99c94-105">**Value**</span></span>|<span data-ttu-id="99c94-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="99c94-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="99c94-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="99c94-107">TRUE</span></span>  <br/> | <span data-ttu-id="99c94-108">Локализация фигуры на языке конечного документа.</span><span class="sxs-lookup"><span data-stu-id="99c94-108">Localize a shape in the language of the destination document.</span></span>  <br/> |
| <span data-ttu-id="99c94-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="99c94-109">FALSE</span></span>  <br/> | <span data-ttu-id="99c94-110">Не локализуйте фигуры на основе языка целевого документа (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="99c94-110">Do not localize a shape based on the language of the destination document (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99c94-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="99c94-111">Remarks</span></span>

<span data-ttu-id="99c94-112">Чтобы получить ссылку на ячейку LocalizeMerge по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="99c94-112">To get a reference to the LocalizeMerge cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="99c94-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="99c94-113">Cell name:</span></span>  <br/> | <span data-ttu-id="99c94-114">LocalizeMerge</span><span class="sxs-lookup"><span data-stu-id="99c94-114">LocalizeMerge</span></span>  <br/> |
   
<span data-ttu-id="99c94-115">Для получения ссылки на ячейки LocalizeMerge по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="99c94-115">To get a reference to the LocalizeMerge cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="99c94-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="99c94-116">Section index:</span></span>  <br/> |<span data-ttu-id="99c94-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="99c94-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="99c94-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="99c94-118">Row index:</span></span>  <br/> |<span data-ttu-id="99c94-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="99c94-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="99c94-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="99c94-120">Cell index:</span></span>  <br/> |<span data-ttu-id="99c94-121">**visObjLocalizeMerge**</span><span class="sxs-lookup"><span data-stu-id="99c94-121">**visObjLocalizeMerge**</span></span> <br/> |
   

