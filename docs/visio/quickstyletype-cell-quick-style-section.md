---
title: QuickStyleType Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Определяет тип Quick Style (2-мерный, 1-мерный или соединитатель), который наследует фигура.
ms.openlocfilehash: 95aced62c6397fc3229de29b98d3f18e5f69d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410506"
---
# <a name="quickstyletype-cell-quick-style-section"></a><span data-ttu-id="fc21d-103">QuickStyleType Cell (Quick Style Section)</span><span class="sxs-lookup"><span data-stu-id="fc21d-103">QuickStyleType Cell (Quick Style Section)</span></span>

<span data-ttu-id="fc21d-104">Определяет тип Quick Style (2-мерный, 1-мерный или соединитатель), который наследует фигура.</span><span class="sxs-lookup"><span data-stu-id="fc21d-104">Determines the type of Quick Style (2-dimensional, 1-dimensional, or connector) that the shape inherits.</span></span> 
  
|<span data-ttu-id="fc21d-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="fc21d-105">**Value**</span></span>|<span data-ttu-id="fc21d-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fc21d-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fc21d-107">0</span><span class="sxs-lookup"><span data-stu-id="fc21d-107">0</span></span>  <br/> |<span data-ttu-id="fc21d-108">Visio выбирает автоматически</span><span class="sxs-lookup"><span data-stu-id="fc21d-108">Visio chooses automatically</span></span>  <br/> |
|<span data-ttu-id="fc21d-109">1</span><span class="sxs-lookup"><span data-stu-id="fc21d-109">1</span></span>  <br/> |<span data-ttu-id="fc21d-110">1-мерный</span><span class="sxs-lookup"><span data-stu-id="fc21d-110">1-dimensional</span></span>  <br/> |
|<span data-ttu-id="fc21d-111">2</span><span class="sxs-lookup"><span data-stu-id="fc21d-111">2</span></span>  <br/> |<span data-ttu-id="fc21d-112">2-мерная</span><span class="sxs-lookup"><span data-stu-id="fc21d-112">2-dimensional</span></span>  <br/> |
|<span data-ttu-id="fc21d-113">3</span><span class="sxs-lookup"><span data-stu-id="fc21d-113">3</span></span>  <br/> |<span data-ttu-id="fc21d-114">Соединитель</span><span class="sxs-lookup"><span data-stu-id="fc21d-114">Connector</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc21d-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="fc21d-115">Remarks</span></span>

<span data-ttu-id="fc21d-116">Чтобы получить ссылку на **ячейку QuickStyleType** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="fc21d-116">To get a reference to the **QuickStyleType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fc21d-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="fc21d-117">Cell name:</span></span>  <br/> | <span data-ttu-id="fc21d-118">QuickStyleType</span><span class="sxs-lookup"><span data-stu-id="fc21d-118">QuickStyleType</span></span>  <br/> |
   
<span data-ttu-id="fc21d-119">Чтобы получить ссылку на **ячейку QuickStyleType** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="fc21d-119">To get a reference to the **QuickStyleType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fc21d-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fc21d-120">Section index:</span></span>  <br/> |<span data-ttu-id="fc21d-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fc21d-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fc21d-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fc21d-122">Row index:</span></span>  <br/> |<span data-ttu-id="fc21d-123">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="fc21d-123">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="fc21d-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fc21d-124">Cell index:</span></span>  <br/> |<span data-ttu-id="fc21d-125">**visQuickStyleType**</span><span class="sxs-lookup"><span data-stu-id="fc21d-125">**visQuickStyleType**</span></span> <br/> |
   

