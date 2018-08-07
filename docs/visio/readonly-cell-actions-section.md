---
title: Ячейка ReadOnly (раздел "Действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60071
localization_priority: Normal
ms.assetid: 158b4188-570c-3817-bf34-8dc0c64befa5
description: Определяет, является ли действие на тег или контекстное меню действий только для чтения.
ms.openlocfilehash: bf2d0f7e50a3126611662af8e068485986c26a13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814522"
---
# <a name="readonly-cell-actions-section"></a><span data-ttu-id="5591a-103">Ячейка ReadOnly (раздел "Действия")</span><span class="sxs-lookup"><span data-stu-id="5591a-103">ReadOnly Cell (Actions Section)</span></span>

<span data-ttu-id="5591a-104">Определяет, является ли действие на тег или контекстное меню действий только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5591a-104">Controls whether the action on an action tag or shortcut menu is read-only.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5591a-105">В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="5591a-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="5591a-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5591a-106">**Value**</span></span>|<span data-ttu-id="5591a-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5591a-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5591a-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="5591a-108">TRUE</span></span>  <br/> |<span data-ttu-id="5591a-109">Действие отображается в меню, но только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5591a-109">The action appears on the menu but is read-only.</span></span>  <br/> |
|<span data-ttu-id="5591a-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="5591a-110">FALSE</span></span>  <br/> |<span data-ttu-id="5591a-111">Действие отображается в меню и может быть установлен (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="5591a-111">The action appears on the menu and can be selected (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5591a-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="5591a-112">Remarks</span></span>

<span data-ttu-id="5591a-113">При действие, которое доступно только для чтения, отображается в действие тег или контекстное меню, но не могут установить его.</span><span class="sxs-lookup"><span data-stu-id="5591a-113">When an action is read-only, it appears on the action tag or shortcut menu but you cannot select it.</span></span> <span data-ttu-id="5591a-114">Он не недоступна, но вместо отображается на цветном фоне, как метки.</span><span class="sxs-lookup"><span data-stu-id="5591a-114">It is not dimmed but rather appears on a colored background, like a label.</span></span> <span data-ttu-id="5591a-115">Чтобы сделать элемент меню недоступны для изменения, используйте ячейку отключено.</span><span class="sxs-lookup"><span data-stu-id="5591a-115">To make the menu item appear dimmed, use the Disabled cell.</span></span> 
  
<span data-ttu-id="5591a-116">Чтобы получить ссылку на ячейку только для чтения по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="5591a-116">To get a reference to the ReadOnly cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5591a-117">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="5591a-117">Cell name:</span></span>  <br/> |<span data-ttu-id="5591a-118">Действия.</span><span class="sxs-lookup"><span data-stu-id="5591a-118">Actions.</span></span> <span data-ttu-id="5591a-119">*имя* . ReadOnlywhere действия.</span><span class="sxs-lookup"><span data-stu-id="5591a-119">*name*  .ReadOnlywhere Actions.</span></span>  <span data-ttu-id="5591a-120">*имя* — это имя строки действий</span><span class="sxs-lookup"><span data-stu-id="5591a-120">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="5591a-121">Для получения ссылки на ячейки только для чтения по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="5591a-121">To get a reference to the ReadOnly cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5591a-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5591a-122">Section index:</span></span>  <br/> |<span data-ttu-id="5591a-123">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="5591a-123">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="5591a-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5591a-124">Row index:</span></span>  <br/> |<span data-ttu-id="5591a-125">**visRowAction** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5591a-125">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="5591a-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5591a-126">Cell index:</span></span>  <br/> |<span data-ttu-id="5591a-127">**visActionReadOnly**</span><span class="sxs-lookup"><span data-stu-id="5591a-127">**visActionReadOnly**</span></span> <br/> |
   

