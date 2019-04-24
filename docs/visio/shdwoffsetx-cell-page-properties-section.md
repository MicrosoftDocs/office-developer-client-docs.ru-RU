---
title: ShdwOffsetX Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251373
localization_priority: Normal
ms.assetid: 92ec9b11-f53f-a1c9-832a-6cac08aa5379
description: Определяет расстояние смещения тени фигуры по горизонтали относительно фигуры в единицах страницы.
ms.openlocfilehash: fbc7d37fc8ba45f3219af6a4350301102954f23d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338754"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a><span data-ttu-id="f6b99-103">ShdwOffsetX Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="f6b99-103">ShdwOffsetX Cell (Page Properties Section)</span></span>

<span data-ttu-id="f6b99-104">Определяет расстояние смещения тени фигуры по горизонтали относительно фигуры в единицах страницы.</span><span class="sxs-lookup"><span data-stu-id="f6b99-104">Determines the distance in page units that a shape's drop shadow is offset horizontally from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f6b99-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6b99-105">Remarks</span></span>

<span data-ttu-id="f6b99-106">Это значение задается в диалоговом окне " **Параметры страницы** " (на вкладке " **конструктор** " щелкните стрелку **Параметры страницы** ).</span><span class="sxs-lookup"><span data-stu-id="f6b99-106">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="f6b99-107">Это значение не зависит от масштаба рисунка.</span><span class="sxs-lookup"><span data-stu-id="f6b99-107">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="f6b99-108">Если масштаб документа изменяется, смещение тени остается прежним.</span><span class="sxs-lookup"><span data-stu-id="f6b99-108">If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="f6b99-109">Чтобы получить ссылку на ячейку ShdwOffsetX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="f6b99-109">To get a reference to the ShdwOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f6b99-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f6b99-110">Cell name:</span></span>  <br/> | <span data-ttu-id="f6b99-111">ShdwOffsetX</span><span class="sxs-lookup"><span data-stu-id="f6b99-111">ShdwOffsetX</span></span>  <br/> |
   
<span data-ttu-id="f6b99-112">Чтобы получить ссылку на ячейку ShdwOffsetX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f6b99-112">To get a reference to the ShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f6b99-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f6b99-113">Section index:</span></span>  <br/> |<span data-ttu-id="f6b99-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f6b99-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f6b99-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f6b99-115">Row index:</span></span>  <br/> |<span data-ttu-id="f6b99-116">**Висровпаже**</span><span class="sxs-lookup"><span data-stu-id="f6b99-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="f6b99-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f6b99-117">Cell index:</span></span>  <br/> |<span data-ttu-id="f6b99-118">**Виспажешдвоффсеткс**</span><span class="sxs-lookup"><span data-stu-id="f6b99-118">**visPageShdwOffsetX**</span></span> <br/> |
   

