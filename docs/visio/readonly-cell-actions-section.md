---
title: ReadOnly Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60071
localization_priority: Normal
ms.assetid: 158b4188-570c-3817-bf34-8dc0c64befa5
description: Контролирует, является ли действие в теге действия или меню ярлыка только для чтения.
ms.openlocfilehash: f45f22001a4d7275bb9367414c8b04ea3c0d9c6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434237"
---
# <a name="readonly-cell-actions-section"></a><span data-ttu-id="be837-103">ReadOnly Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="be837-103">ReadOnly Cell (Actions Section)</span></span>

<span data-ttu-id="be837-104">Контролирует, является ли действие в теге действия или меню ярлыка только для чтения.</span><span class="sxs-lookup"><span data-stu-id="be837-104">Controls whether the action on an action tag or shortcut menu is read-only.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="be837-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="be837-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="be837-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="be837-106">**Value**</span></span>|<span data-ttu-id="be837-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="be837-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="be837-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="be837-108">TRUE</span></span>  <br/> |<span data-ttu-id="be837-109">Действие отображается в меню, но только для чтения.</span><span class="sxs-lookup"><span data-stu-id="be837-109">The action appears on the menu but is read-only.</span></span>  <br/> |
|<span data-ttu-id="be837-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="be837-110">FALSE</span></span>  <br/> |<span data-ttu-id="be837-111">Действие отображается в меню и может быть выбрано (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="be837-111">The action appears on the menu and can be selected (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be837-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="be837-112">Remarks</span></span>

<span data-ttu-id="be837-113">Если действие только для чтения, оно отображается в теге действия или в меню ярлыка, но выбрать его невозможно.</span><span class="sxs-lookup"><span data-stu-id="be837-113">When an action is read-only, it appears on the action tag or shortcut menu but you cannot select it.</span></span> <span data-ttu-id="be837-114">Он не приглушенный, а отображается на цветном фоне, как метка.</span><span class="sxs-lookup"><span data-stu-id="be837-114">It is not dimmed but rather appears on a colored background, like a label.</span></span> <span data-ttu-id="be837-115">Чтобы элемент меню казался неохваченным, используйте ячейку Отключена.</span><span class="sxs-lookup"><span data-stu-id="be837-115">To make the menu item appear dimmed, use the Disabled cell.</span></span> 
  
<span data-ttu-id="be837-116">Чтобы получить ссылку на ячейку ReadOnly по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="be837-116">To get a reference to the ReadOnly cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be837-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="be837-117">Cell name:</span></span>  <br/> |<span data-ttu-id="be837-118">Действия.</span><span class="sxs-lookup"><span data-stu-id="be837-118">Actions.</span></span> <span data-ttu-id="be837-119">*имя*  . Действия ReadOnlywhere.</span><span class="sxs-lookup"><span data-stu-id="be837-119">*name*  .ReadOnlywhere Actions.</span></span>  <span data-ttu-id="be837-120">*имя*  — это имя строки Действия</span><span class="sxs-lookup"><span data-stu-id="be837-120">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="be837-121">Чтобы получить ссылку на ячейку ReadOnly по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="be837-121">To get a reference to the ReadOnly cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be837-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="be837-122">Section index:</span></span>  <br/> |<span data-ttu-id="be837-123">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="be837-123">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="be837-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="be837-124">Row index:</span></span>  <br/> |<span data-ttu-id="be837-125">**visRowAction**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="be837-125">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="be837-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="be837-126">Cell index:</span></span>  <br/> |<span data-ttu-id="be837-127">**visActionReadOnly**</span><span class="sxs-lookup"><span data-stu-id="be837-127">**visActionReadOnly**</span></span> <br/> |
   

