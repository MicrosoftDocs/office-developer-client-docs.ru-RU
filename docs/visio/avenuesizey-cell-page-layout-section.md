---
title: AvenueSizeY Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm70
localization_priority: Normal
ms.assetid: 9ff2893c-afe5-505e-0b55-48ec1de08a5f
description: Определяет объем вертикального пространства между фигурами на странице рисования при разметке фигур с помощью диалоговых окна "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните Re-Layout "Страница" и выберите "Дополнительные параметры макета").
ms.openlocfilehash: 283de8925e34c470fd1f9e78b8ae58882be8b7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420208"
---
# <a name="avenuesizey-cell-page-layout-section"></a><span data-ttu-id="35daa-103">AvenueSizeY Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="35daa-103">AvenueSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="35daa-104">Определяет объем вертикального пространства между фигурами на странице рисования при разметке фигур в диалоговом  окне  "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните "Страница повторного макета" и выберите "Дополнительные параметры   макета"). </span><span class="sxs-lookup"><span data-stu-id="35daa-104">Determines the amount of vertical space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="35daa-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="35daa-105">Remarks</span></span>

<span data-ttu-id="35daa-106">Это значение также можно  установить в диалоговом окне "Макет" и "Интервал маршрутов" (на  вкладке "Конструктор" щелкните стрелку в группе "Настройка страницы", выберите вкладку "Макет" и "Маршрут" и щелкните   "Интервал"). </span><span class="sxs-lookup"><span data-stu-id="35daa-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="35daa-107">Динамическая сетка использует параметр в ячейке AvenueSizeY, если для вычисления интервала по вертикали доступна только одна фигура.</span><span class="sxs-lookup"><span data-stu-id="35daa-107">The dynamic grid uses the setting in the AvenueSizeY cell when only one shape is available for calculating vertical spacing.</span></span> <span data-ttu-id="35daa-108">Чтобы использовать динамическую сетку, на  вкладке **"Вид"** в группе "Визуальные средства" выберите **"Динамическая сетка".**</span><span class="sxs-lookup"><span data-stu-id="35daa-108">To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="35daa-109">Чтобы получить ссылку на ячейку AvenueSizeY по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="35daa-109">To get a reference to the AvenueSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="35daa-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="35daa-110">Cell name:</span></span>  <br/> | <span data-ttu-id="35daa-111">AvenueSizeY</span><span class="sxs-lookup"><span data-stu-id="35daa-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="35daa-112">Чтобы получить ссылку на ячейку AvenueSizeY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="35daa-112">To get a reference to the AvenueSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="35daa-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="35daa-113">Section index:</span></span>  <br/> |<span data-ttu-id="35daa-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="35daa-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="35daa-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="35daa-115">Row index:</span></span>  <br/> |<span data-ttu-id="35daa-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="35daa-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="35daa-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="35daa-117">Cell index:</span></span>  <br/> |<span data-ttu-id="35daa-118">**visPLOAvenueSizeY**</span><span class="sxs-lookup"><span data-stu-id="35daa-118">**visPLOAvenueSizeY**</span></span> <br/> |
   

