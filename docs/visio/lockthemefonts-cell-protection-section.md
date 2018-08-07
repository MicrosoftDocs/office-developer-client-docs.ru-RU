---
title: Ячейка LockThemeFonts (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Запрещает FontIndex ячейку в строке темы свойств изменяются, применение новой темы. Запрещает пользователям изменять это значение в таблице свойств фигуры вручную.
ms.openlocfilehash: b90ffe4c5555df017bb0506a78351514c954ec39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814176"
---
# <a name="lockthemefonts-cell-protection-section"></a><span data-ttu-id="6c6fb-104">Ячейка LockThemeFonts (раздел "Защита")</span><span class="sxs-lookup"><span data-stu-id="6c6fb-104">LockThemeFonts Cell (Protection Section)</span></span>

<span data-ttu-id="6c6fb-105">Запрещает **FontIndex** ячейку в строке **Темы свойств** изменяются, применение новой темы.</span><span class="sxs-lookup"><span data-stu-id="6c6fb-105">Prevents the **FontIndex** cell in the **Theme Properties** row from being altered by applying a new theme.</span></span> <span data-ttu-id="6c6fb-106">Запрещает пользователям изменять это значение в таблице свойств фигуры вручную.</span><span class="sxs-lookup"><span data-stu-id="6c6fb-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="6c6fb-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="6c6fb-107">**Value**</span></span>|<span data-ttu-id="6c6fb-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6c6fb-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6c6fb-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="6c6fb-109">TRUE</span></span>  <br/> |<span data-ttu-id="6c6fb-110">Ячейка **FontIndex** может быть изменен с текущим значением только напрямую изменить в таблице свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="6c6fb-110">The **FontIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="6c6fb-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="6c6fb-111">FALSE</span></span>  <br/> |<span data-ttu-id="6c6fb-112">Ячейка **FontIndex** могут изменяться с текущим значением при изменении темы.</span><span class="sxs-lookup"><span data-stu-id="6c6fb-112">The **FontIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c6fb-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="6c6fb-113">Remarks</span></span>

<span data-ttu-id="6c6fb-114">Для получения ссылки на ячейки **LockThemeFonts** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="6c6fb-114">To get a reference to the **LockThemeFonts** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6c6fb-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="6c6fb-115">Cell name:</span></span>  <br/> | <span data-ttu-id="6c6fb-116">LockThemeFonts</span><span class="sxs-lookup"><span data-stu-id="6c6fb-116">LockThemeFonts</span></span>  <br/> |
   
<span data-ttu-id="6c6fb-117">Для получения ссылки на ячейки **LockThemeFonts** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="6c6fb-117">To get a reference to the **LockThemeFonts** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6c6fb-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6c6fb-118">Section index:</span></span>  <br/> |<span data-ttu-id="6c6fb-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6c6fb-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6c6fb-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6c6fb-120">Row index:</span></span>  <br/> |<span data-ttu-id="6c6fb-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="6c6fb-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="6c6fb-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6c6fb-122">Cell index:</span></span>  <br/> |<span data-ttu-id="6c6fb-123">**visLockThemeFonts**</span><span class="sxs-lookup"><span data-stu-id="6c6fb-123">**visLockThemeFonts**</span></span> <br/> |
   

