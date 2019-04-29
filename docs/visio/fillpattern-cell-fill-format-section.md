---
title: FillPattern Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm375
localization_priority: Normal
ms.assetid: dac82a4f-4508-541a-e118-7d79df987232
description: Определяет узор заливки для фигуры. Чтобы указать настраиваемый узор заливки, используйте функцию USE в этой ячейке.
ms.openlocfilehash: 340ccdc9f3819fb29e210832107e270bd302433c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422931"
---
# <a name="fillpattern-cell-fill-format-section"></a><span data-ttu-id="fc4aa-104">FillPattern Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="fc4aa-104">FillPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="fc4aa-105">Определяет узор заливки для фигуры.</span><span class="sxs-lookup"><span data-stu-id="fc4aa-105">Determines the fill pattern for the shape.</span></span> <span data-ttu-id="fc4aa-106">Чтобы указать настраиваемый узор заливки, используйте функцию USE в этой ячейке.</span><span class="sxs-lookup"><span data-stu-id="fc4aa-106">To specify a custom fill pattern, use the USE function in this cell.</span></span>
  
|<span data-ttu-id="fc4aa-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="fc4aa-107">**Value**</span></span>|<span data-ttu-id="fc4aa-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fc4aa-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fc4aa-109">нуль</span><span class="sxs-lookup"><span data-stu-id="fc4aa-109">0</span></span>  <br/> |<span data-ttu-id="fc4aa-110">Нет (прозрачная заливка).</span><span class="sxs-lookup"><span data-stu-id="fc4aa-110">None (transparent fill).</span></span>  <br/> |
|<span data-ttu-id="fc4aa-111">1,1</span><span class="sxs-lookup"><span data-stu-id="fc4aa-111">1</span></span>  <br/> |<span data-ttu-id="fc4aa-112">Сплошной цвет переднего плана.</span><span class="sxs-lookup"><span data-stu-id="fc4aa-112">Solid foreground color.</span></span>  <br/> |
|<span data-ttu-id="fc4aa-113">2-40</span><span class="sxs-lookup"><span data-stu-id="fc4aa-113">2 - 40</span></span>  <br/> |<span data-ttu-id="fc4aa-114">Шаблоны заливки, которые соответствуют индексированным записям в диалоговом окне **Fill** (Заливка).</span><span class="sxs-lookup"><span data-stu-id="fc4aa-114">Assorted fill patterns that correspond to indexed entries in the **Fill** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc4aa-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="fc4aa-115">Remarks</span></span>

<span data-ttu-id="fc4aa-116">Вы также можете задать это значение с помощью \*\*\*\* диалогового окна "Заливка" (на вкладке **Главная** , в группе **фигур** нажмите кнопку **Заливка** и выберите пункт **Параметры заливки**).</span><span class="sxs-lookup"><span data-stu-id="fc4aa-116">You can also set this value using the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill** and then click **Fill Options**).</span></span>
  
<span data-ttu-id="fc4aa-117">Чтобы получить ссылку на ячейку FillPattern по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="fc4aa-117">To get a reference to the FillPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc4aa-118">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="fc4aa-118">Cell name:</span></span>  <br/> |<span data-ttu-id="fc4aa-119">FillPattern</span><span class="sxs-lookup"><span data-stu-id="fc4aa-119">FillPattern</span></span>  <br/> |
   
<span data-ttu-id="fc4aa-120">Чтобы получить ссылку на ячейку FillPattern по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="fc4aa-120">To get a reference to the FillPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc4aa-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fc4aa-121">Section index:</span></span>  <br/> |<span data-ttu-id="fc4aa-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fc4aa-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fc4aa-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fc4aa-123">Row index:</span></span>  <br/> |<span data-ttu-id="fc4aa-124">**Висровфилл**</span><span class="sxs-lookup"><span data-stu-id="fc4aa-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="fc4aa-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fc4aa-125">Cell index:</span></span>  <br/> |<span data-ttu-id="fc4aa-126">**Висфиллпаттерн**</span><span class="sxs-lookup"><span data-stu-id="fc4aa-126">**visFillPattern**</span></span> <br/> |
   

