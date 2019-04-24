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
description: Задает поле в нижней части печатной страницы.
ms.openlocfilehash: f546d89b8761c6c1b7340af69d2b48f16c180767
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334414"
---
# <a name="pagebottommargin-cell-print-properties-section"></a><span data-ttu-id="37910-103">PageBottomMargin Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="37910-103">PageBottomMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="37910-104">Задает поле в нижней части печатной страницы.</span><span class="sxs-lookup"><span data-stu-id="37910-104">Specifies the margin at the bottom of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="37910-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37910-105">Remarks</span></span>

<span data-ttu-id="37910-106">Это значение представляет физические единицы и не затронет единицы масштабирования или рисования.</span><span class="sxs-lookup"><span data-stu-id="37910-106">This value represents physical units and is unaffected by scale or drawing units.</span></span> <span data-ttu-id="37910-107">Например, если ячейка имеет значение 0,5 в., это поле составляет 0,5 дюйма, даже если единицы страницы — футы.</span><span class="sxs-lookup"><span data-stu-id="37910-107">For example, if this cell has a value of 0.5 in., this margin is 0.5 inch even if page units are feet.</span></span> <span data-ttu-id="37910-108">Если единицы измерения не заданы явным образом, значение по умолчанию равно единицам страницы.</span><span class="sxs-lookup"><span data-stu-id="37910-108">If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="37910-109">Чтобы получить ссылку на ячейку PageBottomMargin по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="37910-109">To get a reference to the PageBottomMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37910-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="37910-110">Cell name:</span></span>  <br/> | <span data-ttu-id="37910-111">PageBottomMargin</span><span class="sxs-lookup"><span data-stu-id="37910-111">PageBottomMargin</span></span>  <br/> |
   
<span data-ttu-id="37910-112">Чтобы получить ссылку на ячейку PageBottomMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="37910-112">To get a reference to the PageBottomMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37910-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="37910-113">Section index:</span></span>  <br/> |<span data-ttu-id="37910-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="37910-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="37910-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="37910-115">Row index:</span></span>  <br/> |<span data-ttu-id="37910-116">**Висровпринтпропертиес**</span><span class="sxs-lookup"><span data-stu-id="37910-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="37910-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="37910-117">Cell index:</span></span>  <br/> |<span data-ttu-id="37910-118">**Виспринтпропертиесботтоммаргин**</span><span class="sxs-lookup"><span data-stu-id="37910-118">**visPrintPropertiesBottomMargin**</span></span> <br/> |
   

