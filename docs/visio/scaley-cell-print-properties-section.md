---
title: Ячейка ScaleY (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
localization_priority: Normal
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: Указывает процент увеличения страницы документа на странице принтера.
ms.openlocfilehash: 2735b2cfce04cc9a8d8da1a815081aaa5892c723
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814724"
---
# <a name="scaley-cell-print-properties-section"></a><span data-ttu-id="e3ab8-103">Ячейка ScaleY (раздел "Свойства печати")</span><span class="sxs-lookup"><span data-stu-id="e3ab8-103">ScaleY Cell (Print Properties Section)</span></span>

<span data-ttu-id="e3ab8-104">Указывает процент увеличения страницы документа на странице принтера.</span><span class="sxs-lookup"><span data-stu-id="e3ab8-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e3ab8-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="e3ab8-105">Remarks</span></span>

<span data-ttu-id="e3ab8-106">Это значение используется только в том случае, если значение ячейки OnPage — FALSE.</span><span class="sxs-lookup"><span data-stu-id="e3ab8-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="e3ab8-107">Ячейки ScaleX и ScaleY всегда с таким же значением, который соответствует значению в параметре **обеспечить, чтобы** на вкладке **Параметры печати** в диалоговом окне " **Параметры страницы** " (на вкладке " **Конструктор** ", щелкните стрелку **Параметры страницы** ).</span><span class="sxs-lookup"><span data-stu-id="e3ab8-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="e3ab8-108">Для получения ссылки на ячейки ScaleY по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e3ab8-108">To get a reference to the ScaleY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3ab8-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="e3ab8-109">Cell name:</span></span>  <br/> |<span data-ttu-id="e3ab8-110">ScaleY</span><span class="sxs-lookup"><span data-stu-id="e3ab8-110">ScaleY</span></span>  <br/> |
   
<span data-ttu-id="e3ab8-111">Для получения ссылки на ячейки ScaleY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="e3ab8-111">To get a reference to the ScaleY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3ab8-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e3ab8-112">Section index:</span></span>  <br/> |<span data-ttu-id="e3ab8-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e3ab8-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e3ab8-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e3ab8-114">Row index:</span></span>  <br/> |<span data-ttu-id="e3ab8-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="e3ab8-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="e3ab8-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e3ab8-116">Cell index:</span></span>  <br/> |<span data-ttu-id="e3ab8-117">**visPrintPropertiesScaleY**</span><span class="sxs-lookup"><span data-stu-id="e3ab8-117">**visPrintPropertiesScaleY**</span></span> <br/> |
   

