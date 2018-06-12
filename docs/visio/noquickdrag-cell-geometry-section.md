---
title: Ячейка NoQuickDrag (раздел геометрии)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
localization_priority: Normal
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: Определяет, установлен или перетащить при нажатии кнопки Заполненная область, определенные в раздел геометрии фигуры.
ms.openlocfilehash: 7d4ffd876d8676af885b8f750fecf6f6d0deaa9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814309"
---
# <a name="noquickdrag-cell-geometry-section"></a><span data-ttu-id="0777c-103">Ячейка NoQuickDrag (раздел геометрии)</span><span class="sxs-lookup"><span data-stu-id="0777c-103">NoQuickDrag Cell (Geometry Section)</span></span>

<span data-ttu-id="0777c-104">Определяет, установлен или перетащить при нажатии кнопки Заполненная область, определенные в раздел геометрии фигуры.</span><span class="sxs-lookup"><span data-stu-id="0777c-104">Determines whether a shape can be selected or dragged when the user clicks the filled area defined by the Geometry section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0777c-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="0777c-105">Remarks</span></span>

<span data-ttu-id="0777c-106">Чтобы получить ссылку на ячейку NoQuickDrag по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="0777c-106">To get a reference to the NoQuickDrag cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0777c-107">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="0777c-107">Cell name:</span></span>  <br/> |<span data-ttu-id="0777c-108">Геометрия *i* . NoQuickDrag, где * я * - < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0777c-108">Geometry  *i*  .NoQuickDrag, where  * i *  - <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0777c-109">Для получения ссылки на ячейки NoQuickDrag по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="0777c-109">To get a reference to the NoQuickDrag cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0777c-110">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0777c-110">Section index:</span></span>  <br/> |<span data-ttu-id="0777c-111">**visSectionFirstComponent** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0777c-111">**visSectionFirstComponent** +  *i*  , where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="0777c-112">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0777c-112">Row index:</span></span>  <br/> |<span data-ttu-id="0777c-113">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="0777c-113">**visRowComponent**</span></span> <br/> |
|<span data-ttu-id="0777c-114">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0777c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="0777c-115">**visCompNoQuickDrag**</span><span class="sxs-lookup"><span data-stu-id="0777c-115">**visCompNoQuickDrag**</span></span> <br/> |
   

