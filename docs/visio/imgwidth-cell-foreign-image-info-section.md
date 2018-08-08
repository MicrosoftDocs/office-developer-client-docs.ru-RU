---
title: Ячейка ImgWidth (раздел "Сведения о внешнем изображении")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm460
localization_priority: Normal
ms.assetid: b57fb962-0b3e-f2e5-3b88-3edf33e40496
description: 'Определяет ширину изображения объекта в рамках его границ. Формула по умолчанию имеет вид:'
ms.openlocfilehash: 3aab65d27d426287060f7572dad15174acb93199
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813949"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a><span data-ttu-id="6b2d6-104">Ячейка ImgWidth (раздел "Сведения о внешнем изображении")</span><span class="sxs-lookup"><span data-stu-id="6b2d6-104">ImgWidth Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="6b2d6-105">Определяет ширину изображения объекта в рамках его границ.</span><span class="sxs-lookup"><span data-stu-id="6b2d6-105">Determines the width of the object's image within its border.</span></span> <span data-ttu-id="6b2d6-106">Формула по умолчанию имеет вид:</span><span class="sxs-lookup"><span data-stu-id="6b2d6-106">The default formula is:</span></span>
  
<span data-ttu-id="6b2d6-107">= Ширина \* 1</span><span class="sxs-lookup"><span data-stu-id="6b2d6-107">= Width \* 1</span></span>
  
<span data-ttu-id="6b2d6-108">Обрезка объекта изменяется коэффициент, на который умножается ширина.</span><span class="sxs-lookup"><span data-stu-id="6b2d6-108">Cropping the object changes the factor by which Width is multiplied.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6b2d6-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="6b2d6-109">Remarks</span></span>

<span data-ttu-id="6b2d6-110">Чтобы получить ссылку на ячейку ImgWidth по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6b2d6-110">To get a reference to the ImgWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6b2d6-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="6b2d6-111">Cell name:</span></span>  <br/> | <span data-ttu-id="6b2d6-112">ImgWidth</span><span class="sxs-lookup"><span data-stu-id="6b2d6-112">ImgWidth</span></span>  <br/> |
   
<span data-ttu-id="6b2d6-113">Для получения ссылки на ячейки ImgWidth по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="6b2d6-113">To get a reference to the ImgWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6b2d6-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6b2d6-114">Section index:</span></span>  <br/> |<span data-ttu-id="6b2d6-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6b2d6-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6b2d6-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6b2d6-116">Row index:</span></span>  <br/> |<span data-ttu-id="6b2d6-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="6b2d6-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="6b2d6-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6b2d6-118">Cell index:</span></span>  <br/> |<span data-ttu-id="6b2d6-119">**visFrgnImgWidth**</span><span class="sxs-lookup"><span data-stu-id="6b2d6-119">**visFrgnImgWidth**</span></span> <br/> |
   

