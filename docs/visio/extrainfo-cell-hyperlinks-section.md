---
title: ExtraInfo Cell (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm360
localization_priority: Normal
ms.assetid: 55834445-8619-f79a-aea0-0f6a1780e016
description: Представляет строку, которая передает информацию, которая будет использоваться при разрешении URL-адреса, например координаты карты ссылок. Например, в ячейке ExtraInfo x = 41&amp;y = 7specifies координаты карты изображения.
ms.openlocfilehash: df2886ef7911b484cc60e8a476bfa53369fbf646
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357822"
---
# <a name="extrainfo-cell-hyperlinks-section"></a><span data-ttu-id="700b9-104">ExtraInfo Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="700b9-104">ExtraInfo Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="700b9-105">Представляет строку, которая передает информацию, которая будет использоваться при разрешении URL-адреса, например координаты карты ссылок.</span><span class="sxs-lookup"><span data-stu-id="700b9-105">Represents a string that passes information to be used in resolving a URL, such as the coordinates of an image map.</span></span> <span data-ttu-id="700b9-106">Например, в ячейке ExtraInfo "x = 41&amp;y = 7" указывает координаты гиперкарты.</span><span class="sxs-lookup"><span data-stu-id="700b9-106">For example, in the ExtraInfo cell, "x=41&amp;y=7" specifies the coordinates of an image map.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="700b9-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="700b9-107">Remarks</span></span>

<span data-ttu-id="700b9-108">Ячейки событий оцениваются только при возникновении события, а не при вводе формул.</span><span class="sxs-lookup"><span data-stu-id="700b9-108">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="700b9-109">Чтобы получить ссылку на ячейку ExtraInfo по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="700b9-109">To get a reference to the ExtraInfo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="700b9-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="700b9-110">Cell name:</span></span>  <br/> | <span data-ttu-id="700b9-111">Гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="700b9-111">Hyperlink.</span></span>  <span data-ttu-id="700b9-112">*Name (имя* ). ExtraInfo, где гиперссылка.</span><span class="sxs-lookup"><span data-stu-id="700b9-112">*name*  .ExtraInfo            where Hyperlink.</span></span>  <span data-ttu-id="700b9-113">*Name* — имя строки</span><span class="sxs-lookup"><span data-stu-id="700b9-113">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="700b9-114">Чтобы получить ссылку на ячейку ExtraInfo по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="700b9-114">To get a reference to the ExtraInfo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="700b9-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="700b9-115">Section index:</span></span>  <br/> |<span data-ttu-id="700b9-116">**Виссектионхиперлинк**</span><span class="sxs-lookup"><span data-stu-id="700b9-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="700b9-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="700b9-117">Row index:</span></span>  <br/> |<span data-ttu-id="700b9-118">**visRow1stHyperlink** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="700b9-118">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="700b9-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="700b9-119">Cell index:</span></span>  <br/> |<span data-ttu-id="700b9-120">**Вишлинкекстраинфо**</span><span class="sxs-lookup"><span data-stu-id="700b9-120">**visHLinkExtraInfo**</span></span> <br/> |
   

