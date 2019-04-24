---
title: Frame Cell (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm405
localization_priority: Normal
ms.assetid: f71d8737-92ef-1124-ba4a-b7e17305bd0a
description: Представляет имя целевого кадра, когда приложение открыто как активный документ в контейнерном приложении. Значение по умолчанию — пустая строка.
ms.openlocfilehash: 8f41e5bf854e31e1f17eabb2aecbded55175ebaf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344856"
---
# <a name="frame-cell-hyperlinks-section"></a><span data-ttu-id="193de-104">Frame Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="193de-104">Frame Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="193de-105">Представляет имя целевого кадра, когда приложение открыто как активный документ в контейнерном приложении.</span><span class="sxs-lookup"><span data-stu-id="193de-105">Represents the name of a frame to target when the application is open as an Active document in a container application.</span></span> <span data-ttu-id="193de-106">Значение по умолчанию — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="193de-106">The default is an empty string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="193de-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="193de-107">Remarks</span></span>

<span data-ttu-id="193de-108">Чтобы получить ссылку на ячейку Frame по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="193de-108">To get a reference to the Frame cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="193de-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="193de-109">Cell name:</span></span>  <br/> | <span data-ttu-id="193de-110">Гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="193de-110">Hyperlink.</span></span>  <span data-ttu-id="193de-111">*Name (имя* ). Frame с гиперссылкой.</span><span class="sxs-lookup"><span data-stu-id="193de-111">*name*  .Frame            where Hyperlink.</span></span>  <span data-ttu-id="193de-112">*Name* — имя строки</span><span class="sxs-lookup"><span data-stu-id="193de-112">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="193de-113">Чтобы получить ссылку на ячейку Frame по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="193de-113">To get a reference to the Frame cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="193de-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="193de-114">Section index:</span></span>  <br/> |<span data-ttu-id="193de-115">**Виссектионхиперлинк**</span><span class="sxs-lookup"><span data-stu-id="193de-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="193de-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="193de-116">Row index:</span></span>  <br/> |<span data-ttu-id="193de-117">**visRow1stHyperlink** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="193de-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="193de-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="193de-118">Cell index:</span></span>  <br/> |<span data-ttu-id="193de-119">**Вишлинкфраме**</span><span class="sxs-lookup"><span data-stu-id="193de-119">**visHLinkFrame**</span></span> <br/> |
   

