---
title: Ячейка QuickStyleType (раздел "Экспресс-стиль")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Определяет тип экспресс-стилей (2 измерения, 1 измерения или соединитель), который наследует фигуры.
ms.openlocfilehash: 211074800eee601d2658edbc03bb95d028920e54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814514"
---
# <a name="quickstyletype-cell-quick-style-section"></a><span data-ttu-id="a9bcd-103">Ячейка QuickStyleType (раздел "Экспресс-стиль")</span><span class="sxs-lookup"><span data-stu-id="a9bcd-103">QuickStyleType Cell (Quick Style Section)</span></span>

<span data-ttu-id="a9bcd-104">Определяет тип экспресс-стилей (2 измерения, 1 измерения или соединитель), который наследует фигуры.</span><span class="sxs-lookup"><span data-stu-id="a9bcd-104">Determines the type of Quick Style (2-dimensional, 1-dimensional, or connector) that the shape inherits.</span></span> 
  
|<span data-ttu-id="a9bcd-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a9bcd-105">**Value**</span></span>|<span data-ttu-id="a9bcd-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a9bcd-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a9bcd-107">0</span><span class="sxs-lookup"><span data-stu-id="a9bcd-107">0</span></span>  <br/> |<span data-ttu-id="a9bcd-108">Автоматически выбирает Visio</span><span class="sxs-lookup"><span data-stu-id="a9bcd-108">Visio chooses automatically</span></span>  <br/> |
|<span data-ttu-id="a9bcd-109">1</span><span class="sxs-lookup"><span data-stu-id="a9bcd-109">1</span></span>  <br/> |<span data-ttu-id="a9bcd-110">измерения 1</span><span class="sxs-lookup"><span data-stu-id="a9bcd-110">1-dimensional</span></span>  <br/> |
|<span data-ttu-id="a9bcd-111">2</span><span class="sxs-lookup"><span data-stu-id="a9bcd-111">2</span></span>  <br/> |<span data-ttu-id="a9bcd-112">2 измерения</span><span class="sxs-lookup"><span data-stu-id="a9bcd-112">2-dimensional</span></span>  <br/> |
|<span data-ttu-id="a9bcd-113">3</span><span class="sxs-lookup"><span data-stu-id="a9bcd-113">3</span></span>  <br/> |<span data-ttu-id="a9bcd-114">Соединитель</span><span class="sxs-lookup"><span data-stu-id="a9bcd-114">Connector</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9bcd-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="a9bcd-115">Remarks</span></span>

<span data-ttu-id="a9bcd-116">Для получения ссылки на ячейки **QuickStyleType** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="a9bcd-116">To get a reference to the **QuickStyleType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a9bcd-117">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="a9bcd-117">Cell name:</span></span>  <br/> | <span data-ttu-id="a9bcd-118">QuickStyleType</span><span class="sxs-lookup"><span data-stu-id="a9bcd-118">QuickStyleType</span></span>  <br/> |
   
<span data-ttu-id="a9bcd-119">Для получения ссылки на ячейки **QuickStyleType** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="a9bcd-119">To get a reference to the **QuickStyleType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a9bcd-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a9bcd-120">Section index:</span></span>  <br/> |<span data-ttu-id="a9bcd-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a9bcd-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a9bcd-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a9bcd-122">Row index:</span></span>  <br/> |<span data-ttu-id="a9bcd-123">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="a9bcd-123">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="a9bcd-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a9bcd-124">Cell index:</span></span>  <br/> |<span data-ttu-id="a9bcd-125">**visQuickStyleType**</span><span class="sxs-lookup"><span data-stu-id="a9bcd-125">**visQuickStyleType**</span></span> <br/> |
   

