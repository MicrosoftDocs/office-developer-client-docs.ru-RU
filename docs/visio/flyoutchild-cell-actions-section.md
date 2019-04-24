---
title: FlyoutChild Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80003
localization_priority: Normal
ms.assetid: b2405457-843c-0d46-5f4f-9c413826c3f1
description: Определяет, является ли строка дочерним всплывающим меню последней строки над ним, которое не является потомком всплывающего списка.
ms.openlocfilehash: 85524ea33258449f5c9ee0991ac9a64f8f0eebae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346153"
---
# <a name="flyoutchild-cell-actions-section"></a><span data-ttu-id="30e17-103">FlyoutChild Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="30e17-103">FlyoutChild Cell (Actions Section)</span></span>

<span data-ttu-id="30e17-104">Определяет, является ли строка дочерним всплывающим меню последней строки над ним, которое не является потомком всплывающего списка.</span><span class="sxs-lookup"><span data-stu-id="30e17-104">Determines whether the row is a child flyout menu of the last row above it that is not a flyout child.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="30e17-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30e17-105">Remarks</span></span>

<span data-ttu-id="30e17-106">Чтобы получить ссылку на ячейку FlyoutChild по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="30e17-106">To get a reference to the FlyoutChild cell by name from another formula, or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30e17-107">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="30e17-107">Cell name:</span></span>  <br/> |<span data-ttu-id="30e17-108">Действия.</span><span class="sxs-lookup"><span data-stu-id="30e17-108">Actions.</span></span> <span data-ttu-id="30e17-109">*Name (имя* ). Действия Флйоутчилдвхере.</span><span class="sxs-lookup"><span data-stu-id="30e17-109">*name*  .FlyoutChildwhere Actions.</span></span>  <span data-ttu-id="30e17-110">*Name* — имя строки действий</span><span class="sxs-lookup"><span data-stu-id="30e17-110">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="30e17-111">Чтобы получить ссылку на ячейку FlyoutChild по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="30e17-111">To get a reference to the FlyoutChild cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30e17-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="30e17-112">Section index:</span></span>  <br/> |<span data-ttu-id="30e17-113">**Виссектионактион**</span><span class="sxs-lookup"><span data-stu-id="30e17-113">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="30e17-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="30e17-114">Row index:</span></span>  <br/> |<span data-ttu-id="30e17-115">**висровактион** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="30e17-115">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="30e17-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="30e17-116">Cell index:</span></span>  <br/> |<span data-ttu-id="30e17-117">**Висактионфлйоутчилд**</span><span class="sxs-lookup"><span data-stu-id="30e17-117">**visActionFlyoutChild**</span></span> <br/> |
   

