---
title: Rounding Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm860
localization_priority: Normal
ms.assetid: c44457ca-997a-5315-44dd-4218e4203550
description: Указывает радиус закругления округления, который применяется, когда два непрерывных сегмента сопоставлены с контуром. Например, округление можно использовать для предоставления закругленных углов прямоугольника. Чтобы задать округление, введите значение с единицами измерения (числом, состоящий из единицы измерения).
ms.openlocfilehash: d64d3266e3dd2b0a3998955efe271aab04905fbf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427012"
---
# <a name="rounding-cell-line-format-section"></a><span data-ttu-id="0428d-105">Rounding Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="0428d-105">Rounding Cell (Line Format Section)</span></span>

<span data-ttu-id="0428d-106">Указывает радиус закругления округления, который применяется, когда два непрерывных сегмента сопоставлены с контуром.</span><span class="sxs-lookup"><span data-stu-id="0428d-106">Indicates the radius of the rounding arc applied where two contiguous segments of a path meet.</span></span> <span data-ttu-id="0428d-107">Например, округление можно использовать для предоставления закругленных углов прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="0428d-107">For example, rounding can be used to give a rectangle rounded corners.</span></span> <span data-ttu-id="0428d-108">Чтобы задать округление, введите значение с единицами измерения (числом, состоящий из единицы измерения).</span><span class="sxs-lookup"><span data-stu-id="0428d-108">To set rounding, enter a value with units of measure (a number-unit pair).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0428d-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="0428d-109">Remarks</span></span>

<span data-ttu-id="0428d-110">Вы также можете задать это значение в диалоговом окне **строка** (на вкладке **Главная** , в группе **фигура** , выберите пункт **линия**, затем выберите **вес**, а затем щелкните **дополнительные линии**).</span><span class="sxs-lookup"><span data-stu-id="0428d-110">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="0428d-111">Чтобы получить ссылку на ячейку округления по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="0428d-111">To get a reference to the Rounding cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0428d-112">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="0428d-112">Cell name:</span></span>  <br/> |<span data-ttu-id="0428d-113">Rounding</span><span class="sxs-lookup"><span data-stu-id="0428d-113">Rounding</span></span>  <br/> |
   
<span data-ttu-id="0428d-114">Чтобы получить ссылку на ячейку округления по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="0428d-114">To get a reference to the Rounding cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0428d-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0428d-115">Section index:</span></span>  <br/> |<span data-ttu-id="0428d-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0428d-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0428d-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0428d-117">Row index:</span></span>  <br/> |<span data-ttu-id="0428d-118">**Висровлине**</span><span class="sxs-lookup"><span data-stu-id="0428d-118">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="0428d-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0428d-119">Cell index:</span></span>  <br/> |<span data-ttu-id="0428d-120">**Вислинераундинг**</span><span class="sxs-lookup"><span data-stu-id="0428d-120">**visLineRounding**</span></span> <br/> |
   

