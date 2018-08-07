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
ms.openlocfilehash: b4d927e1970e994047df3cb89afa7799a825511d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814296"
---
# <a name="newwindow-cell-hyperlinks-section"></a><span data-ttu-id="2a2e0-103">Ячейка NewWindow (раздел "Гиперссылки")</span><span class="sxs-lookup"><span data-stu-id="2a2e0-103">NewWindow Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="2a2e0-104">Указывает, следует ли открывать гиперссылки в новом окне.</span><span class="sxs-lookup"><span data-stu-id="2a2e0-104">Specifies whether to open the hyperlink in a new window.</span></span>
  
|<span data-ttu-id="2a2e0-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="2a2e0-105">**Value**</span></span>|<span data-ttu-id="2a2e0-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2a2e0-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2a2e0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2a2e0-107">TRUE</span></span>  <br/> | <span data-ttu-id="2a2e0-108">Откройте связанную страницу, документа или веб-сайта в новом окне.</span><span class="sxs-lookup"><span data-stu-id="2a2e0-108">Open the linked page, document, or Web site in a new window.</span></span>  <br/> |
| <span data-ttu-id="2a2e0-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2a2e0-109">FALSE</span></span>  <br/> | <span data-ttu-id="2a2e0-110">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2a2e0-110">Default.</span></span> <span data-ttu-id="2a2e0-111">Не открывать новое окно гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="2a2e0-111">Do not open a new window for the hyperlink.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a2e0-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="2a2e0-112">Remarks</span></span>

<span data-ttu-id="2a2e0-113">Чтобы получить ссылку на ячейку NewWindow по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="2a2e0-113">To get a reference to the NewWindow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2a2e0-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="2a2e0-114">Cell name:</span></span>  <br/> | <span data-ttu-id="2a2e0-115">Гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="2a2e0-115">Hyperlink.</span></span>  <span data-ttu-id="2a2e0-116">*Имя* . NewWindow где гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="2a2e0-116">*Name*  .NewWindow            where Hyperlink.</span></span>  <span data-ttu-id="2a2e0-117">*Имя* — это имя строки</span><span class="sxs-lookup"><span data-stu-id="2a2e0-117">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="2a2e0-118">Для получения ссылки на ячейки NewWindow по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="2a2e0-118">To get a reference to the NewWindow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2a2e0-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2a2e0-119">Section index:</span></span>  <br/> |<span data-ttu-id="2a2e0-120">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="2a2e0-120">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="2a2e0-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2a2e0-121">Row index:</span></span>  <br/> |<span data-ttu-id="2a2e0-122">**visRow1stHyperlink** +  *i* где *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="2a2e0-122">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="2a2e0-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2a2e0-123">Cell index:</span></span>  <br/> |<span data-ttu-id="2a2e0-124">**visHLinkNewWin**</span><span class="sxs-lookup"><span data-stu-id="2a2e0-124">**visHLinkNewWin**</span></span> <br/> |
   

