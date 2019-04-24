---
title: Invisible Cell (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033755
localization_priority: Normal
ms.assetid: e67dcd83-4a88-a0f8-5c6a-dae51424edbd
description: Указывает, отображается ли гиперссылка в контекстном меню для фигуры или страницы.
ms.openlocfilehash: b52da8244bf31e75bacbb6f24f73eba6ee8c6e5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348337"
---
# <a name="invisible-cell-hyperlinks-section"></a><span data-ttu-id="138a6-103">Invisible Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="138a6-103">Invisible Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="138a6-104">Указывает, отображается ли гиперссылка в контекстном меню для фигуры или страницы.</span><span class="sxs-lookup"><span data-stu-id="138a6-104">Indicates whether a hyperlink appears on the shortcut menu for a shape or page.</span></span> 
  
|<span data-ttu-id="138a6-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="138a6-105">**Value**</span></span>|<span data-ttu-id="138a6-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="138a6-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="138a6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="138a6-107">TRUE</span></span>  <br/> |<span data-ttu-id="138a6-108">Гиперссылка не отображается как пункт меню в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="138a6-108">The hyperlink does not appear as a menu item on the shortcut menu.</span></span>  <br/> |
|<span data-ttu-id="138a6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="138a6-109">FALSE</span></span>  <br/> |<span data-ttu-id="138a6-110">Гиперссылка отображается как пункт меню в контекстном меню (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="138a6-110">The hyperlink does appear as a menu item on the shortcut menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="138a6-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="138a6-111">Remarks</span></span>

<span data-ttu-id="138a6-112">Чтобы получить ссылку на неВидимую ячейку по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="138a6-112">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="138a6-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="138a6-113">Cell name:</span></span>  <br/> |<span data-ttu-id="138a6-114">Гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="138a6-114">Hyperlink.</span></span> <span data-ttu-id="138a6-115">*Name (имя* ). НеВидимое расположение *. Name* — имя строки</span><span class="sxs-lookup"><span data-stu-id="138a6-115">*name*  .Invisible where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="138a6-116">Чтобы получить ссылку на неВидимую ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="138a6-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="138a6-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="138a6-117">Section index:</span></span>  <br/> |<span data-ttu-id="138a6-118">**Виссектионхиперлинк**</span><span class="sxs-lookup"><span data-stu-id="138a6-118">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="138a6-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="138a6-119">Row index:</span></span>  <br/> |<span data-ttu-id="138a6-120">**visRow1stHyperlink** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="138a6-120">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="138a6-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="138a6-121">Cell index:</span></span>  <br/> |<span data-ttu-id="138a6-122">**Вишлинкинвисибле**</span><span class="sxs-lookup"><span data-stu-id="138a6-122">**visHLinkInvisible**</span></span> <br/> |
   

