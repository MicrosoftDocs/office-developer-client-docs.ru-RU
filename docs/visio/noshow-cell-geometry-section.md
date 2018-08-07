---
title: Ячейка NoShow (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
localization_priority: Normal
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: Указывает, отображается ли путь на странице документа.
ms.openlocfilehash: ad4d9cf1aa3e541f512bc09ffc38cf03204b3c94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814334"
---
# <a name="noshow-cell-geometry-section"></a><span data-ttu-id="932a6-103">Ячейка NoShow (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="932a6-103">NoShow Cell (Geometry Section)</span></span>

<span data-ttu-id="932a6-104">Указывает, отображается ли путь на странице документа.</span><span class="sxs-lookup"><span data-stu-id="932a6-104">Indicates whether a path is displayed on the drawing page.</span></span>
  
|<span data-ttu-id="932a6-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="932a6-105">**Value**</span></span>|<span data-ttu-id="932a6-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="932a6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="932a6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="932a6-107">TRUE</span></span>  <br/> | <span data-ttu-id="932a6-108">Числу штрихов и заливки пути, представленный в разделе является скрытым.</span><span class="sxs-lookup"><span data-stu-id="932a6-108">The stroke and fill of the path represented by the section is hidden.</span></span>  <br/> |
| <span data-ttu-id="932a6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="932a6-109">FALSE</span></span>  <br/> | <span data-ttu-id="932a6-110">Показана числу штрихов и заливки пути.</span><span class="sxs-lookup"><span data-stu-id="932a6-110">The stroke and fill of the path is shown.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="932a6-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="932a6-111">Remarks</span></span>

<span data-ttu-id="932a6-112">Чтобы получить ссылку на ячейку NoShow по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="932a6-112">To get a reference to the NoShow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="932a6-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="932a6-113">Cell name:</span></span>  <br/> | <span data-ttu-id="932a6-114">Геометрия *i* . NoShow где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="932a6-114">Geometry  *i*  .NoShow            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="932a6-115">Для получения ссылки на ячейки NoShow по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="932a6-115">To get a reference to the NoShow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="932a6-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="932a6-116">Section index:</span></span>  <br/> |<span data-ttu-id="932a6-117">**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="932a6-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="932a6-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="932a6-118">Row index:</span></span>  <br/> |<span data-ttu-id="932a6-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="932a6-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="932a6-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="932a6-120">Cell index:</span></span>  <br/> |<span data-ttu-id="932a6-121">**visCompNoShow**</span><span class="sxs-lookup"><span data-stu-id="932a6-121">**visCompNoShow**</span></span> <br/> |
   

