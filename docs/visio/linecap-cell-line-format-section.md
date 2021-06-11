---
title: LineCap Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251231
localization_priority: Normal
ms.assetid: 3519216b-b6cf-2e8c-e20f-adfa373c9028
description: Указывает, закруглили ли строки, квадрат или расширенные ограничения строки.
ms.openlocfilehash: 44de4bff87fd3d121dfce9eec934ec39bc61065a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425201"
---
# <a name="linecap-cell-line-format-section"></a><span data-ttu-id="21b09-103">LineCap Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="21b09-103">LineCap Cell (Line Format Section)</span></span>

<span data-ttu-id="21b09-104">Указывает, закруглили ли строки, квадрат или расширенные ограничения строки.</span><span class="sxs-lookup"><span data-stu-id="21b09-104">Indicates whether a line has rounded, square, or extended line caps.</span></span>
  
|<span data-ttu-id="21b09-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="21b09-105">**Value**</span></span>|<span data-ttu-id="21b09-106">**Стиль конца строки**</span><span class="sxs-lookup"><span data-stu-id="21b09-106">**Line end style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="21b09-107">0</span><span class="sxs-lookup"><span data-stu-id="21b09-107">0</span></span>  <br/> |<span data-ttu-id="21b09-108">Округлый</span><span class="sxs-lookup"><span data-stu-id="21b09-108">Rounded</span></span>  <br/> |
|<span data-ttu-id="21b09-109">1</span><span class="sxs-lookup"><span data-stu-id="21b09-109">1</span></span>  <br/> |<span data-ttu-id="21b09-110">Square</span><span class="sxs-lookup"><span data-stu-id="21b09-110">Square</span></span>  <br/> |
|<span data-ttu-id="21b09-111">2</span><span class="sxs-lookup"><span data-stu-id="21b09-111">2</span></span>  <br/> |<span data-ttu-id="21b09-112">Долго</span><span class="sxs-lookup"><span data-stu-id="21b09-112">Extended</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21b09-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="21b09-113">Remarks</span></span>

<span data-ttu-id="21b09-114">Вы также можете установить значение этой ячейки в диалоговом окне **Line** (на вкладке Главная, в группе **Shape** щелкните Строка, указать стрелки, а затем нажмите кнопку **Дополнительные стрелки).**   </span><span class="sxs-lookup"><span data-stu-id="21b09-114">You can also set the value of this cell in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span>
  
<span data-ttu-id="21b09-115">Чтобы получить ссылку на ячейку LineCap по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="21b09-115">To get a reference to the LineCap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="21b09-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="21b09-116">Cell name:</span></span>  <br/> |<span data-ttu-id="21b09-117">LineCap</span><span class="sxs-lookup"><span data-stu-id="21b09-117">LineCap</span></span>  <br/> |
   
<span data-ttu-id="21b09-118">Чтобы получить ссылку на ячейку LineCap по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="21b09-118">To get a reference to the LineCap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="21b09-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="21b09-119">Section index:</span></span>  <br/> |<span data-ttu-id="21b09-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="21b09-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="21b09-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="21b09-121">Row index:</span></span>  <br/> |<span data-ttu-id="21b09-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="21b09-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="21b09-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="21b09-123">Cell index:</span></span>  <br/> |<span data-ttu-id="21b09-124">**visLineEndCap**</span><span class="sxs-lookup"><span data-stu-id="21b09-124">**visLineEndCap**</span></span> <br/> |
   

