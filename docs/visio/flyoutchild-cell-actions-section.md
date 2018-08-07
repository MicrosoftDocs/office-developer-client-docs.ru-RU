---
title: Ячейка FlyoutChild (раздел "Действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80003
localization_priority: Normal
ms.assetid: b2405457-843c-0d46-5f4f-9c413826c3f1
description: Определяет, является ли строку всплывающего меню дочерние последней строки над текстом, который не является дочерним всплывающее меню.
ms.openlocfilehash: 8a41721f91fa9632246e512cfd4ba1a2d871ece5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813784"
---
# <a name="flyoutchild-cell-actions-section"></a><span data-ttu-id="59c88-103">Ячейка FlyoutChild (раздел "Действия")</span><span class="sxs-lookup"><span data-stu-id="59c88-103">FlyoutChild Cell (Actions Section)</span></span>

<span data-ttu-id="59c88-104">Определяет, является ли строку всплывающего меню дочерние последней строки над текстом, который не является дочерним всплывающее меню.</span><span class="sxs-lookup"><span data-stu-id="59c88-104">Determines whether the row is a child flyout menu of the last row above it that is not a flyout child.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="59c88-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="59c88-105">Remarks</span></span>

<span data-ttu-id="59c88-106">Для получения ссылки на ячейку с параметром FlyoutChild по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте следующее.</span><span class="sxs-lookup"><span data-stu-id="59c88-106">To get a reference to the FlyoutChild cell by name from another formula, or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59c88-107">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="59c88-107">Cell name:</span></span>  <br/> |<span data-ttu-id="59c88-108">Действия.</span><span class="sxs-lookup"><span data-stu-id="59c88-108">Actions.</span></span> <span data-ttu-id="59c88-109">*имя* . FlyoutChildwhere действия.</span><span class="sxs-lookup"><span data-stu-id="59c88-109">*name*  .FlyoutChildwhere Actions.</span></span>  <span data-ttu-id="59c88-110">*имя* — это имя строки действий</span><span class="sxs-lookup"><span data-stu-id="59c88-110">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="59c88-111">Для получения ссылки на ячейки с параметром FlyoutChild по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="59c88-111">To get a reference to the FlyoutChild cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59c88-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="59c88-112">Section index:</span></span>  <br/> |<span data-ttu-id="59c88-113">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="59c88-113">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="59c88-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="59c88-114">Row index:</span></span>  <br/> |<span data-ttu-id="59c88-115">**visRowAction** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="59c88-115">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="59c88-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="59c88-116">Cell index:</span></span>  <br/> |<span data-ttu-id="59c88-117">**visActionFlyoutChild**</span><span class="sxs-lookup"><span data-stu-id="59c88-117">**visActionFlyoutChild**</span></span> <br/> |
   

