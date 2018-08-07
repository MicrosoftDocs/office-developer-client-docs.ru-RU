---
title: Ячейка LockVariation (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Определяет, будет ли вариантов темы, применяются на страницу или форму можно изменить, как логическое значение.
ms.openlocfilehash: c3c272a637f28aa4df43f6c23030d6676280138e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814172"
---
# <a name="lockvariation-cell-protection-section"></a><span data-ttu-id="8153e-103">Ячейка LockVariation (раздел "Защита")</span><span class="sxs-lookup"><span data-stu-id="8153e-103">LockVariation Cell (Protection Section)</span></span>

<span data-ttu-id="8153e-104">Определяет, будет ли вариантов темы, применяются на страницу или форму можно изменить, как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="8153e-104">Determines whether the theme variation applied to the page or shape can be changed, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8153e-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="8153e-105">TRUE</span></span>  <br/> |<span data-ttu-id="8153e-106">Нельзя изменить текущий вариантов, применяется к странице или фигуры.</span><span class="sxs-lookup"><span data-stu-id="8153e-106">The current variation applied to the page or shape cannot be changed.</span></span>  <br/> |
|<span data-ttu-id="8153e-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="8153e-107">FALSE</span></span>  <br/> |<span data-ttu-id="8153e-108">Можно изменить вариантов фигуры или страницы.</span><span class="sxs-lookup"><span data-stu-id="8153e-108">The variation of the page or shape can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8153e-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="8153e-109">Remarks</span></span>

<span data-ttu-id="8153e-110">Для получения ссылки на ячейки **LockVariation** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="8153e-110">To get a reference to the **LockVariation** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8153e-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="8153e-111">Cell name:</span></span>  <br/> | <span data-ttu-id="8153e-112">LockVariation</span><span class="sxs-lookup"><span data-stu-id="8153e-112">LockVariation</span></span>  <br/> |
   
<span data-ttu-id="8153e-113">Для получения ссылки на ячейки **LockVariation** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="8153e-113">To get a reference to the **LockVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8153e-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8153e-114">Section index:</span></span>  <br/> |<span data-ttu-id="8153e-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8153e-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8153e-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8153e-116">Row index:</span></span>  <br/> |<span data-ttu-id="8153e-117">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="8153e-117">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="8153e-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8153e-118">Cell index:</span></span>  <br/> |<span data-ttu-id="8153e-119">**visLockVariation**</span><span class="sxs-lookup"><span data-stu-id="8153e-119">**visLockVariation**</span></span> <br/> |
   

