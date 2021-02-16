---
title: LockThemeIndex Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Предотвращает изменение ячейки ThemeIndex в строке "Свойства темы" путем применения новой темы или выбора новой схемы соединителя. Не мешает пользователям вручную редактировать это значение в таблице shapeSheet.
ms.openlocfilehash: 519c17f6e00c9aad2b5522bc66b41c0ceb75911b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411241"
---
# <a name="lockthemeindex-cell-protection-section"></a><span data-ttu-id="1b431-104">LockThemeIndex Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="1b431-104">LockThemeIndex Cell (Protection Section)</span></span>

<span data-ttu-id="1b431-105">Предотвращает изменение **ячейки ThemeIndex** в строке **"Свойства** темы" путем применения новой темы или выбора новой схемы соединителя.</span><span class="sxs-lookup"><span data-stu-id="1b431-105">Prevents **ThemeIndex** cell in **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="1b431-106">Не мешает пользователям вручную редактировать это значение в таблице shapeSheet.</span><span class="sxs-lookup"><span data-stu-id="1b431-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="1b431-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="1b431-107">**Value**</span></span>|<span data-ttu-id="1b431-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1b431-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b431-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="1b431-109">TRUE</span></span>  <br/> |<span data-ttu-id="1b431-110">Ячейку **ThemeIndex** нельзя изменить с текущего значения, если она не изменена непосредственно в shapeSheet.</span><span class="sxs-lookup"><span data-stu-id="1b431-110">The **ThemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="1b431-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="1b431-111">FALSE</span></span>  <br/> |<span data-ttu-id="1b431-112">При смене темы ячейку **ThemeIndex** можно изменить с текущего значения.</span><span class="sxs-lookup"><span data-stu-id="1b431-112">The **ThemeIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b431-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="1b431-113">Remarks</span></span>

<span data-ttu-id="1b431-114">Чтобы получить ссылку на ячейку **LockThemeIndex** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="1b431-114">To get a reference to the **LockThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1b431-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="1b431-115">Cell name:</span></span>  <br/> | <span data-ttu-id="1b431-116">LockThemeIndex</span><span class="sxs-lookup"><span data-stu-id="1b431-116">LockThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="1b431-117">Чтобы получить ссылку на ячейку **LockThemeIndex** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="1b431-117">To get a reference to the **LockThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1b431-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="1b431-118">Section index:</span></span>  <br/> |<span data-ttu-id="1b431-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1b431-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1b431-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="1b431-120">Row index:</span></span>  <br/> |<span data-ttu-id="1b431-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="1b431-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="1b431-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="1b431-122">Cell index:</span></span>  <br/> |<span data-ttu-id="1b431-123">**visLockThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="1b431-123">**visLockThemeIndex**</span></span> <br/> |
   

