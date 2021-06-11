---
title: LockThemeConnectors Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Предотвращает изменение ячейки ConnectorsSchemeIndex в строке Свойства темы путем применения новой темы или выбора новой схемы соединителя. Не мешает пользователям вручную изменять это значение в ShapeSheet.
ms.openlocfilehash: 8097e50646fd59f4ac0212cbe9ca2ecfaadab7a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438409"
---
# <a name="lockthemeconnectors-cell-protection-section"></a><span data-ttu-id="2d253-104">LockThemeConnectors Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="2d253-104">LockThemeConnectors Cell (Protection Section)</span></span>

<span data-ttu-id="2d253-105">Предотвращает изменение **ячейки ConnectorsSchemeIndex** в строке **Свойства** темы путем применения новой темы или выбора новой схемы соединителя.</span><span class="sxs-lookup"><span data-stu-id="2d253-105">Prevents the **ConnectorsSchemeIndex** cell in the **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="2d253-106">Не мешает пользователям вручную изменять это значение в ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="2d253-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="2d253-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="2d253-107">**Value**</span></span>|<span data-ttu-id="2d253-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2d253-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2d253-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="2d253-109">TRUE</span></span>  <br/> |<span data-ttu-id="2d253-110">Ячейка **ConnectorsSchemeIndex** не может быть изменена с текущего значения, если не будет изменена непосредственно в ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="2d253-110">The **ConnectorsSchemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="2d253-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="2d253-111">FALSE</span></span>  <br/> |<span data-ttu-id="2d253-112">Ячейка **ConnectorsSchemeIndex** может быть изменена с текущего значения на пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2d253-112">The **ConnectorsSchemeIndex** cell can be changed from its current value through the UI.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d253-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="2d253-113">Remarks</span></span>

<span data-ttu-id="2d253-114">Чтобы получить ссылку на ячейку **LockThemeConnectors** по имени из другой формулы, по значению **атрибута N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="2d253-114">To get a reference to the **LockThemeConnectors** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2d253-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="2d253-115">Cell name:</span></span>  <br/> | <span data-ttu-id="2d253-116">LockThemeConnectors</span><span class="sxs-lookup"><span data-stu-id="2d253-116">LockThemeConnectors</span></span>  <br/> |
   
<span data-ttu-id="2d253-117">Чтобы получить ссылку на ячейку **LockThemeConnectors** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="2d253-117">To get a reference to the **LockThemeConnectors** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2d253-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2d253-118">Section index:</span></span>  <br/> |<span data-ttu-id="2d253-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2d253-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2d253-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2d253-120">Row index:</span></span>  <br/> |<span data-ttu-id="2d253-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="2d253-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="2d253-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2d253-122">Cell index:</span></span>  <br/> |<span data-ttu-id="2d253-123">**visLockThemeConnectors**</span><span class="sxs-lookup"><span data-stu-id="2d253-123">**visLockThemeConnectors**</span></span> <br/> |
   

