---
title: Ячейка LockThemeConnectors (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Запрещает ConnectorsSchemeIndex ячейку в строке темы свойств изменяются применение новой темы или выбрать новую схему соединителя. Запрещает пользователям изменять это значение в таблице свойств фигуры вручную.
ms.openlocfilehash: c74bcf554f0f14de47480397a96680469826d2c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814155"
---
# <a name="lockthemeconnectors-cell-protection-section"></a><span data-ttu-id="a8cf1-104">Ячейка LockThemeConnectors (раздел "Защита")</span><span class="sxs-lookup"><span data-stu-id="a8cf1-104">LockThemeConnectors Cell (Protection Section)</span></span>

<span data-ttu-id="a8cf1-105">Запрещает **ConnectorsSchemeIndex** ячейку в строке **Темы свойств** изменяются применение новой темы или выбрать новую схему соединителя.</span><span class="sxs-lookup"><span data-stu-id="a8cf1-105">Prevents the **ConnectorsSchemeIndex** cell in the **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="a8cf1-106">Запрещает пользователям изменять это значение в таблице свойств фигуры вручную.</span><span class="sxs-lookup"><span data-stu-id="a8cf1-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="a8cf1-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a8cf1-107">**Value**</span></span>|<span data-ttu-id="a8cf1-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a8cf1-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8cf1-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="a8cf1-109">TRUE</span></span>  <br/> |<span data-ttu-id="a8cf1-110">Ячейка **ConnectorsSchemeIndex** может быть изменен с текущим значением только напрямую изменить в таблице свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="a8cf1-110">The **ConnectorsSchemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="a8cf1-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="a8cf1-111">FALSE</span></span>  <br/> |<span data-ttu-id="a8cf1-112">Ячейка **ConnectorsSchemeIndex** могут изменяться с текущим значением в пользовательском Интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="a8cf1-112">The **ConnectorsSchemeIndex** cell can be changed from its current value through the UI.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8cf1-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="a8cf1-113">Remarks</span></span>

<span data-ttu-id="a8cf1-114">Для получения ссылки на ячейки **LockThemeConnectors** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="a8cf1-114">To get a reference to the **LockThemeConnectors** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a8cf1-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="a8cf1-115">Cell name:</span></span>  <br/> | <span data-ttu-id="a8cf1-116">LockThemeConnectors</span><span class="sxs-lookup"><span data-stu-id="a8cf1-116">LockThemeConnectors</span></span>  <br/> |
   
<span data-ttu-id="a8cf1-117">Для получения ссылки на ячейки **LockThemeConnectors** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="a8cf1-117">To get a reference to the **LockThemeConnectors** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a8cf1-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a8cf1-118">Section index:</span></span>  <br/> |<span data-ttu-id="a8cf1-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a8cf1-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a8cf1-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a8cf1-120">Row index:</span></span>  <br/> |<span data-ttu-id="a8cf1-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="a8cf1-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="a8cf1-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a8cf1-122">Cell index:</span></span>  <br/> |<span data-ttu-id="a8cf1-123">**visLockThemeConnectors**</span><span class="sxs-lookup"><span data-stu-id="a8cf1-123">**visLockThemeConnectors**</span></span> <br/> |
   

