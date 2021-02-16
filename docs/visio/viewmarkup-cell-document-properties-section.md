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
# <a name="viewmarkup-cell-document-properties-section"></a><span data-ttu-id="c4762-103">ViewMarkup Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="c4762-103">ViewMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="c4762-104">Определяет, отображается ли разметка в окне рисования.</span><span class="sxs-lookup"><span data-stu-id="c4762-104">Determines whether markup appears in the drawing window.</span></span> 
  
|<span data-ttu-id="c4762-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c4762-105">**Value**</span></span>|<span data-ttu-id="c4762-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c4762-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c4762-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c4762-107">TRUE</span></span>  <br/> |<span data-ttu-id="c4762-108">Разметка отображается на рисунке.</span><span class="sxs-lookup"><span data-stu-id="c4762-108">Markup is displayed on the drawing.</span></span>  <br/> |
|<span data-ttu-id="c4762-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c4762-109">FALSE</span></span>  <br/> |<span data-ttu-id="c4762-110">Разметка не отображается (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="c4762-110">Markup is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4762-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="c4762-111">Remarks</span></span>

 <span data-ttu-id="c4762-112">Если отслеживание разметки включено (ячейка AddMarkup имеет true), ячейка ViewMarkup автоматически получает true и остается TRUE даже после отключения отслеживания разметки (ячейка AddMarkup имеет вид FALSE).</span><span class="sxs-lookup"><span data-stu-id="c4762-112">When markup tracking is turned on (AddMarkup cell is TRUE), the ViewMarkup cell is automatically set to TRUE and remains TRUE even after markup tracking has been turned off (AddMarkup cell is FALSE).</span></span> <span data-ttu-id="c4762-113">Значение в ячейке ViewMarkup игнорируется, если ячейка AddMarkup имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="c4762-113">The value in the ViewMarkup cell is ignored when the AddMarkup cell is TRUE.</span></span> 
  
<span data-ttu-id="c4762-114">Ячейка ViewMarkup также имеет true, когда комментарии вставляются в рисунок (включено ли отслеживание разметки) и должна иметь true, чтобы увидеть комментарии в рисунке.</span><span class="sxs-lookup"><span data-stu-id="c4762-114">The ViewMarkup cell is also set to TRUE when comments are inserted in a drawing (whether or not markup tracking is turned on) and must be TRUE to see comments in the drawing.</span></span>
  
<span data-ttu-id="c4762-115">Эта ячейка соответствует команде **"Показать разметку"** в группе **разметки** на вкладке **"Обзор".**</span><span class="sxs-lookup"><span data-stu-id="c4762-115">This cell corresponds to the **Show Markup** command in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="c4762-116">Чтобы получить ссылку на ячейку ViewMarkup по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="c4762-116">To get a reference to the ViewMarkup cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4762-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c4762-117">Cell name:</span></span>  <br/> |<span data-ttu-id="c4762-118">ViewMarkup</span><span class="sxs-lookup"><span data-stu-id="c4762-118">ViewMarkup</span></span>  <br/> |
   
<span data-ttu-id="c4762-119">Чтобы получить ссылку на ячейку ViewMarkup по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c4762-119">To get a reference to the ViewMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4762-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c4762-120">Section index:</span></span>  <br/> |<span data-ttu-id="c4762-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c4762-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c4762-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c4762-122">Row index:</span></span>  <br/> |<span data-ttu-id="c4762-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="c4762-123">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="c4762-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c4762-124">Cell index:</span></span>  <br/> |<span data-ttu-id="c4762-125">**visDocViewMarkup**</span><span class="sxs-lookup"><span data-stu-id="c4762-125">**visDocViewMarkup**</span></span> <br/> |
   

