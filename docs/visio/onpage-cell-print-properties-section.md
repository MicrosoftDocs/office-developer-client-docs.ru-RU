---
title: OnPage Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033793
localization_priority: Normal
ms.assetid: 4015506a-e24a-0276-c854-7791a7019067
description: Указывает, печатается ли документ на определенном числе страниц принтера.
ms.openlocfilehash: 61d45a5bffdbb1afd5db9c608f80bc4f797f5191
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439606"
---
# <a name="onpage-cell-print-properties-section"></a><span data-ttu-id="b8b47-103">OnPage Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="b8b47-103">OnPage Cell (Print Properties Section)</span></span>

<span data-ttu-id="b8b47-104">Указывает, печатается ли документ на определенном числе страниц принтера.</span><span class="sxs-lookup"><span data-stu-id="b8b47-104">Indicates whether the drawing is printed on a specific number of printer pages.</span></span> 
  
|<span data-ttu-id="b8b47-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b8b47-105">**Value**</span></span>|<span data-ttu-id="b8b47-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b8b47-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b8b47-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b8b47-107">TRUE</span></span>  <br/> |<span data-ttu-id="b8b47-108">ПодГонку страницы документа к определенному числу страниц принтера.</span><span class="sxs-lookup"><span data-stu-id="b8b47-108">Fit the drawing page to a defined number of printer pages.</span></span>  <br/> |
|<span data-ttu-id="b8b47-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b8b47-109">FALSE</span></span>  <br/> |<span data-ttu-id="b8b47-110">Не подгонять страницу документа к определенному количеству страниц принтера (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="b8b47-110">Do not fit the drawing page to a defined number of printer pages (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8b47-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="b8b47-111">Remarks</span></span>

<span data-ttu-id="b8b47-112">Если ячейка onPage имеет значение TRUE, в Microsoft Visio используются ячейки PagesX и Pages, чтобы определить количество страниц принтера, на которых будет расположиться документ.</span><span class="sxs-lookup"><span data-stu-id="b8b47-112">If the OnPage cell is set to TRUE, Microsoft Visio uses the PagesX and PagesY cells to determine the number of printer pages on which to fit the drawing.</span></span> <span data-ttu-id="b8b47-113">Значения в ячейках ScaleX и Scale игнорируются.</span><span class="sxs-lookup"><span data-stu-id="b8b47-113">Values in the ScaleX and ScaleY cells are ignored.</span></span> <span data-ttu-id="b8b47-114">Этот параметр можно считать параметром "автомасштабирование".</span><span class="sxs-lookup"><span data-stu-id="b8b47-114">This can be considered an "autoscale" setting.</span></span>
  
<span data-ttu-id="b8b47-115">Это значение соответствует параметру " **разместить** на" на вкладке " **Настройка печати** " диалогового окна " **Параметры страницы** " (на вкладке " **конструктор** " щелкните стрелку **Параметры страницы** ).</span><span class="sxs-lookup"><span data-stu-id="b8b47-115">This value corresponds to the **Fit to** option on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) .</span></span> 
  
<span data-ttu-id="b8b47-116">Чтобы получить ссылку на ячейку onPage по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="b8b47-116">To get a reference to the OnPage cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b8b47-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b8b47-117">Cell name:</span></span>  <br/> |<span data-ttu-id="b8b47-118">OnPage</span><span class="sxs-lookup"><span data-stu-id="b8b47-118">OnPage</span></span>  <br/> |
   
<span data-ttu-id="b8b47-119">Чтобы получить ссылку на ячейку onPage по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b8b47-119">To get a reference to the OnPage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b8b47-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b8b47-120">Section index:</span></span>  <br/> |<span data-ttu-id="b8b47-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b8b47-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b8b47-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b8b47-122">Row index:</span></span>  <br/> |<span data-ttu-id="b8b47-123">**Висровпринтпропертиес**</span><span class="sxs-lookup"><span data-stu-id="b8b47-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="b8b47-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b8b47-124">Cell index:</span></span>  <br/> |<span data-ttu-id="b8b47-125">**Виспринтпропертиесонпаже**</span><span class="sxs-lookup"><span data-stu-id="b8b47-125">**visPrintPropertiesOnPage**</span></span> <br/> |
   

