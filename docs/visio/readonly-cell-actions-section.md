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
description: Определяет, является ли действие для тега действия или контекстного меню предназначенным только для чтения.
ms.openlocfilehash: f45f22001a4d7275bb9367414c8b04ea3c0d9c6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434237"
---
# <a name="readonly-cell-actions-section"></a><span data-ttu-id="5548d-103">ReadOnly Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="5548d-103">ReadOnly Cell (Actions Section)</span></span>

<span data-ttu-id="5548d-104">Определяет, является ли действие для тега действия или контекстного меню предназначенным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5548d-104">Controls whether the action on an action tag or shortcut menu is read-only.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5548d-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="5548d-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="5548d-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5548d-106">**Value**</span></span>|<span data-ttu-id="5548d-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5548d-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5548d-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="5548d-108">TRUE</span></span>  <br/> |<span data-ttu-id="5548d-109">Действие отображается в меню, но доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5548d-109">The action appears on the menu but is read-only.</span></span>  <br/> |
|<span data-ttu-id="5548d-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="5548d-110">FALSE</span></span>  <br/> |<span data-ttu-id="5548d-111">Действие отображается в меню и может быть выбрано (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="5548d-111">The action appears on the menu and can be selected (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5548d-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="5548d-112">Remarks</span></span>

<span data-ttu-id="5548d-113">Если действие доступно только для чтения, оно отображается в теге действия или в контекстном меню, но его нельзя выбрать.</span><span class="sxs-lookup"><span data-stu-id="5548d-113">When an action is read-only, it appears on the action tag or shortcut menu but you cannot select it.</span></span> <span data-ttu-id="5548d-114">Он не затенен, а отображается на цветном фоне, например в метке.</span><span class="sxs-lookup"><span data-stu-id="5548d-114">It is not dimmed but rather appears on a colored background, like a label.</span></span> <span data-ttu-id="5548d-115">Чтобы элемент меню отображался серым цветом, используйте отключенную ячейку.</span><span class="sxs-lookup"><span data-stu-id="5548d-115">To make the menu item appear dimmed, use the Disabled cell.</span></span> 
  
<span data-ttu-id="5548d-116">Чтобы получить ссылку на ячейку ReadOnly по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="5548d-116">To get a reference to the ReadOnly cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5548d-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="5548d-117">Cell name:</span></span>  <br/> |<span data-ttu-id="5548d-118">Действия.</span><span class="sxs-lookup"><span data-stu-id="5548d-118">Actions.</span></span> <span data-ttu-id="5548d-119">*Name (имя* ). Действия Реадонливхере.</span><span class="sxs-lookup"><span data-stu-id="5548d-119">*name*  .ReadOnlywhere Actions.</span></span>  <span data-ttu-id="5548d-120">*Name* — имя строки действий</span><span class="sxs-lookup"><span data-stu-id="5548d-120">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="5548d-121">Чтобы получить ссылку на ячейку ReadOnly по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="5548d-121">To get a reference to the ReadOnly cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5548d-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5548d-122">Section index:</span></span>  <br/> |<span data-ttu-id="5548d-123">**виссектионактион**</span><span class="sxs-lookup"><span data-stu-id="5548d-123">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="5548d-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5548d-124">Row index:</span></span>  <br/> |<span data-ttu-id="5548d-125">**висровактион** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5548d-125">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="5548d-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5548d-126">Cell index:</span></span>  <br/> |<span data-ttu-id="5548d-127">**висактионреадонли**</span><span class="sxs-lookup"><span data-stu-id="5548d-127">**visActionReadOnly**</span></span> <br/> |
   

