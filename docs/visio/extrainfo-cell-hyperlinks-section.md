---
title: Ячейка ExtraInfo (раздел "Гиперссылки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm360
localization_priority: Normal
ms.assetid: 55834445-8619-f79a-aea0-0f6a1780e016
description: Представляет строку, которая передает сведения, которые будут использоваться для разрешения URL-адрес, например координаты гиперкарты. Например, значение в ячейке ExtraInfo x = 41&amp;y = 7specifies координаты гиперкарты.
ms.openlocfilehash: aa035d5ec863cd8045063af970efa26b53683793
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813732"
---
# <a name="extrainfo-cell-hyperlinks-section"></a><span data-ttu-id="f33eb-104">Ячейка ExtraInfo (раздел "Гиперссылки")</span><span class="sxs-lookup"><span data-stu-id="f33eb-104">ExtraInfo Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="f33eb-105">Представляет строку, которая передает сведения, которые будут использоваться для разрешения URL-адрес, например координаты гиперкарты.</span><span class="sxs-lookup"><span data-stu-id="f33eb-105">Represents a string that passes information to be used in resolving a URL, such as the coordinates of an image map.</span></span> <span data-ttu-id="f33eb-106">Например, значение в ячейке ExtraInfo «x = 41&amp;y = 7» указывает координаты гиперкарты.</span><span class="sxs-lookup"><span data-stu-id="f33eb-106">For example, in the ExtraInfo cell, "x=41&amp;y=7" specifies the coordinates of an image map.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f33eb-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="f33eb-107">Remarks</span></span>

<span data-ttu-id="f33eb-108">Событие ячеек вычисляются только в том случае, когда возникает событие, не после ввода формул.</span><span class="sxs-lookup"><span data-stu-id="f33eb-108">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="f33eb-109">Для получения ссылки на ячейки ExtraInfo по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f33eb-109">To get a reference to the ExtraInfo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f33eb-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="f33eb-110">Cell name:</span></span>  <br/> | <span data-ttu-id="f33eb-111">Гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="f33eb-111">Hyperlink.</span></span>  <span data-ttu-id="f33eb-112">*имя* . ExtraInfo где гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="f33eb-112">*name*  .ExtraInfo            where Hyperlink.</span></span>  <span data-ttu-id="f33eb-113">*имя* — это имя строки</span><span class="sxs-lookup"><span data-stu-id="f33eb-113">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="f33eb-114">Для получения ссылки на ячейки ExtraInfo по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="f33eb-114">To get a reference to the ExtraInfo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f33eb-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f33eb-115">Section index:</span></span>  <br/> |<span data-ttu-id="f33eb-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="f33eb-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="f33eb-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f33eb-117">Row index:</span></span>  <br/> |<span data-ttu-id="f33eb-118">**visRow1stHyperlink** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f33eb-118">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f33eb-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f33eb-119">Cell index:</span></span>  <br/> |<span data-ttu-id="f33eb-120">**visHLinkExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="f33eb-120">**visHLinkExtraInfo**</span></span> <br/> |
   

