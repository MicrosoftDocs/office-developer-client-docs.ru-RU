---
title: AvenueSizeX Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm65
localization_priority: Normal
ms.assetid: 86fe25ed-590d-b2f0-5dfe-9746a19c6b04
description: Определяет горизонтальное расстояние между фигурами на странице документа при размещении фигур с помощью диалогового окна "Настройка макета" (на вкладке Конструктор в группе Макет выберите пункт изменить макет страницы, а затем щелкните Дополнительные параметры макета).
ms.openlocfilehash: 28eea2589e34c7793e89e01495eb519b987553a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338824"
---
# <a name="avenuesizex-cell-page-layout-section"></a><span data-ttu-id="dfa89-103">AvenueSizeX Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="dfa89-103">AvenueSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="dfa89-104">Определяет горизонтальное расстояние между фигурами на странице документа при размещении фигур с помощью диалогового окна " **Настройка макета** " (на вкладке **конструктор** в группе **Макет** выберите пункт **изменить макет страницы**, а затем нажмите кнопку \* \* Дополнительно). Параметры макета \* \*).</span><span class="sxs-lookup"><span data-stu-id="dfa89-104">Determines the amount of horizontal space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click \*\* More Layout Options \*\*).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dfa89-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dfa89-105">Remarks</span></span>

<span data-ttu-id="dfa89-106">Вы также можете задать это значение в диалоговом окне **Макет и интервалы маршрутизации** (на вкладке **конструктор** щелкните стрелку в группе **Параметры страницы** , перейдите на вкладку **Макет и маршрутизация** , а затем выберите **интервал**).</span><span class="sxs-lookup"><span data-stu-id="dfa89-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="dfa89-107">Динамическая сетка использует параметр в ячейке AvenueSizeX, когда доступна только одна фигура для вычисления горизонтального интервала.</span><span class="sxs-lookup"><span data-stu-id="dfa89-107">The dynamic grid uses the setting in the AvenueSizeX cell when only one shape is available for calculating horizontal spacing.</span></span> <span data-ttu-id="dfa89-108">Чтобы использовать динамическую сетку, на вкладке **вид** в группе **визуальные подсказки** выберите **Динамическая сетка**.</span><span class="sxs-lookup"><span data-stu-id="dfa89-108">To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="dfa89-109">Чтобы получить ссылку на ячейку AvenueSizeX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="dfa89-109">To get a reference to the AvenueSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dfa89-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="dfa89-110">Cell name:</span></span>  <br/> | <span data-ttu-id="dfa89-111">AvenueSizeY</span><span class="sxs-lookup"><span data-stu-id="dfa89-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="dfa89-112">Чтобы получить ссылку на ячейку AvenueSizeX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="dfa89-112">To get a reference to the AvenueSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dfa89-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="dfa89-113">Section index:</span></span>  <br/> |<span data-ttu-id="dfa89-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dfa89-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dfa89-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="dfa89-115">Row index:</span></span>  <br/> |<span data-ttu-id="dfa89-116">**Висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="dfa89-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="dfa89-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="dfa89-117">Cell index:</span></span>  <br/> |<span data-ttu-id="dfa89-118">**Висплоавенуесизекс**</span><span class="sxs-lookup"><span data-stu-id="dfa89-118">**visPLOAvenueSizeX**</span></span> <br/> |
   

