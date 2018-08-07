---
title: Ячейка Rounding (раздел "Формат линий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm860
localization_priority: Normal
ms.assetid: c44457ca-997a-5315-44dd-4218e4203550
description: Указывает radius округления дуги которых соответствуют двух смежных сегментов пути. Например округления можно использовать для предоставления прямоугольника скругленные углы. Чтобы установить для округления, введите значение с помощью единиц измерения (пару число единица).
ms.openlocfilehash: 0624ec42978292e84965c978d25e4052fc41613f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814640"
---
# <a name="rounding-cell-line-format-section"></a><span data-ttu-id="dc12d-105">Ячейка Rounding (раздел "Формат линий")</span><span class="sxs-lookup"><span data-stu-id="dc12d-105">Rounding Cell (Line Format Section)</span></span>

<span data-ttu-id="dc12d-106">Указывает radius округления дуги которых соответствуют двух смежных сегментов пути.</span><span class="sxs-lookup"><span data-stu-id="dc12d-106">Indicates the radius of the rounding arc applied where two contiguous segments of a path meet.</span></span> <span data-ttu-id="dc12d-107">Например округления можно использовать для предоставления прямоугольника скругленные углы.</span><span class="sxs-lookup"><span data-stu-id="dc12d-107">For example, rounding can be used to give a rectangle rounded corners.</span></span> <span data-ttu-id="dc12d-108">Чтобы установить для округления, введите значение с помощью единиц измерения (пару число единица).</span><span class="sxs-lookup"><span data-stu-id="dc12d-108">To set rounding, enter a value with units of measure (a number-unit pair).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc12d-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="dc12d-109">Remarks</span></span>

<span data-ttu-id="dc12d-110">Также можно задать это значение в поле **строка** (на вкладке **Главная** в группе **фигуры** щелкните **строку**, выберите пункт **Вес**и нажмите кнопку **Другие линии**).</span><span class="sxs-lookup"><span data-stu-id="dc12d-110">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="dc12d-111">Для получения ссылки на ячейки округление по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="dc12d-111">To get a reference to the Rounding cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc12d-112">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="dc12d-112">Cell name:</span></span>  <br/> |<span data-ttu-id="dc12d-113">Округление</span><span class="sxs-lookup"><span data-stu-id="dc12d-113">Rounding</span></span>  <br/> |
   
<span data-ttu-id="dc12d-114">Для получения ссылки на ячейки округление по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="dc12d-114">To get a reference to the Rounding cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc12d-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="dc12d-115">Section index:</span></span>  <br/> |<span data-ttu-id="dc12d-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dc12d-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="dc12d-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="dc12d-117">Row index:</span></span>  <br/> |<span data-ttu-id="dc12d-118">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="dc12d-118">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="dc12d-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="dc12d-119">Cell index:</span></span>  <br/> |<span data-ttu-id="dc12d-120">**visLineRounding**</span><span class="sxs-lookup"><span data-stu-id="dc12d-120">**visLineRounding**</span></span> <br/> |
   

