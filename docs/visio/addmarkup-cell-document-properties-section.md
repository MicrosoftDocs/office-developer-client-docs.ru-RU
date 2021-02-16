---
title: AddMarkup Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030801
localization_priority: Normal
ms.assetid: 46146424-b4c9-2240-36c0-19bb35ec51d1
description: Указывает, просматривается ли документ на разметку.
ms.openlocfilehash: 4e0860639b0d89fce2c35a8947bd5ac00fcc63e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427635"
---
# <a name="addmarkup-cell-document-properties-section"></a><span data-ttu-id="68345-103">AddMarkup Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="68345-103">AddMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="68345-104">Указывает, просматривается ли документ на разметку.</span><span class="sxs-lookup"><span data-stu-id="68345-104">Indicates whether the document is being reviewed for markup.</span></span>
  
|<span data-ttu-id="68345-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="68345-105">**Value**</span></span>|<span data-ttu-id="68345-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="68345-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="68345-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="68345-107">TRUE</span></span>  <br/> |<span data-ttu-id="68345-108">Документ просматривается.</span><span class="sxs-lookup"><span data-stu-id="68345-108">Document is being reviewed.</span></span>  <br/> |
|<span data-ttu-id="68345-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="68345-109">FALSE</span></span>  <br/> |<span data-ttu-id="68345-110">Документ не просматривается (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="68345-110">Document is not being reviewed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68345-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="68345-111">Remarks</span></span>

<span data-ttu-id="68345-112">Если для ячейки AddMarkup установлено true, рецензент добавляет разметку, и изменения применяются к страницам наложения разметки, а не к исходным страницам рисования.</span><span class="sxs-lookup"><span data-stu-id="68345-112">When the AddMarkup cell is set to TRUE, the reviewer is adding markup and changes are applied to markup overlay pages, not to original drawing pages.</span></span> <span data-ttu-id="68345-113">Если ячейка AddMarkup имеет false, отслеживание разметки отключено и изменения применяются к исходным страницам рисования.</span><span class="sxs-lookup"><span data-stu-id="68345-113">When the AddMarkup cell is FALSE, markup tracking is off and changes are applied to the original drawing pages.</span></span>
  
> [!NOTE]
> <span data-ttu-id="68345-114">Вы можете запретить разметку документов с помощью функции GUARD.</span><span class="sxs-lookup"><span data-stu-id="68345-114">You can prevent markup on your documents by using the GUARD function.</span></span> <span data-ttu-id="68345-115">Если ячейка AddMarkup содержит формулу =GUARD(FALSE), команда **разметки Track** отключена.</span><span class="sxs-lookup"><span data-stu-id="68345-115">If the AddMarkup cell contains the formula =GUARD(FALSE), the **Track Markup** command is disabled.</span></span> 
  
<span data-ttu-id="68345-116">Этот параметр соответствует параметру команды **"Отслеживание разметки"** в группе **разметки** на вкладке **"Просмотр".**</span><span class="sxs-lookup"><span data-stu-id="68345-116">This setting corresponds to the **Track Markup** command setting in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="68345-117">Чтобы получить ссылку на ячейку AddMarkup по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="68345-117">To get a reference to the AddMarkup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68345-118">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="68345-118">Cell name:</span></span>  <br/> |<span data-ttu-id="68345-119">AddMarkup</span><span class="sxs-lookup"><span data-stu-id="68345-119">AddMarkup</span></span>  <br/> |
   
<span data-ttu-id="68345-120">Чтобы получить ссылку на ячейку AddMarkup по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="68345-120">To get a reference to the AddMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68345-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="68345-121">Section index:</span></span>  <br/> |<span data-ttu-id="68345-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="68345-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="68345-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="68345-123">Row index:</span></span>  <br/> |<span data-ttu-id="68345-124">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="68345-124">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="68345-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="68345-125">Cell index:</span></span>  <br/> |<span data-ttu-id="68345-126">**visDocAddMarkup**</span><span class="sxs-lookup"><span data-stu-id="68345-126">**visDocAddMarkup**</span></span> <br/> |
   

