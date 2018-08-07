---
title: Ячейка EndArrow (раздел "Формат линий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm320
localization_priority: Normal
ms.assetid: 2f9c11ba-a316-bc34-60d4-0a41b2af486f
description: Указывает, будет ли линия стрелки или другого плана формата в последней вершине.
ms.openlocfilehash: fa37e4896fdab0f2e8fee6d94aa38c72519a7e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813684"
---
# <a name="endarrow-cell-line-format-section"></a><span data-ttu-id="c93e1-103">Ячейка EndArrow (раздел "Формат линий")</span><span class="sxs-lookup"><span data-stu-id="c93e1-103">EndArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="c93e1-104">Указывает, будет ли линия стрелки или другого плана формата в последней вершине.</span><span class="sxs-lookup"><span data-stu-id="c93e1-104">Indicates whether a line has an arrowhead or other line end format at its last vertex.</span></span>
  
|<span data-ttu-id="c93e1-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c93e1-105">**Value**</span></span>|<span data-ttu-id="c93e1-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c93e1-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c93e1-107">0</span><span class="sxs-lookup"><span data-stu-id="c93e1-107">0</span></span>  <br/> |<span data-ttu-id="c93e1-108">Не стрелки.</span><span class="sxs-lookup"><span data-stu-id="c93e1-108">No arrowhead.</span></span>  <br/> |
|<span data-ttu-id="c93e1-109">1 - 45</span><span class="sxs-lookup"><span data-stu-id="c93e1-109">1 - 45</span></span>  <br/> |<span data-ttu-id="c93e1-110">Различные стрелки стили, которые соответствуют индексирование записей в диалоговом окне " **строка** ".</span><span class="sxs-lookup"><span data-stu-id="c93e1-110">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c93e1-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="c93e1-111">Remarks</span></span>

<span data-ttu-id="c93e1-112">Также можно задать это значение в поле **строка** (на вкладке **Главная** в группе **фигуру** щелкните **строку**, выберите пункт **стрелки**и нажмите кнопку **Дополнительно стрелки**).</span><span class="sxs-lookup"><span data-stu-id="c93e1-112">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span> <span data-ttu-id="c93e1-113">Размер стрелки имеет значение в ячейке EndArrowSize.</span><span class="sxs-lookup"><span data-stu-id="c93e1-113">The size of the arrowhead is set in the EndArrowSize cell.</span></span>
  
<span data-ttu-id="c93e1-114">Можно указать конец настраиваемой строки, с помощью функции используется в этой ячейке.</span><span class="sxs-lookup"><span data-stu-id="c93e1-114">You can specify a custom line end using the USE function in this cell.</span></span> 
  
<span data-ttu-id="c93e1-115">Чтобы получить ссылку на ячейку EndArrow по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="c93e1-115">To get a reference to the EndArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c93e1-116">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="c93e1-116">Cell name:</span></span>  <br/> |<span data-ttu-id="c93e1-117">EndArrow</span><span class="sxs-lookup"><span data-stu-id="c93e1-117">EndArrow</span></span>  <br/> |
   
<span data-ttu-id="c93e1-118">Для получения ссылки на ячейки EndArrow по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="c93e1-118">To get a reference to the EndArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c93e1-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c93e1-119">Section index:</span></span>  <br/> |<span data-ttu-id="c93e1-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c93e1-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c93e1-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c93e1-121">Row index:</span></span>  <br/> |<span data-ttu-id="c93e1-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="c93e1-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="c93e1-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c93e1-123">Cell index:</span></span>  <br/> |<span data-ttu-id="c93e1-124">**visLineEndArrow**</span><span class="sxs-lookup"><span data-stu-id="c93e1-124">**visLineEndArrow**</span></span> <br/> |
   

