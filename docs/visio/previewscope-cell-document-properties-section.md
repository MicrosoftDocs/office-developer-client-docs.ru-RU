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
description: Определяет, содержит ли документ предварительный просмотр. Если в документе есть предварительный просмотр, он определяет, отображается ли в предварительном просмотре только первая страница или все страницы документа.
ms.openlocfilehash: 34dbc9ac02032b2cb5cb6373c3c6361e3d822312
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426508"
---
# <a name="previewscope-cell-document-properties-section"></a><span data-ttu-id="487d7-104">PreviewScope Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="487d7-104">PreviewScope Cell (Document Properties Section)</span></span>

<span data-ttu-id="487d7-105">Определяет, содержит ли документ предварительный просмотр.</span><span class="sxs-lookup"><span data-stu-id="487d7-105">Determines whether your drawing includes a preview.</span></span> <span data-ttu-id="487d7-106">Если в документе есть предварительный просмотр, он определяет, отображается ли в предварительном просмотре только первая страница или все страницы документа.</span><span class="sxs-lookup"><span data-stu-id="487d7-106">If your drawing does include a preview, it determines whether the preview shows the first page only or all of the pages in the drawing.</span></span>
  
|<span data-ttu-id="487d7-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="487d7-107">**Value**</span></span>|<span data-ttu-id="487d7-108">**Область предварительного просмотра**</span><span class="sxs-lookup"><span data-stu-id="487d7-108">**Preview scope**</span></span>|<span data-ttu-id="487d7-109">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="487d7-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="487d7-110">нуль</span><span class="sxs-lookup"><span data-stu-id="487d7-110">0</span></span>  <br/> | <span data-ttu-id="487d7-111">Первая страница</span><span class="sxs-lookup"><span data-stu-id="487d7-111">First page</span></span>  <br/> |<span data-ttu-id="487d7-112">**visDocPreviewScope1stPage**</span><span class="sxs-lookup"><span data-stu-id="487d7-112">**visDocPreviewScope1stPage**</span></span> <br/> |
| <span data-ttu-id="487d7-113">1,1</span><span class="sxs-lookup"><span data-stu-id="487d7-113">1</span></span>  <br/> | <span data-ttu-id="487d7-114">Нет</span><span class="sxs-lookup"><span data-stu-id="487d7-114">None</span></span>  <br/> |<span data-ttu-id="487d7-115">**Висдокпревиевскопеноне**</span><span class="sxs-lookup"><span data-stu-id="487d7-115">**visDocPreviewScopeNone**</span></span> <br/> |
| <span data-ttu-id="487d7-116">2</span><span class="sxs-lookup"><span data-stu-id="487d7-116">2</span></span>  <br/> | <span data-ttu-id="487d7-117">Все страницы</span><span class="sxs-lookup"><span data-stu-id="487d7-117">All pages</span></span>  <br/> |<span data-ttu-id="487d7-118">**Висдокпревиевскопеаллпажес**</span><span class="sxs-lookup"><span data-stu-id="487d7-118">**visDocPreviewScopeAllPages**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="487d7-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="487d7-119">Remarks</span></span>

<span data-ttu-id="487d7-120">Это значение можно также задать на вкладке **Сводка** диалогового окна **Свойства** (нажмите кнопку **Office** , перейдите на вкладку **сведения** , щелкните **Свойства документа**, а затем выберите **Дополнительные свойства**).</span><span class="sxs-lookup"><span data-stu-id="487d7-120">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="487d7-121">Чтобы получить ссылку на ячейку PreviewScope по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="487d7-121">To get a reference to the PreviewScope cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="487d7-122">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="487d7-122">Cell name:</span></span>  <br/> | <span data-ttu-id="487d7-123">PreviewScope</span><span class="sxs-lookup"><span data-stu-id="487d7-123">PreviewScope</span></span>  <br/> |
   
<span data-ttu-id="487d7-124">Чтобы получить ссылку на ячейку PreviewScope по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="487d7-124">To get a reference to the PreviewScope cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="487d7-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="487d7-125">Section index:</span></span>  <br/> |<span data-ttu-id="487d7-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="487d7-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="487d7-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="487d7-127">Row index:</span></span>  <br/> |<span data-ttu-id="487d7-128">**Висровдок**</span><span class="sxs-lookup"><span data-stu-id="487d7-128">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="487d7-129">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="487d7-129">Cell index:</span></span>  <br/> |<span data-ttu-id="487d7-130">**Висдокпревиевскопе**</span><span class="sxs-lookup"><span data-stu-id="487d7-130">**visDocPreviewScope**</span></span> <br/> |
   

