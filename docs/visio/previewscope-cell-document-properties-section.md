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
description: Определяет, включает ли ваш рисунок предварительный просмотр. Если на рисунке содержится предварительный просмотр, он определяет, показывает ли предварительный просмотр только первую страницу или все страницы в рисунке.
ms.openlocfilehash: 34dbc9ac02032b2cb5cb6373c3c6361e3d822312
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426508"
---
# <a name="previewscope-cell-document-properties-section"></a><span data-ttu-id="922d6-104">PreviewScope Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="922d6-104">PreviewScope Cell (Document Properties Section)</span></span>

<span data-ttu-id="922d6-105">Определяет, включает ли ваш рисунок предварительный просмотр.</span><span class="sxs-lookup"><span data-stu-id="922d6-105">Determines whether your drawing includes a preview.</span></span> <span data-ttu-id="922d6-106">Если на рисунке содержится предварительный просмотр, он определяет, показывает ли предварительный просмотр только первую страницу или все страницы в рисунке.</span><span class="sxs-lookup"><span data-stu-id="922d6-106">If your drawing does include a preview, it determines whether the preview shows the first page only or all of the pages in the drawing.</span></span>
  
|<span data-ttu-id="922d6-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="922d6-107">**Value**</span></span>|<span data-ttu-id="922d6-108">**Область предварительного просмотра**</span><span class="sxs-lookup"><span data-stu-id="922d6-108">**Preview scope**</span></span>|<span data-ttu-id="922d6-109">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="922d6-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="922d6-110">0</span><span class="sxs-lookup"><span data-stu-id="922d6-110">0</span></span>  <br/> | <span data-ttu-id="922d6-111">Первая страница</span><span class="sxs-lookup"><span data-stu-id="922d6-111">First page</span></span>  <br/> |<span data-ttu-id="922d6-112">**visDocPreviewScope1stPage**</span><span class="sxs-lookup"><span data-stu-id="922d6-112">**visDocPreviewScope1stPage**</span></span> <br/> |
| <span data-ttu-id="922d6-113">1</span><span class="sxs-lookup"><span data-stu-id="922d6-113">1</span></span>  <br/> | <span data-ttu-id="922d6-114">Нет</span><span class="sxs-lookup"><span data-stu-id="922d6-114">None</span></span>  <br/> |<span data-ttu-id="922d6-115">**visDocPreviewScopeNone**</span><span class="sxs-lookup"><span data-stu-id="922d6-115">**visDocPreviewScopeNone**</span></span> <br/> |
| <span data-ttu-id="922d6-116">2</span><span class="sxs-lookup"><span data-stu-id="922d6-116">2</span></span>  <br/> | <span data-ttu-id="922d6-117">Все страницы</span><span class="sxs-lookup"><span data-stu-id="922d6-117">All pages</span></span>  <br/> |<span data-ttu-id="922d6-118">**visDocPreviewScopeAllPages**</span><span class="sxs-lookup"><span data-stu-id="922d6-118">**visDocPreviewScopeAllPages**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="922d6-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="922d6-119">Remarks</span></span>

<span data-ttu-id="922d6-120">Это значение также можно задать на  вкладке **Сводка** в диалоговом окне Свойства (нажмите кнопку **Office,** нажмите вкладку **Info,** нажмите кнопку **Свойства** документа и нажмите кнопку **Расширенные свойства).**</span><span class="sxs-lookup"><span data-stu-id="922d6-120">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="922d6-121">Чтобы получить ссылку на ячейку PreviewScope по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="922d6-121">To get a reference to the PreviewScope cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="922d6-122">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="922d6-122">Cell name:</span></span>  <br/> | <span data-ttu-id="922d6-123">PreviewScope</span><span class="sxs-lookup"><span data-stu-id="922d6-123">PreviewScope</span></span>  <br/> |
   
<span data-ttu-id="922d6-124">Чтобы получить ссылку на ячейку PreviewScope по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="922d6-124">To get a reference to the PreviewScope cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="922d6-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="922d6-125">Section index:</span></span>  <br/> |<span data-ttu-id="922d6-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="922d6-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="922d6-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="922d6-127">Row index:</span></span>  <br/> |<span data-ttu-id="922d6-128">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="922d6-128">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="922d6-129">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="922d6-129">Cell index:</span></span>  <br/> |<span data-ttu-id="922d6-130">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="922d6-130">**visDocPreviewScope**</span></span> <br/> |
   

