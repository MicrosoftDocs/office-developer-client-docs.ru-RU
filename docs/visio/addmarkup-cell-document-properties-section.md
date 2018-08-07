---
title: Ячейка AddMarkup (раздел "Свойства документа")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030801
localization_priority: Normal
ms.assetid: 46146424-b4c9-2240-36c0-19bb35ec51d1
description: Указывает ли рецензирование документа для разметки.
ms.openlocfilehash: 69430122b0a7665d7daa4a6b28f3a51745b74473
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813153"
---
# <a name="addmarkup-cell-document-properties-section"></a><span data-ttu-id="aa24a-103">Ячейка AddMarkup (раздел "Свойства документа")</span><span class="sxs-lookup"><span data-stu-id="aa24a-103">AddMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="aa24a-104">Указывает ли рецензирование документа для разметки.</span><span class="sxs-lookup"><span data-stu-id="aa24a-104">Indicates whether the document is being reviewed for markup.</span></span>
  
|<span data-ttu-id="aa24a-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="aa24a-105">**Value**</span></span>|<span data-ttu-id="aa24a-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="aa24a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aa24a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="aa24a-107">TRUE</span></span>  <br/> |<span data-ttu-id="aa24a-108">Время просмотра документа.</span><span class="sxs-lookup"><span data-stu-id="aa24a-108">Document is being reviewed.</span></span>  <br/> |
|<span data-ttu-id="aa24a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="aa24a-109">FALSE</span></span>  <br/> |<span data-ttu-id="aa24a-110">Документ не находится на рассмотрении (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="aa24a-110">Document is not being reviewed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa24a-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="aa24a-111">Remarks</span></span>

<span data-ttu-id="aa24a-112">При AddMarkup, ячейки имеет значение TRUE, проверяющий является добавление разметки и изменения применяются к перекрытия страницы разметки, не следует страниц исходного документа.</span><span class="sxs-lookup"><span data-stu-id="aa24a-112">When the AddMarkup cell is set to TRUE, the reviewer is adding markup and changes are applied to markup overlay pages, not to original drawing pages.</span></span> <span data-ttu-id="aa24a-113">Когда ячейки AddMarkup имеет значение FALSE, отслеживание исправлений отключено и изменения применяются к страниц исходного документа.</span><span class="sxs-lookup"><span data-stu-id="aa24a-113">When the AddMarkup cell is FALSE, markup tracking is off and changes are applied to the original drawing pages.</span></span>
  
> [!NOTE]
> <span data-ttu-id="aa24a-114">Можно запретить разметки с документами с помощью функции защиты.</span><span class="sxs-lookup"><span data-stu-id="aa24a-114">You can prevent markup on your documents by using the GUARD function.</span></span> <span data-ttu-id="aa24a-115">Если ячейка AddMarkup содержит формулу = GUARD(FALSE), команда **Отслеживать разметку** отключена.</span><span class="sxs-lookup"><span data-stu-id="aa24a-115">If the AddMarkup cell contains the formula =GUARD(FALSE), the **Track Markup** command is disabled.</span></span> 
  
<span data-ttu-id="aa24a-116">Этот параметр соответствует параметру команду **Отслеживать разметку** **разметки** группы на вкладке **Review** .</span><span class="sxs-lookup"><span data-stu-id="aa24a-116">This setting corresponds to the **Track Markup** command setting in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="aa24a-117">Чтобы получить ссылку на ячейку AddMarkup по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="aa24a-117">To get a reference to the AddMarkup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aa24a-118">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="aa24a-118">Cell name:</span></span>  <br/> |<span data-ttu-id="aa24a-119">AddMarkup</span><span class="sxs-lookup"><span data-stu-id="aa24a-119">AddMarkup</span></span>  <br/> |
   
<span data-ttu-id="aa24a-120">Для получения ссылки на ячейки AddMarkup по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="aa24a-120">To get a reference to the AddMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aa24a-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="aa24a-121">Section index:</span></span>  <br/> |<span data-ttu-id="aa24a-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="aa24a-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="aa24a-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="aa24a-123">Row index:</span></span>  <br/> |<span data-ttu-id="aa24a-124">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="aa24a-124">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="aa24a-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="aa24a-125">Cell index:</span></span>  <br/> |<span data-ttu-id="aa24a-126">**visDocAddMarkup**</span><span class="sxs-lookup"><span data-stu-id="aa24a-126">**visDocAddMarkup**</span></span> <br/> |
   

