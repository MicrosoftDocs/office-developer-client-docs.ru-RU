---
title: LockThemeFonts Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Предотвращает изменение ячейки FontIndex в строке Свойства темы, применяя новую тему. Не мешает пользователям вручную изменять это значение в ShapeSheet.
ms.openlocfilehash: b3bd21c1dcd8c8c13d843c50cb29edcc5b8c4999
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421230"
---
# <a name="lockthemefonts-cell-protection-section"></a><span data-ttu-id="14a4e-104">LockThemeFonts Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="14a4e-104">LockThemeFonts Cell (Protection Section)</span></span>

<span data-ttu-id="14a4e-105">Предотвращает изменение **ячейки FontIndex** в строке **Свойства** темы, применяя новую тему.</span><span class="sxs-lookup"><span data-stu-id="14a4e-105">Prevents the **FontIndex** cell in the **Theme Properties** row from being altered by applying a new theme.</span></span> <span data-ttu-id="14a4e-106">Не мешает пользователям вручную изменять это значение в ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="14a4e-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="14a4e-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="14a4e-107">**Value**</span></span>|<span data-ttu-id="14a4e-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="14a4e-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="14a4e-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="14a4e-109">TRUE</span></span>  <br/> |<span data-ttu-id="14a4e-110">Ячейка **FontIndex** не может быть изменена с текущего значения, если она не будет изменена непосредственно в ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="14a4e-110">The **FontIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="14a4e-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="14a4e-111">FALSE</span></span>  <br/> |<span data-ttu-id="14a4e-112">Ячейка **FontIndex** может быть изменена с текущего значения при смене темы.</span><span class="sxs-lookup"><span data-stu-id="14a4e-112">The **FontIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14a4e-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="14a4e-113">Remarks</span></span>

<span data-ttu-id="14a4e-114">Чтобы получить ссылку на ячейку **LockThemeFonts** по имени из другой формулы, по значению **атрибута N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="14a4e-114">To get a reference to the **LockThemeFonts** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="14a4e-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="14a4e-115">Cell name:</span></span>  <br/> | <span data-ttu-id="14a4e-116">LockThemeFonts</span><span class="sxs-lookup"><span data-stu-id="14a4e-116">LockThemeFonts</span></span>  <br/> |
   
<span data-ttu-id="14a4e-117">Чтобы получить ссылку на ячейку **LockThemeFonts** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="14a4e-117">To get a reference to the **LockThemeFonts** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="14a4e-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="14a4e-118">Section index:</span></span>  <br/> |<span data-ttu-id="14a4e-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="14a4e-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="14a4e-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="14a4e-120">Row index:</span></span>  <br/> |<span data-ttu-id="14a4e-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="14a4e-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="14a4e-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="14a4e-122">Cell index:</span></span>  <br/> |<span data-ttu-id="14a4e-123">**visLockThemeFonts**</span><span class="sxs-lookup"><span data-stu-id="14a4e-123">**visLockThemeFonts**</span></span> <br/> |
   

