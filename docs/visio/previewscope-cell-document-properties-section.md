---
title: Ячейка PreviewScope (раздел "Свойства документа")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm820
localization_priority: Normal
ms.assetid: d03ae1b3-da6c-56d3-4f96-6e131c04e93e
description: Определяет, имеется ли в документе Предварительный просмотр. Создание документа включается Предварительный просмотр, определяет, отображается ли только первой страницы или всех страниц в документе.
ms.openlocfilehash: 865da052f710481c146d3c2692ddf506018be789
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814475"
---
# <a name="previewscope-cell-document-properties-section"></a><span data-ttu-id="b367c-104">Ячейка PreviewScope (раздел "Свойства документа")</span><span class="sxs-lookup"><span data-stu-id="b367c-104">PreviewScope Cell (Document Properties Section)</span></span>

<span data-ttu-id="b367c-105">Определяет, имеется ли в документе Предварительный просмотр.</span><span class="sxs-lookup"><span data-stu-id="b367c-105">Determines whether your drawing includes a preview.</span></span> <span data-ttu-id="b367c-106">Создание документа включается Предварительный просмотр, определяет, отображается ли только первой страницы или всех страниц в документе.</span><span class="sxs-lookup"><span data-stu-id="b367c-106">If your drawing does include a preview, it determines whether the preview shows the first page only or all of the pages in the drawing.</span></span>
  
|<span data-ttu-id="b367c-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b367c-107">**Value**</span></span>|<span data-ttu-id="b367c-108">**Область предварительного просмотра**</span><span class="sxs-lookup"><span data-stu-id="b367c-108">**Preview scope**</span></span>|<span data-ttu-id="b367c-109">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="b367c-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="b367c-110">0</span><span class="sxs-lookup"><span data-stu-id="b367c-110">0</span></span>  <br/> | <span data-ttu-id="b367c-111">Первая страница</span><span class="sxs-lookup"><span data-stu-id="b367c-111">First page</span></span>  <br/> |<span data-ttu-id="b367c-112">**visDocPreviewScope1stPage**</span><span class="sxs-lookup"><span data-stu-id="b367c-112">**visDocPreviewScope1stPage**</span></span> <br/> |
| <span data-ttu-id="b367c-113">1</span><span class="sxs-lookup"><span data-stu-id="b367c-113">1</span></span>  <br/> | <span data-ttu-id="b367c-114">Нет</span><span class="sxs-lookup"><span data-stu-id="b367c-114">None</span></span>  <br/> |<span data-ttu-id="b367c-115">**visDocPreviewScopeNone**</span><span class="sxs-lookup"><span data-stu-id="b367c-115">**visDocPreviewScopeNone**</span></span> <br/> |
| <span data-ttu-id="b367c-116">2</span><span class="sxs-lookup"><span data-stu-id="b367c-116">2</span></span>  <br/> | <span data-ttu-id="b367c-117">Все страницы</span><span class="sxs-lookup"><span data-stu-id="b367c-117">All pages</span></span>  <br/> |<span data-ttu-id="b367c-118">**visDocPreviewScopeAllPages**</span><span class="sxs-lookup"><span data-stu-id="b367c-118">**visDocPreviewScopeAllPages**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b367c-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="b367c-119">Remarks</span></span>

<span data-ttu-id="b367c-120">Это значение также можно настроить на вкладке **Обзор** в диалоговом окне **Свойства** (нажмите кнопку **Office** , перейдите на вкладку **сведения** , нажмите кнопку **Свойства документа**и выберите команду **Дополнительные свойства**).</span><span class="sxs-lookup"><span data-stu-id="b367c-120">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="b367c-121">Чтобы получить ссылку на ячейку PreviewScope по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="b367c-121">To get a reference to the PreviewScope cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b367c-122">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="b367c-122">Cell name:</span></span>  <br/> | <span data-ttu-id="b367c-123">PreviewScope</span><span class="sxs-lookup"><span data-stu-id="b367c-123">PreviewScope</span></span>  <br/> |
   
<span data-ttu-id="b367c-124">Для получения ссылки на ячейки PreviewScope по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="b367c-124">To get a reference to the PreviewScope cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b367c-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b367c-125">Section index:</span></span>  <br/> |<span data-ttu-id="b367c-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b367c-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b367c-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b367c-127">Row index:</span></span>  <br/> |<span data-ttu-id="b367c-128">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="b367c-128">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="b367c-129">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b367c-129">Cell index:</span></span>  <br/> |<span data-ttu-id="b367c-130">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="b367c-130">**visDocPreviewScope**</span></span> <br/> |
   

