---
title: Ячейка PinY (раздел "Преобразование фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm795
localization_priority: Normal
ms.assetid: 98b86b9d-9cc0-1169-1c44-ef1505bf92fa
description: Представляет y-координата ПИН-код фигуры (центр вращения) относительно начала родительского элемента.
ms.openlocfilehash: 7002415e813ae63dafb64f416079da2e6b170494
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814367"
---
# <a name="piny-cell-shape-transform-section"></a><span data-ttu-id="d21c7-103">Ячейка PinY (раздел "Преобразование фигуры")</span><span class="sxs-lookup"><span data-stu-id="d21c7-103">PinY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="d21c7-104">Представляет *y* -координата ПИН-код фигуры (центр вращения) относительно начала родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="d21c7-104">Represents the  *y*  -coordinate of the shape's pin (center of rotation) in relation to the origin of its parent.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d21c7-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="d21c7-105">Remarks</span></span>

<span data-ttu-id="d21c7-106">Чтобы получить ссылку на PinY ячейки по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="d21c7-106">To get a reference to the PinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d21c7-107">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="d21c7-107">Cell name:</span></span>  <br/> | <span data-ttu-id="d21c7-108">PinY</span><span class="sxs-lookup"><span data-stu-id="d21c7-108">PinY</span></span>  <br/> |
   
<span data-ttu-id="d21c7-109">Для получения ссылки на ячейки PinY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="d21c7-109">To get a reference to the PinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d21c7-110">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d21c7-110">Section index:</span></span>  <br/> |<span data-ttu-id="d21c7-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d21c7-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d21c7-112">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d21c7-112">Row index:</span></span>  <br/> |<span data-ttu-id="d21c7-113">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="d21c7-113">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="d21c7-114">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d21c7-114">Cell index:</span></span>  <br/> |<span data-ttu-id="d21c7-115">**visXFormPinY**</span><span class="sxs-lookup"><span data-stu-id="d21c7-115">**visXFormPinY**</span></span> <br/> |
   

