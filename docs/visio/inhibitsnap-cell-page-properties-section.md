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
description: Определяет, привязываются ли фигуры на переднем плане к другим объектам на странице и фигурам на фоновой странице.
ms.openlocfilehash: 665130e9f9f938349028ffa1d1c06224e746de5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426753"
---
# <a name="inhibitsnap-cell-page-properties-section"></a><span data-ttu-id="aab07-103">InhibitSnap Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="aab07-103">InhibitSnap Cell (Page Properties Section)</span></span>

<span data-ttu-id="aab07-104">Определяет, привязываются ли фигуры на переднем плане к другим объектам на странице и фигурам на фоновой странице.</span><span class="sxs-lookup"><span data-stu-id="aab07-104">Determines whether the shapes on a foreground page snap to other objects on the page and shapes on the background page.</span></span>
  
|<span data-ttu-id="aab07-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="aab07-105">**Value**</span></span>|<span data-ttu-id="aab07-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="aab07-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="aab07-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="aab07-107">TRUE</span></span>  <br/> | <span data-ttu-id="aab07-108">Запрет на все привязки на странице, за исключением привязки к линейке и сетке.</span><span class="sxs-lookup"><span data-stu-id="aab07-108">Inhibit all snapping on the page, except for snapping to the ruler and grid.</span></span>  <br/> |
| <span data-ttu-id="aab07-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="aab07-109">FALSE</span></span>  <br/> | <span data-ttu-id="aab07-110">Включить привязку.</span><span class="sxs-lookup"><span data-stu-id="aab07-110">Enable snapping.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aab07-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="aab07-111">Remarks</span></span>

<span data-ttu-id="aab07-112">Чтобы получить ссылку на ячейку InhibitSnap по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="aab07-112">To get a reference to the InhibitSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aab07-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="aab07-113">Cell name:</span></span>  <br/> | <span data-ttu-id="aab07-114">InhibitSnap</span><span class="sxs-lookup"><span data-stu-id="aab07-114">InhibitSnap</span></span>  <br/> |
   
<span data-ttu-id="aab07-115">Чтобы получить ссылку на ячейку InhibitSnap по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="aab07-115">To get a reference to the InhibitSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aab07-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="aab07-116">Section index:</span></span>  <br/> |<span data-ttu-id="aab07-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="aab07-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="aab07-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="aab07-118">Row index:</span></span>  <br/> |<span data-ttu-id="aab07-119">**Висровпаже**</span><span class="sxs-lookup"><span data-stu-id="aab07-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="aab07-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="aab07-120">Cell index:</span></span>  <br/> |<span data-ttu-id="aab07-121">**Виспажеинхибитснап**</span><span class="sxs-lookup"><span data-stu-id="aab07-121">**visPageInhibitSnap**</span></span> <br/> |
   

