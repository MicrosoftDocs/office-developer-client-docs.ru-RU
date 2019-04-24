---
title: NewWindow Cell (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm695
localization_priority: Normal
ms.assetid: 44995137-d241-937a-c097-0f9d79203cdf
description: Указывает, следует ли открывать гиперссылку в новом окне.
ms.openlocfilehash: 0f9d1e4b1294dea3f211c8d0d69ffc49b6180066
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342233"
---
# <a name="newwindow-cell-hyperlinks-section"></a><span data-ttu-id="636a3-103">NewWindow Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="636a3-103">NewWindow Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="636a3-104">Указывает, следует ли открывать гиперссылку в новом окне.</span><span class="sxs-lookup"><span data-stu-id="636a3-104">Specifies whether to open the hyperlink in a new window.</span></span>
  
|<span data-ttu-id="636a3-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="636a3-105">**Value**</span></span>|<span data-ttu-id="636a3-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="636a3-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="636a3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="636a3-107">TRUE</span></span>  <br/> | <span data-ttu-id="636a3-108">Откройте связанную страницу, документ или веб-сайт в новом окне.</span><span class="sxs-lookup"><span data-stu-id="636a3-108">Open the linked page, document, or website in a new window.</span></span>  <br/> |
| <span data-ttu-id="636a3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="636a3-109">FALSE</span></span>  <br/> | <span data-ttu-id="636a3-110">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="636a3-110">Default.</span></span> <span data-ttu-id="636a3-111">Не открывайте новое окно для гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="636a3-111">Do not open a new window for the hyperlink.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="636a3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="636a3-112">Remarks</span></span>

<span data-ttu-id="636a3-113">Чтобы получить ссылку на ячейку NewWindow по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="636a3-113">To get a reference to the NewWindow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="636a3-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="636a3-114">Cell name:</span></span>  <br/> | <span data-ttu-id="636a3-115">Гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="636a3-115">Hyperlink.</span></span>  <span data-ttu-id="636a3-116">*Name (имя* ). NewWindow, где гиперссылка.</span><span class="sxs-lookup"><span data-stu-id="636a3-116">*Name*  .NewWindow            where Hyperlink.</span></span>  <span data-ttu-id="636a3-117">*Name* — имя строки</span><span class="sxs-lookup"><span data-stu-id="636a3-117">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="636a3-118">Чтобы получить ссылку на ячейку NewWindow по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="636a3-118">To get a reference to the NewWindow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="636a3-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="636a3-119">Section index:</span></span>  <br/> |<span data-ttu-id="636a3-120">**Виссектионхиперлинк**</span><span class="sxs-lookup"><span data-stu-id="636a3-120">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="636a3-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="636a3-121">Row index:</span></span>  <br/> |<span data-ttu-id="636a3-122">**visRow1stHyperlink** +  *i* , где *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="636a3-122">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="636a3-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="636a3-123">Cell index:</span></span>  <br/> |<span data-ttu-id="636a3-124">**Вишлинкневвин**</span><span class="sxs-lookup"><span data-stu-id="636a3-124">**visHLinkNewWin**</span></span> <br/> |
   

