---
title: LockThemeConnectors Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Запрещает изменение ячейки Коннекторссчемеиндекс в строке "свойства темы" путем применения новой темы или выбора новой схемы соединителей. Не запрещает пользователям вручную изменять это значение в таблице свойств фигуры.
ms.openlocfilehash: 8097e50646fd59f4ac0212cbe9ca2ecfaadab7a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438409"
---
# <a name="lockthemeconnectors-cell-protection-section"></a><span data-ttu-id="9a608-104">LockThemeConnectors Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="9a608-104">LockThemeConnectors Cell (Protection Section)</span></span>

<span data-ttu-id="9a608-105">Запрещает изменение ячейки **коннекторссчемеиндекс** в строке " **свойства темы** " путем применения новой темы или выбора новой схемы соединителей.</span><span class="sxs-lookup"><span data-stu-id="9a608-105">Prevents the **ConnectorsSchemeIndex** cell in the **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="9a608-106">Не запрещает пользователям вручную изменять это значение в таблице свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="9a608-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="9a608-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="9a608-107">**Value**</span></span>|<span data-ttu-id="9a608-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9a608-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9a608-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="9a608-109">TRUE</span></span>  <br/> |<span data-ttu-id="9a608-110">Ячейка **коннекторссчемеиндекс** не может быть изменена с текущим значением, если только таблица свойств не будет изменена напрямую.</span><span class="sxs-lookup"><span data-stu-id="9a608-110">The **ConnectorsSchemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="9a608-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="9a608-111">FALSE</span></span>  <br/> |<span data-ttu-id="9a608-112">Ячейка **коннекторссчемеиндекс** может быть изменена из текущего значения с помощью пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9a608-112">The **ConnectorsSchemeIndex** cell can be changed from its current value through the UI.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a608-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="9a608-113">Remarks</span></span>

<span data-ttu-id="9a608-114">Чтобы получить ссылку на ячейку **LockThemeConnectors** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="9a608-114">To get a reference to the **LockThemeConnectors** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9a608-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="9a608-115">Cell name:</span></span>  <br/> | <span data-ttu-id="9a608-116">LockThemeConnectors</span><span class="sxs-lookup"><span data-stu-id="9a608-116">LockThemeConnectors</span></span>  <br/> |
   
<span data-ttu-id="9a608-117">Чтобы получить ссылку на ячейку **LockThemeConnectors** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="9a608-117">To get a reference to the **LockThemeConnectors** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9a608-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9a608-118">Section index:</span></span>  <br/> |<span data-ttu-id="9a608-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9a608-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9a608-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9a608-120">Row index:</span></span>  <br/> |<span data-ttu-id="9a608-121">**висровлокк**</span><span class="sxs-lookup"><span data-stu-id="9a608-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="9a608-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9a608-122">Cell index:</span></span>  <br/> |<span data-ttu-id="9a608-123">**вислокксемеконнекторс**</span><span class="sxs-lookup"><span data-stu-id="9a608-123">**visLockThemeConnectors**</span></span> <br/> |
   

