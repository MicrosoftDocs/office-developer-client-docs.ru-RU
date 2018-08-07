---
title: Ячейка ViewMarkup (раздел "Свойства документа")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
localization_priority: Normal
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: Определяет, отображается ли разметка в окне документа.
ms.openlocfilehash: dda908595b243878ec755cf73351ec1fd672dc55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815157"
---
# <a name="viewmarkup-cell-document-properties-section"></a><span data-ttu-id="8bb62-103">Ячейка ViewMarkup (раздел "Свойства документа")</span><span class="sxs-lookup"><span data-stu-id="8bb62-103">ViewMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="8bb62-104">Определяет, отображается ли разметка в окне документа.</span><span class="sxs-lookup"><span data-stu-id="8bb62-104">Determines whether markup appears in the drawing window.</span></span> 
  
|<span data-ttu-id="8bb62-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8bb62-105">**Value**</span></span>|<span data-ttu-id="8bb62-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8bb62-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8bb62-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="8bb62-107">TRUE</span></span>  <br/> |<span data-ttu-id="8bb62-108">Разметка отображается в документе.</span><span class="sxs-lookup"><span data-stu-id="8bb62-108">Markup is displayed on the drawing.</span></span>  <br/> |
|<span data-ttu-id="8bb62-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="8bb62-109">FALSE</span></span>  <br/> |<span data-ttu-id="8bb62-110">Разметка не отображаются (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="8bb62-110">Markup is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8bb62-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="8bb62-111">Remarks</span></span>

 <span data-ttu-id="8bb62-112">При включении отслеживания разметки (ячейки AddMarkup имеет значение TRUE), ViewMarkup ячейки автоматически устанавливается значение TRUE и остается равным TRUE даже после разметки трассировка отключена (ячейки AddMarkup — значение FALSE).</span><span class="sxs-lookup"><span data-stu-id="8bb62-112">When markup tracking is turned on (AddMarkup cell is TRUE), the ViewMarkup cell is automatically set to TRUE and remains TRUE even after markup tracking has been turned off (AddMarkup cell is FALSE).</span></span> <span data-ttu-id="8bb62-113">Значение в ячейке ViewMarkup игнорируется, если ячейка AddMarkup имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="8bb62-113">The value in the ViewMarkup cell is ignored when the AddMarkup cell is TRUE.</span></span> 
  
<span data-ttu-id="8bb62-114">Ячейка ViewMarkup также имеет значение TRUE, когда комментариев вставляется в документе, (ли отслеживание исправлений включено) и должно быть значение true, чтобы см. комментарии в документе.</span><span class="sxs-lookup"><span data-stu-id="8bb62-114">The ViewMarkup cell is also set to TRUE when comments are inserted in a drawing (whether or not markup tracking is turned on) and must be TRUE to see comments in the drawing.</span></span>
  
<span data-ttu-id="8bb62-115">В этой ячейке соответствует команда **Показать исправления** в группе **разметки** на вкладке **Обзор** .</span><span class="sxs-lookup"><span data-stu-id="8bb62-115">This cell corresponds to the **Show Markup** command in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="8bb62-116">Чтобы получить ссылку на ячейку ViewMarkup по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="8bb62-116">To get a reference to the ViewMarkup cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8bb62-117">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="8bb62-117">Cell name:</span></span>  <br/> |<span data-ttu-id="8bb62-118">ViewMarkup</span><span class="sxs-lookup"><span data-stu-id="8bb62-118">ViewMarkup</span></span>  <br/> |
   
<span data-ttu-id="8bb62-119">Для получения ссылки на ячейки ViewMarkup по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="8bb62-119">To get a reference to the ViewMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8bb62-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8bb62-120">Section index:</span></span>  <br/> |<span data-ttu-id="8bb62-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8bb62-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8bb62-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8bb62-122">Row index:</span></span>  <br/> |<span data-ttu-id="8bb62-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="8bb62-123">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="8bb62-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8bb62-124">Cell index:</span></span>  <br/> |<span data-ttu-id="8bb62-125">**visDocViewMarkup**</span><span class="sxs-lookup"><span data-stu-id="8bb62-125">**visDocViewMarkup**</span></span> <br/> |
   

