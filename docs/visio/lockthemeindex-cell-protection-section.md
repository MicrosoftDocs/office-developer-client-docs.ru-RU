---
title: Ячейка LockThemeIndex (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Запрещает ThemeIndex ячейка в строке темы свойств изменяются применение новой темы или выбрать новую схему соединителя. Запрещает пользователям изменять это значение в таблице свойств фигуры вручную.
ms.openlocfilehash: 4bef3eb799c943ff89027e69ae8580c9c0e51243
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814158"
---
# <a name="lockthemeindex-cell-protection-section"></a><span data-ttu-id="d856f-104">Ячейка LockThemeIndex (раздел Защита)</span><span class="sxs-lookup"><span data-stu-id="d856f-104">LockThemeIndex Cell (Protection Section)</span></span>

<span data-ttu-id="d856f-105">Запрещает **ThemeIndex** ячейка в строке **Темы свойств** изменяются применение новой темы или выбрать новую схему соединителя.</span><span class="sxs-lookup"><span data-stu-id="d856f-105">Prevents **ThemeIndex** cell in **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="d856f-106">Запрещает пользователям изменять это значение в таблице свойств фигуры вручную.</span><span class="sxs-lookup"><span data-stu-id="d856f-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="d856f-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="d856f-107">**Value**</span></span>|<span data-ttu-id="d856f-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d856f-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d856f-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="d856f-109">TRUE</span></span>  <br/> |<span data-ttu-id="d856f-110">Ячейка **ThemeIndex** может быть изменен с текущим значением только напрямую изменить в таблице свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="d856f-110">The **ThemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="d856f-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="d856f-111">FALSE</span></span>  <br/> |<span data-ttu-id="d856f-112">Ячейка **ThemeIndex** могут изменяться с текущим значением при изменении темы.</span><span class="sxs-lookup"><span data-stu-id="d856f-112">The **ThemeIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d856f-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="d856f-113">Remarks</span></span>

<span data-ttu-id="d856f-114">Для получения ссылки на ячейки **LockThemeIndex** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="d856f-114">To get a reference to the **LockThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d856f-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="d856f-115">Cell name:</span></span>  <br/> | <span data-ttu-id="d856f-116">LockThemeIndex</span><span class="sxs-lookup"><span data-stu-id="d856f-116">LockThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="d856f-117">Для получения ссылки на ячейки **LockThemeIndex** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="d856f-117">To get a reference to the **LockThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d856f-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d856f-118">Section index:</span></span>  <br/> |<span data-ttu-id="d856f-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d856f-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d856f-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d856f-120">Row index:</span></span>  <br/> |<span data-ttu-id="d856f-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="d856f-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="d856f-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d856f-122">Cell index:</span></span>  <br/> |<span data-ttu-id="d856f-123">**visLockThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="d856f-123">**visLockThemeIndex**</span></span> <br/> |
   

