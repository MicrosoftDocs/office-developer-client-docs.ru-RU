---
title: InhibitSnap Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251620
localization_priority: Normal
ms.assetid: ab9fcebc-1550-3b9e-e3b4-e8b92424390b
description: Определяет, прикрепит ли фигуры на переднем плане к другим объектам на странице и фигуры на фоновой странице.
ms.openlocfilehash: 665130e9f9f938349028ffa1d1c06224e746de5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426753"
---
# <a name="inhibitsnap-cell-page-properties-section"></a><span data-ttu-id="aa6d3-103">InhibitSnap Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="aa6d3-103">InhibitSnap Cell (Page Properties Section)</span></span>

<span data-ttu-id="aa6d3-104">Определяет, прикрепит ли фигуры на переднем плане к другим объектам на странице и фигуры на фоновой странице.</span><span class="sxs-lookup"><span data-stu-id="aa6d3-104">Determines whether the shapes on a foreground page snap to other objects on the page and shapes on the background page.</span></span>
  
|<span data-ttu-id="aa6d3-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="aa6d3-105">**Value**</span></span>|<span data-ttu-id="aa6d3-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="aa6d3-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="aa6d3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="aa6d3-107">TRUE</span></span>  <br/> | <span data-ttu-id="aa6d3-108">Ингибирование всех щелкающих на странице, за исключением привязки к линейке и сетке.</span><span class="sxs-lookup"><span data-stu-id="aa6d3-108">Inhibit all snapping on the page, except for snapping to the ruler and grid.</span></span>  <br/> |
| <span data-ttu-id="aa6d3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="aa6d3-109">FALSE</span></span>  <br/> | <span data-ttu-id="aa6d3-110">Включить привязку.</span><span class="sxs-lookup"><span data-stu-id="aa6d3-110">Enable snapping.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa6d3-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="aa6d3-111">Remarks</span></span>

<span data-ttu-id="aa6d3-112">Чтобы получить ссылку на ячейку InhibitSnap по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="aa6d3-112">To get a reference to the InhibitSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aa6d3-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="aa6d3-113">Cell name:</span></span>  <br/> | <span data-ttu-id="aa6d3-114">InhibitSnap</span><span class="sxs-lookup"><span data-stu-id="aa6d3-114">InhibitSnap</span></span>  <br/> |
   
<span data-ttu-id="aa6d3-115">Чтобы получить ссылку на ячейку InhibitSnap по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="aa6d3-115">To get a reference to the InhibitSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aa6d3-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="aa6d3-116">Section index:</span></span>  <br/> |<span data-ttu-id="aa6d3-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="aa6d3-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="aa6d3-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="aa6d3-118">Row index:</span></span>  <br/> |<span data-ttu-id="aa6d3-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="aa6d3-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="aa6d3-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="aa6d3-120">Cell index:</span></span>  <br/> |<span data-ttu-id="aa6d3-121">**visPageInhibitSnap**</span><span class="sxs-lookup"><span data-stu-id="aa6d3-121">**visPageInhibitSnap**</span></span> <br/> |
   

