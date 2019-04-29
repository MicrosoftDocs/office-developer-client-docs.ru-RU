---
title: NoShow Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
localization_priority: Normal
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: Указывает, отображается ли путь на странице документа.
ms.openlocfilehash: bd42b069e6796b107aafaea3080f6970c4f678c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410352"
---
# <a name="noshow-cell-geometry-section"></a><span data-ttu-id="68614-103">NoShow Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="68614-103">NoShow Cell (Geometry Section)</span></span>

<span data-ttu-id="68614-104">Указывает, отображается ли путь на странице документа.</span><span class="sxs-lookup"><span data-stu-id="68614-104">Indicates whether a path is displayed on the drawing page.</span></span>
  
|<span data-ttu-id="68614-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="68614-105">**Value**</span></span>|<span data-ttu-id="68614-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="68614-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="68614-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="68614-107">TRUE</span></span>  <br/> | <span data-ttu-id="68614-108">Обводка и заливка контура, представленного в разделе, скрыта.</span><span class="sxs-lookup"><span data-stu-id="68614-108">The stroke and fill of the path represented by the section is hidden.</span></span>  <br/> |
| <span data-ttu-id="68614-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="68614-109">FALSE</span></span>  <br/> | <span data-ttu-id="68614-110">Отображается обводка и заливка контура.</span><span class="sxs-lookup"><span data-stu-id="68614-110">The stroke and fill of the path is shown.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68614-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="68614-111">Remarks</span></span>

<span data-ttu-id="68614-112">Чтобы получить ссылку на ячейку Show по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="68614-112">To get a reference to the NoShow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="68614-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="68614-113">Cell name:</span></span>  <br/> | <span data-ttu-id="68614-114">Геометрия *i* . Показать, где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="68614-114">Geometry  *i*  .NoShow            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="68614-115">Чтобы получить ссылку на ячейку Show по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="68614-115">To get a reference to the NoShow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="68614-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="68614-116">Section index:</span></span>  <br/> |<span data-ttu-id="68614-117">**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="68614-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="68614-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="68614-118">Row index:</span></span>  <br/> |<span data-ttu-id="68614-119">**Висровкомпонент**</span><span class="sxs-lookup"><span data-stu-id="68614-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="68614-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="68614-120">Cell index:</span></span>  <br/> |<span data-ttu-id="68614-121">**Вискомпношов**</span><span class="sxs-lookup"><span data-stu-id="68614-121">**visCompNoShow**</span></span> <br/> |
   

