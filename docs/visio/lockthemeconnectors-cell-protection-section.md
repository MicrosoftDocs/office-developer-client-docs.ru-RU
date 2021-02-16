---
title: LockThemeConnectors Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Предотвращает изменение ячейки ConnectorsSchemeIndex в строке "Свойства темы" путем применения новой темы или выбора новой схемы соединителя. Не мешает пользователям вручную редактировать это значение в таблице shapeSheet.
ms.openlocfilehash: 8097e50646fd59f4ac0212cbe9ca2ecfaadab7a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438409"
---
# <a name="lockthemeconnectors-cell-protection-section"></a><span data-ttu-id="d3c92-104">LockThemeConnectors Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="d3c92-104">LockThemeConnectors Cell (Protection Section)</span></span>

<span data-ttu-id="d3c92-105">Предотвращает изменение **ячейки ConnectorsSchemeIndex** в строке **"Свойства** темы" путем применения новой темы или выбора новой схемы соединителя.</span><span class="sxs-lookup"><span data-stu-id="d3c92-105">Prevents the **ConnectorsSchemeIndex** cell in the **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="d3c92-106">Не мешает пользователям вручную редактировать это значение в таблице shapeSheet.</span><span class="sxs-lookup"><span data-stu-id="d3c92-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="d3c92-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="d3c92-107">**Value**</span></span>|<span data-ttu-id="d3c92-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d3c92-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d3c92-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="d3c92-109">TRUE</span></span>  <br/> |<span data-ttu-id="d3c92-110">Ячейку **ConnectorsSchemeIndex** нельзя изменить по текущему значению, если она не изменена непосредственно в shapeSheet.</span><span class="sxs-lookup"><span data-stu-id="d3c92-110">The **ConnectorsSchemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="d3c92-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="d3c92-111">FALSE</span></span>  <br/> |<span data-ttu-id="d3c92-112">Ячейку **ConnectorsSchemeIndex** можно изменить с текущего значения через пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d3c92-112">The **ConnectorsSchemeIndex** cell can be changed from its current value through the UI.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3c92-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="d3c92-113">Remarks</span></span>

<span data-ttu-id="d3c92-114">Чтобы получить ссылку на ячейку **LockThemeConnectors** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="d3c92-114">To get a reference to the **LockThemeConnectors** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d3c92-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d3c92-115">Cell name:</span></span>  <br/> | <span data-ttu-id="d3c92-116">LockThemeConnectors</span><span class="sxs-lookup"><span data-stu-id="d3c92-116">LockThemeConnectors</span></span>  <br/> |
   
<span data-ttu-id="d3c92-117">Чтобы получить ссылку на ячейку **LockThemeConnectors** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d3c92-117">To get a reference to the **LockThemeConnectors** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d3c92-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d3c92-118">Section index:</span></span>  <br/> |<span data-ttu-id="d3c92-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d3c92-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d3c92-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d3c92-120">Row index:</span></span>  <br/> |<span data-ttu-id="d3c92-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="d3c92-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="d3c92-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d3c92-122">Cell index:</span></span>  <br/> |<span data-ttu-id="d3c92-123">**visLockThemeConnectors**</span><span class="sxs-lookup"><span data-stu-id="d3c92-123">**visLockThemeConnectors**</span></span> <br/> |
   

