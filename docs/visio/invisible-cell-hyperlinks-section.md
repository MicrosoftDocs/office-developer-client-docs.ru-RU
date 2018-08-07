---
title: Ячейка Invisible (раздел "Гиперссылки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033755
localization_priority: Normal
ms.assetid: e67dcd83-4a88-a0f8-5c6a-dae51424edbd
description: Указывает, отображается ли гиперссылка в контекстном меню для фигуры или страницы.
ms.openlocfilehash: e269c5e907afa0d49f1fc6115b7a031835467c2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813979"
---
# <a name="invisible-cell-hyperlinks-section"></a><span data-ttu-id="18565-103">Ячейка Invisible (раздел "Гиперссылки")</span><span class="sxs-lookup"><span data-stu-id="18565-103">Invisible Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="18565-104">Указывает, отображается ли гиперссылка в контекстном меню для фигуры или страницы.</span><span class="sxs-lookup"><span data-stu-id="18565-104">Indicates whether a hyperlink appears on the shortcut menu for a shape or page.</span></span> 
  
|<span data-ttu-id="18565-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="18565-105">**Value**</span></span>|<span data-ttu-id="18565-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="18565-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18565-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="18565-107">TRUE</span></span>  <br/> |<span data-ttu-id="18565-108">Гиперссылка не отображается в виде элемента меню в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="18565-108">The hyperlink does not appear as a menu item on the shortcut menu.</span></span>  <br/> |
|<span data-ttu-id="18565-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="18565-109">FALSE</span></span>  <br/> |<span data-ttu-id="18565-110">Гиперссылки отображаются в виде элемента меню в контекстном меню (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="18565-110">The hyperlink does appear as a menu item on the shortcut menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18565-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="18565-111">Remarks</span></span>

<span data-ttu-id="18565-112">Для получения ссылки на ячейки невидимой по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="18565-112">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18565-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="18565-113">Cell name:</span></span>  <br/> |<span data-ttu-id="18565-114">Гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="18565-114">Hyperlink.</span></span> <span data-ttu-id="18565-115">*имя* . Невидимое, где гиперссылки *.name* — это имя строки</span><span class="sxs-lookup"><span data-stu-id="18565-115">*name*  .Invisible where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="18565-116">Для получения ссылки на ячейки невидимой по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="18565-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18565-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="18565-117">Section index:</span></span>  <br/> |<span data-ttu-id="18565-118">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="18565-118">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="18565-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="18565-119">Row index:</span></span>  <br/> |<span data-ttu-id="18565-120">**visRow1stHyperlink** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="18565-120">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="18565-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="18565-121">Cell index:</span></span>  <br/> |<span data-ttu-id="18565-122">**visHLinkInvisible**</span><span class="sxs-lookup"><span data-stu-id="18565-122">**visHLinkInvisible**</span></span> <br/> |
   

