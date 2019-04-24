---
title: PageTopMargin Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033785
localization_priority: Normal
ms.assetid: 2ba0fd22-65a6-6cb6-da00-08f391705544
description: Задает поле в верхней части страницы принтера.
ms.openlocfilehash: ff2bffffed39c5571386e792d2ffc8d20d6b291e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327365"
---
# <a name="pagetopmargin-cell-print-properties-section"></a><span data-ttu-id="459d4-103">PageTopMargin Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="459d4-103">PageTopMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="459d4-104">Задает поле в верхней части страницы принтера.</span><span class="sxs-lookup"><span data-stu-id="459d4-104">Specifies the margin at the top of the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="459d4-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="459d4-105">Remarks</span></span>

<span data-ttu-id="459d4-106">Это значение представляет физические единицы и не затронет единицы масштабирования или рисования.</span><span class="sxs-lookup"><span data-stu-id="459d4-106">This value represents physical units and is unaffected by scale or drawing units.</span></span> <span data-ttu-id="459d4-107">Например, если ячейка имеет значение 0,25 в., это поле составляет 0,25 дюйма, даже если единицы страницы — футы.</span><span class="sxs-lookup"><span data-stu-id="459d4-107">For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet.</span></span> <span data-ttu-id="459d4-108">Если единицы измерения не заданы явным образом, значение по умолчанию равно единицам страницы.</span><span class="sxs-lookup"><span data-stu-id="459d4-108">If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="459d4-109">Чтобы получить ссылку на ячейку PageTopMargin по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="459d4-109">To get a reference to the PageTopMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="459d4-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="459d4-110">Cell name:</span></span>  <br/> | <span data-ttu-id="459d4-111">PageTopMargin</span><span class="sxs-lookup"><span data-stu-id="459d4-111">PageTopMargin</span></span>  <br/> |
   
<span data-ttu-id="459d4-112">Чтобы получить ссылку на ячейку PageTopMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="459d4-112">To get a reference to the PageTopMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="459d4-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="459d4-113">Section index:</span></span>  <br/> |<span data-ttu-id="459d4-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="459d4-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="459d4-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="459d4-115">Row index:</span></span>  <br/> |<span data-ttu-id="459d4-116">**Висровпринтпропертиес**</span><span class="sxs-lookup"><span data-stu-id="459d4-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="459d4-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="459d4-117">Cell index:</span></span>  <br/> |<span data-ttu-id="459d4-118">**Виспринтпропертиестопмаргин**</span><span class="sxs-lookup"><span data-stu-id="459d4-118">**visPrintPropertiesTopMargin**</span></span> <br/> |
   

