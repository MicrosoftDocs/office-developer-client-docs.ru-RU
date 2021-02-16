---
title: PreviewScope Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm820
localization_priority: Normal
ms.assetid: d03ae1b3-da6c-56d3-4f96-6e131c04e93e
description: Определяет, включает ли ваш рисунок предварительный просмотр. Если в вашем рисунке есть предварительный просмотр, он определяет, будет ли в режиме предварительного просмотра показана только первая страница или все страницы в этом рисунке.
ms.openlocfilehash: 34dbc9ac02032b2cb5cb6373c3c6361e3d822312
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426508"
---
# <a name="previewscope-cell-document-properties-section"></a><span data-ttu-id="d03db-104">PreviewScope Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="d03db-104">PreviewScope Cell (Document Properties Section)</span></span>

<span data-ttu-id="d03db-105">Определяет, включает ли ваш рисунок предварительный просмотр.</span><span class="sxs-lookup"><span data-stu-id="d03db-105">Determines whether your drawing includes a preview.</span></span> <span data-ttu-id="d03db-106">Если в вашем рисунке есть предварительный просмотр, он определяет, будет ли в режиме предварительного просмотра показана только первая страница или все страницы в этом рисунке.</span><span class="sxs-lookup"><span data-stu-id="d03db-106">If your drawing does include a preview, it determines whether the preview shows the first page only or all of the pages in the drawing.</span></span>
  
|<span data-ttu-id="d03db-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="d03db-107">**Value**</span></span>|<span data-ttu-id="d03db-108">**Область предварительного просмотра**</span><span class="sxs-lookup"><span data-stu-id="d03db-108">**Preview scope**</span></span>|<span data-ttu-id="d03db-109">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="d03db-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="d03db-110">0</span><span class="sxs-lookup"><span data-stu-id="d03db-110">0</span></span>  <br/> | <span data-ttu-id="d03db-111">Первая страница</span><span class="sxs-lookup"><span data-stu-id="d03db-111">First page</span></span>  <br/> |<span data-ttu-id="d03db-112">**visDocPreviewScope1stPage**</span><span class="sxs-lookup"><span data-stu-id="d03db-112">**visDocPreviewScope1stPage**</span></span> <br/> |
| <span data-ttu-id="d03db-113">1 </span><span class="sxs-lookup"><span data-stu-id="d03db-113">1</span></span>  <br/> | <span data-ttu-id="d03db-114">Нет</span><span class="sxs-lookup"><span data-stu-id="d03db-114">None</span></span>  <br/> |<span data-ttu-id="d03db-115">**visDocPreviewScopeNone**</span><span class="sxs-lookup"><span data-stu-id="d03db-115">**visDocPreviewScopeNone**</span></span> <br/> |
| <span data-ttu-id="d03db-116">2 </span><span class="sxs-lookup"><span data-stu-id="d03db-116">2</span></span>  <br/> | <span data-ttu-id="d03db-117">Все страницы</span><span class="sxs-lookup"><span data-stu-id="d03db-117">All pages</span></span>  <br/> |<span data-ttu-id="d03db-118">**visDocPreviewScopeAllPages**</span><span class="sxs-lookup"><span data-stu-id="d03db-118">**visDocPreviewScopeAllPages**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d03db-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="d03db-119">Remarks</span></span>

<span data-ttu-id="d03db-120">Это значение также можно  установить на вкладке "Сводка" в диалоговом окне "Свойства" (нажмите кнопку **"Office",** выберите вкладку "Сведения", "Свойства документа" и "Дополнительные **свойства").**  </span><span class="sxs-lookup"><span data-stu-id="d03db-120">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="d03db-121">Чтобы получить ссылку на ячейку PreviewScope по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="d03db-121">To get a reference to the PreviewScope cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d03db-122">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d03db-122">Cell name:</span></span>  <br/> | <span data-ttu-id="d03db-123">PreviewScope</span><span class="sxs-lookup"><span data-stu-id="d03db-123">PreviewScope</span></span>  <br/> |
   
<span data-ttu-id="d03db-124">Чтобы получить ссылку на ячейку PreviewScope по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d03db-124">To get a reference to the PreviewScope cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d03db-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d03db-125">Section index:</span></span>  <br/> |<span data-ttu-id="d03db-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d03db-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d03db-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d03db-127">Row index:</span></span>  <br/> |<span data-ttu-id="d03db-128">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="d03db-128">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="d03db-129">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d03db-129">Cell index:</span></span>  <br/> |<span data-ttu-id="d03db-130">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="d03db-130">**visDocPreviewScope**</span></span> <br/> |
   

