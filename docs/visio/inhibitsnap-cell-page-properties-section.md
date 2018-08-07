---
title: Ячейка InhibitSnap (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251620
localization_priority: Normal
ms.assetid: ab9fcebc-1550-3b9e-e3b4-e8b92424390b
description: Определяет, будет ли фигуры на переднем плане привязать к другие объекты на странице и фигуры на странице заднего плана.
ms.openlocfilehash: b95dafda9ebef36db34f60585ab3ed2164ade415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813962"
---
# <a name="inhibitsnap-cell-page-properties-section"></a><span data-ttu-id="865e9-103">Ячейка InhibitSnap (раздел "Свойства страницы")</span><span class="sxs-lookup"><span data-stu-id="865e9-103">InhibitSnap Cell (Page Properties Section)</span></span>

<span data-ttu-id="865e9-104">Определяет, будет ли фигуры на переднем плане привязать к другие объекты на странице и фигуры на странице заднего плана.</span><span class="sxs-lookup"><span data-stu-id="865e9-104">Determines whether the shapes on a foreground page snap to other objects on the page and shapes on the background page.</span></span>
  
|<span data-ttu-id="865e9-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="865e9-105">**Value**</span></span>|<span data-ttu-id="865e9-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="865e9-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="865e9-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="865e9-107">TRUE</span></span>  <br/> | <span data-ttu-id="865e9-108">Запретить все привязки на странице, за исключением привязка к линейки и сетки.</span><span class="sxs-lookup"><span data-stu-id="865e9-108">Inhibit all snapping on the page, except for snapping to the ruler and grid.</span></span>  <br/> |
| <span data-ttu-id="865e9-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="865e9-109">FALSE</span></span>  <br/> | <span data-ttu-id="865e9-110">Включение привязки.</span><span class="sxs-lookup"><span data-stu-id="865e9-110">Enable snapping.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="865e9-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="865e9-111">Remarks</span></span>

<span data-ttu-id="865e9-112">Чтобы получить ссылку на ячейку InhibitSnap по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="865e9-112">To get a reference to the InhibitSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="865e9-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="865e9-113">Cell name:</span></span>  <br/> | <span data-ttu-id="865e9-114">InhibitSnap</span><span class="sxs-lookup"><span data-stu-id="865e9-114">InhibitSnap</span></span>  <br/> |
   
<span data-ttu-id="865e9-115">Для получения ссылки на ячейки InhibitSnap по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="865e9-115">To get a reference to the InhibitSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="865e9-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="865e9-116">Section index:</span></span>  <br/> |<span data-ttu-id="865e9-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="865e9-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="865e9-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="865e9-118">Row index:</span></span>  <br/> |<span data-ttu-id="865e9-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="865e9-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="865e9-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="865e9-120">Cell index:</span></span>  <br/> |<span data-ttu-id="865e9-121">**visPageInhibitSnap**</span><span class="sxs-lookup"><span data-stu-id="865e9-121">**visPageInhibitSnap**</span></span> <br/> |
   

