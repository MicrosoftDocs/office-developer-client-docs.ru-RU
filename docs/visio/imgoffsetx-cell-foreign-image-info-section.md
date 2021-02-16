---
title: ImgOffsetX Cell (Foreign Image Info Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251308
localization_priority: Normal
ms.assetid: c079fb10-4db7-4657-75d2-2fb953c86670
description: Определяет расстояние, на которое объект смещен по горизонтали от начала границы объекта. По умолчанию используется значение 0. Панорамирование объекта с помощью средства crop изменяет это значение.
ms.openlocfilehash: d9b3e97a07bc1cadc0276905c4199861ab0590ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405235"
---
# <a name="imgoffsetx-cell-foreign-image-info-section"></a><span data-ttu-id="54352-105">ImgOffsetX Cell (Foreign Image Info Section)</span><span class="sxs-lookup"><span data-stu-id="54352-105">ImgOffsetX Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="54352-106">Определяет расстояние, на которое объект смещен по горизонтали от начала границы объекта.</span><span class="sxs-lookup"><span data-stu-id="54352-106">Determines the distance the object is offset horizontally from the origin of the object's border.</span></span> <span data-ttu-id="54352-107">По умолчанию используется значение 0.</span><span class="sxs-lookup"><span data-stu-id="54352-107">The default is 0.</span></span> <span data-ttu-id="54352-108">Панорамирование объекта с помощью средства **crop** изменяет это значение.</span><span class="sxs-lookup"><span data-stu-id="54352-108">Panning the object with the **Crop** tool changes this value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="54352-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="54352-109">Remarks</span></span>

<span data-ttu-id="54352-110">Чтобы получить ссылку на ячейку ImgOffsetX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="54352-110">To get a reference to the ImgOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54352-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="54352-111">Cell name:</span></span>  <br/> | <span data-ttu-id="54352-112">ImgOffsetX</span><span class="sxs-lookup"><span data-stu-id="54352-112">ImgOffsetX</span></span>  <br/> |
   
<span data-ttu-id="54352-113">Чтобы получить ссылку на ячейку ImgOffsetX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="54352-113">To get a reference to the ImgOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54352-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="54352-114">Section index:</span></span>  <br/> |<span data-ttu-id="54352-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="54352-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="54352-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="54352-116">Row index:</span></span>  <br/> |<span data-ttu-id="54352-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="54352-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="54352-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="54352-118">Cell index:</span></span>  <br/> |<span data-ttu-id="54352-119">**visFrgnImgOffsetX**</span><span class="sxs-lookup"><span data-stu-id="54352-119">**visFrgnImgOffsetX**</span></span> <br/> |
   

