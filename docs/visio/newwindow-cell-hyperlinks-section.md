---
title: Ячейка NewWindow (раздел "Гиперссылки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm695
localization_priority: Normal
ms.assetid: 44995137-d241-937a-c097-0f9d79203cdf
description: Указывает, следует ли открывать гиперссылки в новом окне.
ms.openlocfilehash: 0f9d1e4b1294dea3f211c8d0d69ffc49b6180066
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396339"
---
# <a name="newwindow-cell-hyperlinks-section"></a><span data-ttu-id="b7596-103">Ячейка NewWindow (раздел "Гиперссылки")</span><span class="sxs-lookup"><span data-stu-id="b7596-103">NewWindow Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="b7596-104">Указывает, следует ли открывать гиперссылки в новом окне.</span><span class="sxs-lookup"><span data-stu-id="b7596-104">Specifies whether to open the hyperlink in a new window.</span></span>
  
|<span data-ttu-id="b7596-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b7596-105">**Value**</span></span>|<span data-ttu-id="b7596-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7596-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b7596-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b7596-107">TRUE</span></span>  <br/> | <span data-ttu-id="b7596-108">Откройте связанную страницу, документа или веб-сайт в новом окне.</span><span class="sxs-lookup"><span data-stu-id="b7596-108">Open the linked page, document, or website in a new window.</span></span>  <br/> |
| <span data-ttu-id="b7596-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b7596-109">FALSE</span></span>  <br/> | <span data-ttu-id="b7596-110">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b7596-110">Default.</span></span> <span data-ttu-id="b7596-111">Не открывать новое окно гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="b7596-111">Do not open a new window for the hyperlink.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7596-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="b7596-112">Remarks</span></span>

<span data-ttu-id="b7596-113">Чтобы получить ссылку на ячейку NewWindow по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="b7596-113">To get a reference to the NewWindow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b7596-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b7596-114">Cell name:</span></span>  <br/> | <span data-ttu-id="b7596-115">Гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="b7596-115">Hyperlink.</span></span>  <span data-ttu-id="b7596-116">*Имя* . NewWindow где гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="b7596-116">*Name*  .NewWindow            where Hyperlink.</span></span>  <span data-ttu-id="b7596-117">*Имя* — это имя строки</span><span class="sxs-lookup"><span data-stu-id="b7596-117">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="b7596-118">Для получения ссылки на ячейки NewWindow по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="b7596-118">To get a reference to the NewWindow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b7596-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b7596-119">Section index:</span></span>  <br/> |<span data-ttu-id="b7596-120">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="b7596-120">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="b7596-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b7596-121">Row index:</span></span>  <br/> |<span data-ttu-id="b7596-122">**visRow1stHyperlink** +  *i* где *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="b7596-122">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="b7596-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b7596-123">Cell index:</span></span>  <br/> |<span data-ttu-id="b7596-124">**visHLinkNewWin**</span><span class="sxs-lookup"><span data-stu-id="b7596-124">**visHLinkNewWin**</span></span> <br/> |
   

