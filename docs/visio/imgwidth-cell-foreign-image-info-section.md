---
title: ImgWidth Cell (Foreign Image Info Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm460
localization_priority: Normal
ms.assetid: b57fb962-0b3e-f2e5-3b88-3edf33e40496
description: 'Определяет ширину изображения объекта в пределах границы. Формула по умолчанию:'
ms.openlocfilehash: 9da5e06a7fbf6ae77a49fb0410aefb406e2afecb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422833"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a><span data-ttu-id="1f0c6-104">ImgWidth Cell (Foreign Image Info Section)</span><span class="sxs-lookup"><span data-stu-id="1f0c6-104">ImgWidth Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="1f0c6-105">Определяет ширину изображения объекта в пределах границы.</span><span class="sxs-lookup"><span data-stu-id="1f0c6-105">Determines the width of the object's image within its border.</span></span> <span data-ttu-id="1f0c6-106">Формула по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="1f0c6-106">The default formula is:</span></span>
  
<span data-ttu-id="1f0c6-107">= Ширина \* 1</span><span class="sxs-lookup"><span data-stu-id="1f0c6-107">= Width \* 1</span></span>
  
<span data-ttu-id="1f0c6-108">Обрезка объекта изменяет фактор, на который умножается ширина.</span><span class="sxs-lookup"><span data-stu-id="1f0c6-108">Cropping the object changes the factor by which Width is multiplied.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1f0c6-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="1f0c6-109">Remarks</span></span>

<span data-ttu-id="1f0c6-110">Чтобы получить ссылку на ячейку ImgWidth по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="1f0c6-110">To get a reference to the ImgWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1f0c6-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="1f0c6-111">Cell name:</span></span>  <br/> | <span data-ttu-id="1f0c6-112">ImgWidth</span><span class="sxs-lookup"><span data-stu-id="1f0c6-112">ImgWidth</span></span>  <br/> |
   
<span data-ttu-id="1f0c6-113">Чтобы получить ссылку на ячейку ImgWidth по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="1f0c6-113">To get a reference to the ImgWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1f0c6-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="1f0c6-114">Section index:</span></span>  <br/> |<span data-ttu-id="1f0c6-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1f0c6-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1f0c6-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="1f0c6-116">Row index:</span></span>  <br/> |<span data-ttu-id="1f0c6-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="1f0c6-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="1f0c6-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="1f0c6-118">Cell index:</span></span>  <br/> |<span data-ttu-id="1f0c6-119">**visFrgnImgWidth**</span><span class="sxs-lookup"><span data-stu-id="1f0c6-119">**visFrgnImgWidth**</span></span> <br/> |
   

