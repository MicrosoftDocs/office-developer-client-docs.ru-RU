---
title: ViewMarkup Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
localization_priority: Normal
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: Определяет, отображается ли разметка в окне рисования.
ms.openlocfilehash: eeccdd0d14bf28630937b0e480822abb6fb19da5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416407"
---
# <a name="viewmarkup-cell-document-properties-section"></a><span data-ttu-id="b6871-103">ViewMarkup Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="b6871-103">ViewMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="b6871-104">Определяет, отображается ли разметка в окне рисования.</span><span class="sxs-lookup"><span data-stu-id="b6871-104">Determines whether markup appears in the drawing window.</span></span> 
  
|<span data-ttu-id="b6871-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b6871-105">**Value**</span></span>|<span data-ttu-id="b6871-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b6871-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b6871-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b6871-107">TRUE</span></span>  <br/> |<span data-ttu-id="b6871-108">Разметка отображается на рисунке.</span><span class="sxs-lookup"><span data-stu-id="b6871-108">Markup is displayed on the drawing.</span></span>  <br/> |
|<span data-ttu-id="b6871-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b6871-109">FALSE</span></span>  <br/> |<span data-ttu-id="b6871-110">Разметка не отображается (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="b6871-110">Markup is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6871-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="b6871-111">Remarks</span></span>

 <span data-ttu-id="b6871-112">При включении отслеживания разметки (ячейка AddMarkup является TRUE), ячейка ViewMarkup автоматически устанавливается в TRUE и остается TRUE даже после отключения отслеживания разметки (ячейка AddMarkup является FALSE).</span><span class="sxs-lookup"><span data-stu-id="b6871-112">When markup tracking is turned on (AddMarkup cell is TRUE), the ViewMarkup cell is automatically set to TRUE and remains TRUE even after markup tracking has been turned off (AddMarkup cell is FALSE).</span></span> <span data-ttu-id="b6871-113">Значение в ячейке ViewMarkup игнорируется, когда ячейка AddMarkup является TRUE.</span><span class="sxs-lookup"><span data-stu-id="b6871-113">The value in the ViewMarkup cell is ignored when the AddMarkup cell is TRUE.</span></span> 
  
<span data-ttu-id="b6871-114">Ячейка ViewMarkup также настроена как TRUE, когда комментарии вставляются в рисунок (включено ли отслеживание разметки) и должна быть TRUE, чтобы просмотреть комментарии на рисунке.</span><span class="sxs-lookup"><span data-stu-id="b6871-114">The ViewMarkup cell is also set to TRUE when comments are inserted in a drawing (whether or not markup tracking is turned on) and must be TRUE to see comments in the drawing.</span></span>
  
<span data-ttu-id="b6871-115">Эта ячейка соответствует команде **разметки Show** в группе **разметки** на вкладке **Обзор.**</span><span class="sxs-lookup"><span data-stu-id="b6871-115">This cell corresponds to the **Show Markup** command in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="b6871-116">Чтобы получить ссылку на ячейку ViewMarkup по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="b6871-116">To get a reference to the ViewMarkup cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6871-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b6871-117">Cell name:</span></span>  <br/> |<span data-ttu-id="b6871-118">ViewMarkup</span><span class="sxs-lookup"><span data-stu-id="b6871-118">ViewMarkup</span></span>  <br/> |
   
<span data-ttu-id="b6871-119">Чтобы получить ссылку на ячейку ViewMarkup по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b6871-119">To get a reference to the ViewMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6871-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b6871-120">Section index:</span></span>  <br/> |<span data-ttu-id="b6871-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b6871-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b6871-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b6871-122">Row index:</span></span>  <br/> |<span data-ttu-id="b6871-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="b6871-123">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="b6871-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b6871-124">Cell index:</span></span>  <br/> |<span data-ttu-id="b6871-125">**visDocViewMarkup**</span><span class="sxs-lookup"><span data-stu-id="b6871-125">**visDocViewMarkup**</span></span> <br/> |
   

