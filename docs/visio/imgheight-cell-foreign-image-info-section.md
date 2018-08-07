---
title: Ячейка ImgHeight (раздел "Сведения о внешнем изображении")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
localization_priority: Normal
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: 'Определяет высоту изображения объекта в рамках его границ. Формула по умолчанию имеет вид:'
ms.openlocfilehash: 983bb919dbfada65b6d9af464ecfa17c04e970c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813951"
---
# <a name="imgheight-cell-foreign-image-info-section"></a><span data-ttu-id="8f28f-104">Ячейка ImgHeight (раздел "Сведения о внешнем изображении")</span><span class="sxs-lookup"><span data-stu-id="8f28f-104">ImgHeight Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="8f28f-105">Определяет высоту изображения объекта в рамках его границ.</span><span class="sxs-lookup"><span data-stu-id="8f28f-105">Determines the height of the object's image within its border.</span></span> <span data-ttu-id="8f28f-106">Формула по умолчанию имеет вид:</span><span class="sxs-lookup"><span data-stu-id="8f28f-106">The default formula is:</span></span>
  
<span data-ttu-id="8f28f-107">= Высота \* 1</span><span class="sxs-lookup"><span data-stu-id="8f28f-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8f28f-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="8f28f-108">Remarks</span></span>

<span data-ttu-id="8f28f-109">Чтобы получить ссылку на ячейку ImgHeight по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="8f28f-109">To get a reference to the ImgHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8f28f-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="8f28f-110">Cell name:</span></span>  <br/> | <span data-ttu-id="8f28f-111">ImgHeight</span><span class="sxs-lookup"><span data-stu-id="8f28f-111">ImgHeight</span></span>  <br/> |
   
<span data-ttu-id="8f28f-112">Для получения ссылки на ячейки ImgHeight по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="8f28f-112">To get a reference to the ImgHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8f28f-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8f28f-113">Section index:</span></span>  <br/> |<span data-ttu-id="8f28f-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8f28f-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8f28f-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8f28f-115">Row index:</span></span>  <br/> |<span data-ttu-id="8f28f-116">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="8f28f-116">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="8f28f-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8f28f-117">Cell index:</span></span>  <br/> |<span data-ttu-id="8f28f-118">**visFrgnImgHeight**</span><span class="sxs-lookup"><span data-stu-id="8f28f-118">**visFrgnImgHeight**</span></span> <br/> |
   

