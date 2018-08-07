---
title: Ячейка Frame (раздел "Гиперссылки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm405
localization_priority: Normal
ms.assetid: f71d8737-92ef-1124-ba4a-b7e17305bd0a
description: Представляет имя frame конечного при открытом как активный документ в приложении контейнера приложения. По умолчанию используется пустая строка.
ms.openlocfilehash: b94e5efd4a3fdf53e01f7518252852214a72c766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813830"
---
# <a name="frame-cell-hyperlinks-section"></a><span data-ttu-id="93968-104">Ячейка Frame (раздел "Гиперссылки")</span><span class="sxs-lookup"><span data-stu-id="93968-104">Frame Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="93968-105">Представляет имя frame конечного при открытом как активный документ в приложении контейнера приложения.</span><span class="sxs-lookup"><span data-stu-id="93968-105">Represents the name of a frame to target when the application is open as an Active document in a container application.</span></span> <span data-ttu-id="93968-106">По умолчанию используется пустая строка.</span><span class="sxs-lookup"><span data-stu-id="93968-106">The default is an empty string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="93968-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="93968-107">Remarks</span></span>

<span data-ttu-id="93968-108">Для получения ссылки на ячейки Frame с именем, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="93968-108">To get a reference to the Frame cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="93968-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="93968-109">Cell name:</span></span>  <br/> | <span data-ttu-id="93968-110">Гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="93968-110">Hyperlink.</span></span>  <span data-ttu-id="93968-111">*имя* . Помещался where гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="93968-111">*name*  .Frame            where Hyperlink.</span></span>  <span data-ttu-id="93968-112">*имя* — это имя строки</span><span class="sxs-lookup"><span data-stu-id="93968-112">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="93968-113">Для получения ссылки на ячейки Frame с индекса из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="93968-113">To get a reference to the Frame cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="93968-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="93968-114">Section index:</span></span>  <br/> |<span data-ttu-id="93968-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="93968-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="93968-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="93968-116">Row index:</span></span>  <br/> |<span data-ttu-id="93968-117">**visRow1stHyperlink** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="93968-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="93968-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="93968-118">Cell index:</span></span>  <br/> |<span data-ttu-id="93968-119">**visHLinkFrame**</span><span class="sxs-lookup"><span data-stu-id="93968-119">**visHLinkFrame**</span></span> <br/> |
   

