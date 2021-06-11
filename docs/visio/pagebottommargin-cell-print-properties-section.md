---
title: PageBottomMargin Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60060
localization_priority: Normal
ms.assetid: 7a97e97c-278d-2e1e-6c4f-f5f32e2cdeb0
description: Указывает поле в нижней части печатной страницы.
ms.openlocfilehash: f546d89b8761c6c1b7340af69d2b48f16c180767
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438598"
---
# <a name="pagebottommargin-cell-print-properties-section"></a><span data-ttu-id="f7660-103">PageBottomMargin Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="f7660-103">PageBottomMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="f7660-104">Указывает поле в нижней части печатной страницы.</span><span class="sxs-lookup"><span data-stu-id="f7660-104">Specifies the margin at the bottom of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f7660-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="f7660-105">Remarks</span></span>

<span data-ttu-id="f7660-106">Это значение представляет физические единицы и не влияет на единицы масштабирования или рисования.</span><span class="sxs-lookup"><span data-stu-id="f7660-106">This value represents physical units and is unaffected by scale or drawing units.</span></span> <span data-ttu-id="f7660-107">Например, если эта ячейка имеет значение 0,5 дюйма, эта маржа составляет 0,5 дюйма, даже если блоки страниц являются ногами.</span><span class="sxs-lookup"><span data-stu-id="f7660-107">For example, if this cell has a value of 0.5 in., this margin is 0.5 inch even if page units are feet.</span></span> <span data-ttu-id="f7660-108">Если единицы явно не заявлены, это значение по умолчанию передается на страницы.</span><span class="sxs-lookup"><span data-stu-id="f7660-108">If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="f7660-109">Чтобы получить ссылку на ячейку PageBottomMargin по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="f7660-109">To get a reference to the PageBottomMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f7660-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f7660-110">Cell name:</span></span>  <br/> | <span data-ttu-id="f7660-111">PageBottomMargin</span><span class="sxs-lookup"><span data-stu-id="f7660-111">PageBottomMargin</span></span>  <br/> |
   
<span data-ttu-id="f7660-112">Чтобы получить ссылку на ячейку PageBottomMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f7660-112">To get a reference to the PageBottomMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f7660-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f7660-113">Section index:</span></span>  <br/> |<span data-ttu-id="f7660-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f7660-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f7660-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f7660-115">Row index:</span></span>  <br/> |<span data-ttu-id="f7660-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="f7660-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="f7660-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f7660-117">Cell index:</span></span>  <br/> |<span data-ttu-id="f7660-118">**visPrintPropertiesBottomMargin**</span><span class="sxs-lookup"><span data-stu-id="f7660-118">**visPrintPropertiesBottomMargin**</span></span> <br/> |
   

