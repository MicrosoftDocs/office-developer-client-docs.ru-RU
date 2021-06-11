---
title: Invisible Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60046
localization_priority: Normal
ms.assetid: 070b4468-c907-b201-1633-1d3e10ecc2b2
description: Указывает, отображается ли действие в теге действия или в меню ярлыка.
ms.openlocfilehash: 69bc96e76f27a64d6e1443f045c27566f598c1db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423876"
---
# <a name="invisible-cell-actions-section"></a><span data-ttu-id="7ccfa-103">Invisible Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="7ccfa-103">Invisible Cell (Actions Section)</span></span>

<span data-ttu-id="7ccfa-104">Указывает, отображается ли действие в теге действия или в меню ярлыка.</span><span class="sxs-lookup"><span data-stu-id="7ccfa-104">Indicates whether the action is visible on the action tag or shortcut menu.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7ccfa-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="7ccfa-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="7ccfa-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="7ccfa-106">**Value**</span></span>|<span data-ttu-id="7ccfa-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7ccfa-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7ccfa-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="7ccfa-108">TRUE</span></span>  <br/> |<span data-ttu-id="7ccfa-109">Действие не отображается в меню.</span><span class="sxs-lookup"><span data-stu-id="7ccfa-109">The action is not visible on the menu.</span></span>  <br/> |
|<span data-ttu-id="7ccfa-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="7ccfa-110">FALSE</span></span>  <br/> |<span data-ttu-id="7ccfa-111">Действие отображается в меню (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="7ccfa-111">The action is visible on the menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ccfa-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="7ccfa-112">Remarks</span></span>

<span data-ttu-id="7ccfa-113">Чтобы получить ссылку на невидимую ячейку по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="7ccfa-113">To get a reference to the Invisible cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7ccfa-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="7ccfa-114">Cell name:</span></span>  <br/> |<span data-ttu-id="7ccfa-115">Действия.</span><span class="sxs-lookup"><span data-stu-id="7ccfa-115">Actions.</span></span> <span data-ttu-id="7ccfa-116">*имя*  . Действия invisiblewhere.</span><span class="sxs-lookup"><span data-stu-id="7ccfa-116">*name*  .Invisiblewhere Actions.</span></span>  <span data-ttu-id="7ccfa-117">*имя*  — это имя строки Действия</span><span class="sxs-lookup"><span data-stu-id="7ccfa-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="7ccfa-118">Чтобы получить ссылку на невидимую ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="7ccfa-118">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7ccfa-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="7ccfa-119">Section index:</span></span>  <br/> |<span data-ttu-id="7ccfa-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="7ccfa-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="7ccfa-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="7ccfa-121">Row index:</span></span>  <br/> |<span data-ttu-id="7ccfa-122">**visRowAction**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="7ccfa-122">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="7ccfa-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="7ccfa-123">Cell index:</span></span>  <br/> |<span data-ttu-id="7ccfa-124">**visActionInvisible**</span><span class="sxs-lookup"><span data-stu-id="7ccfa-124">**visActionInvisible**</span></span> <br/> |
   

