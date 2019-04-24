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
description: Определяет, отображаются ли разметки в окне документа.
ms.openlocfilehash: eeccdd0d14bf28630937b0e480822abb6fb19da5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355827"
---
# <a name="viewmarkup-cell-document-properties-section"></a><span data-ttu-id="6fcd1-103">ViewMarkup Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="6fcd1-103">ViewMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="6fcd1-104">Определяет, отображаются ли разметки в окне документа.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-104">Determines whether markup appears in the drawing window.</span></span> 
  
|<span data-ttu-id="6fcd1-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="6fcd1-105">**Value**</span></span>|<span data-ttu-id="6fcd1-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6fcd1-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6fcd1-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="6fcd1-107">TRUE</span></span>  <br/> |<span data-ttu-id="6fcd1-108">В документе отображается разМетка.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-108">Markup is displayed on the drawing.</span></span>  <br/> |
|<span data-ttu-id="6fcd1-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="6fcd1-109">FALSE</span></span>  <br/> |<span data-ttu-id="6fcd1-110">РазМетка не отображается (значение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="6fcd1-110">Markup is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6fcd1-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="6fcd1-111">Remarks</span></span>

 <span data-ttu-id="6fcd1-112">Если включено отслеживание разметки (ячейка AddMarkup имеет значение TRUE), ячейка ViewMarkup автоматически задается как TRUE и остается ДЕЙСТВИТЕЛЬНОй даже после выключения отслеживания разметки (ячейка AddMarkup имеет значение FALSE).</span><span class="sxs-lookup"><span data-stu-id="6fcd1-112">When markup tracking is turned on (AddMarkup cell is TRUE), the ViewMarkup cell is automatically set to TRUE and remains TRUE even after markup tracking has been turned off (AddMarkup cell is FALSE).</span></span> <span data-ttu-id="6fcd1-113">Если ячейка AddMarkup имеет значение TRUE, значение в ячейке ViewMarkup игнорируется.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-113">The value in the ViewMarkup cell is ignored when the AddMarkup cell is TRUE.</span></span> 
  
<span data-ttu-id="6fcd1-114">Ячейка ViewMarkup также имеет значение TRUE при вставке комментариев в документ (независимо от того, включено ли отслеживание разметки) и должно иметь значение TRUE, чтобы увидеть комментарии в документе.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-114">The ViewMarkup cell is also set to TRUE when comments are inserted in a drawing (whether or not markup tracking is turned on) and must be TRUE to see comments in the drawing.</span></span>
  
<span data-ttu-id="6fcd1-115">Эта ячейка соответствует команде " **Показать разметку** " в группе разметки на вкладке " **Рецензирование** ". \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6fcd1-115">This cell corresponds to the **Show Markup** command in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="6fcd1-116">Чтобы получить ссылку на ячейку ViewMarkup по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="6fcd1-116">To get a reference to the ViewMarkup cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6fcd1-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="6fcd1-117">Cell name:</span></span>  <br/> |<span data-ttu-id="6fcd1-118">ViewMarkup</span><span class="sxs-lookup"><span data-stu-id="6fcd1-118">ViewMarkup</span></span>  <br/> |
   
<span data-ttu-id="6fcd1-119">Чтобы получить ссылку на ячейку ViewMarkup по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="6fcd1-119">To get a reference to the ViewMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6fcd1-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6fcd1-120">Section index:</span></span>  <br/> |<span data-ttu-id="6fcd1-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6fcd1-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6fcd1-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6fcd1-122">Row index:</span></span>  <br/> |<span data-ttu-id="6fcd1-123">**Висровдок**</span><span class="sxs-lookup"><span data-stu-id="6fcd1-123">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="6fcd1-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6fcd1-124">Cell index:</span></span>  <br/> |<span data-ttu-id="6fcd1-125">**Висдоквиевмаркуп**</span><span class="sxs-lookup"><span data-stu-id="6fcd1-125">**visDocViewMarkup**</span></span> <br/> |
   

