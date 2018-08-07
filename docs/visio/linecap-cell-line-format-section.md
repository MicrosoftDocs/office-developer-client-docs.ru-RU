---
title: Ячейка LineCap (раздел "Формат линий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251231
localization_priority: Normal
ms.assetid: 3519216b-b6cf-2e8c-e20f-adfa373c9028
description: Указывает, будет ли строки скругленные, квадратные или расширенные отрезков.
ms.openlocfilehash: 1bd427801e6d95ce6167fa9681da2c567307f072
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814080"
---
# <a name="linecap-cell-line-format-section"></a><span data-ttu-id="5fa36-103">Ячейка LineCap (раздел "Формат линий")</span><span class="sxs-lookup"><span data-stu-id="5fa36-103">LineCap Cell (Line Format Section)</span></span>

<span data-ttu-id="5fa36-104">Указывает, будет ли строки скругленные, квадратные или расширенные отрезков.</span><span class="sxs-lookup"><span data-stu-id="5fa36-104">Indicates whether a line has rounded, square, or extended line caps.</span></span>
  
|<span data-ttu-id="5fa36-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5fa36-105">**Value**</span></span>|<span data-ttu-id="5fa36-106">**Стиль конца строки**</span><span class="sxs-lookup"><span data-stu-id="5fa36-106">**Line end style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5fa36-107">0</span><span class="sxs-lookup"><span data-stu-id="5fa36-107">0</span></span>  <br/> |<span data-ttu-id="5fa36-108">Округленный</span><span class="sxs-lookup"><span data-stu-id="5fa36-108">Rounded</span></span>  <br/> |
|<span data-ttu-id="5fa36-109">1</span><span class="sxs-lookup"><span data-stu-id="5fa36-109">1</span></span>  <br/> |<span data-ttu-id="5fa36-110">Квадратный</span><span class="sxs-lookup"><span data-stu-id="5fa36-110">Square</span></span>  <br/> |
|<span data-ttu-id="5fa36-111">2</span><span class="sxs-lookup"><span data-stu-id="5fa36-111">2</span></span>  <br/> |<span data-ttu-id="5fa36-112">Долго</span><span class="sxs-lookup"><span data-stu-id="5fa36-112">Extended</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5fa36-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="5fa36-113">Remarks</span></span>

<span data-ttu-id="5fa36-114">Также можно задать значение данной ячейки в диалоговом окне " **строка** " (на вкладке **Главная** в группе **фигуру** щелкните **строку**, выберите пункт **стрелки**и нажмите кнопку **Дополнительно стрелки**).</span><span class="sxs-lookup"><span data-stu-id="5fa36-114">You can also set the value of this cell in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span>
  
<span data-ttu-id="5fa36-115">Чтобы получить ссылку на ячейку LineCap по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5fa36-115">To get a reference to the LineCap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5fa36-116">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="5fa36-116">Cell name:</span></span>  <br/> |<span data-ttu-id="5fa36-117">LineCap</span><span class="sxs-lookup"><span data-stu-id="5fa36-117">LineCap</span></span>  <br/> |
   
<span data-ttu-id="5fa36-118">Для получения ссылки на ячейки LineCap по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="5fa36-118">To get a reference to the LineCap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5fa36-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5fa36-119">Section index:</span></span>  <br/> |<span data-ttu-id="5fa36-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5fa36-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5fa36-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5fa36-121">Row index:</span></span>  <br/> |<span data-ttu-id="5fa36-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="5fa36-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="5fa36-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5fa36-123">Cell index:</span></span>  <br/> |<span data-ttu-id="5fa36-124">**visLineEndCap**</span><span class="sxs-lookup"><span data-stu-id="5fa36-124">**visLineEndCap**</span></span> <br/> |
   

