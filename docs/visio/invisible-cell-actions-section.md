---
title: Ячейка Invisible (раздел "Действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60046
localization_priority: Normal
ms.assetid: 070b4468-c907-b201-1633-1d3e10ecc2b2
description: Указывает, видима ли действие в меню Действие тег или ярлык.
ms.openlocfilehash: 8749b7d6db4a932b97c68ab5cf30b879a57d28f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813970"
---
# <a name="invisible-cell-actions-section"></a><span data-ttu-id="92cf1-103">Ячейка Invisible (раздел "Действия")</span><span class="sxs-lookup"><span data-stu-id="92cf1-103">Invisible Cell (Actions Section)</span></span>

<span data-ttu-id="92cf1-104">Указывает, видима ли действие в меню Действие тег или ярлык.</span><span class="sxs-lookup"><span data-stu-id="92cf1-104">Indicates whether the action is visible on the action tag or shortcut menu.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="92cf1-105">В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="92cf1-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="92cf1-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="92cf1-106">**Value**</span></span>|<span data-ttu-id="92cf1-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="92cf1-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="92cf1-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="92cf1-108">TRUE</span></span>  <br/> |<span data-ttu-id="92cf1-109">Действие не отображается в меню.</span><span class="sxs-lookup"><span data-stu-id="92cf1-109">The action is not visible on the menu.</span></span>  <br/> |
|<span data-ttu-id="92cf1-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="92cf1-110">FALSE</span></span>  <br/> |<span data-ttu-id="92cf1-111">Действие отображается в меню (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="92cf1-111">The action is visible on the menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92cf1-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="92cf1-112">Remarks</span></span>

<span data-ttu-id="92cf1-113">Для получения ссылки на невидимой ячейку по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="92cf1-113">To get a reference to the Invisible cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92cf1-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="92cf1-114">Cell name:</span></span>  <br/> |<span data-ttu-id="92cf1-115">Действия.</span><span class="sxs-lookup"><span data-stu-id="92cf1-115">Actions.</span></span> <span data-ttu-id="92cf1-116">*имя* . Invisiblewhere действия.</span><span class="sxs-lookup"><span data-stu-id="92cf1-116">*name*  .Invisiblewhere Actions.</span></span>  <span data-ttu-id="92cf1-117">*имя* — это имя строки действий</span><span class="sxs-lookup"><span data-stu-id="92cf1-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="92cf1-118">Для получения ссылки на ячейки невидимой по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="92cf1-118">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92cf1-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="92cf1-119">Section index:</span></span>  <br/> |<span data-ttu-id="92cf1-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="92cf1-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="92cf1-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="92cf1-121">Row index:</span></span>  <br/> |<span data-ttu-id="92cf1-122">**visRowAction** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="92cf1-122">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="92cf1-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="92cf1-123">Cell index:</span></span>  <br/> |<span data-ttu-id="92cf1-124">**visActionInvisible**</span><span class="sxs-lookup"><span data-stu-id="92cf1-124">**visActionInvisible**</span></span> <br/> |
   

