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
description: Определяет количество горизонтального пространства между фигурами на странице рисования при раскладке фигур с помощью диалогового окна Настройка макета (на вкладке Дизайн, в группе Макет, щелкните Re-Layout страницу, а затем нажмите кнопку Дополнительные параметры макета).
ms.openlocfilehash: 28eea2589e34c7793e89e01495eb519b987553a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411647"
---
# <a name="avenuesizex-cell-page-layout-section"></a><span data-ttu-id="e9549-103">AvenueSizeX Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="e9549-103">AvenueSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="e9549-104">Определяет количество горизонтального пространства между фигурами на странице рисования при раскладке фигур с  помощью диалогового окна **Configure Layout** (на вкладке Design, в группе **Макет** щелкните Страницу повторного макета, а затем щелкните \*\* Дополнительные параметры макета \*\*). </span><span class="sxs-lookup"><span data-stu-id="e9549-104">Determines the amount of horizontal space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click \*\* More Layout Options \*\*).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e9549-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="e9549-105">Remarks</span></span>

<span data-ttu-id="e9549-106">Вы также можете установить  это значение в диалоговом окне  Макет и Маршрутинг интервалов (на вкладке Дизайн щелкните стрелку в группе установки страницы, щелкните вкладку Макет и маршрутизацию, а затем щелкните **Spacing).**  </span><span class="sxs-lookup"><span data-stu-id="e9549-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="e9549-107">Динамическая сетка использует параметр в ячейке AvenueSizeX, когда для вычисления горизонтального интервала доступна только одна фигура.</span><span class="sxs-lookup"><span data-stu-id="e9549-107">The dynamic grid uses the setting in the AvenueSizeX cell when only one shape is available for calculating horizontal spacing.</span></span> <span data-ttu-id="e9549-108">Чтобы использовать динамическую сетку, на вкладке **Просмотр** в группе **Visual Aids** выберите **Dynamic Grid**.</span><span class="sxs-lookup"><span data-stu-id="e9549-108">To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="e9549-109">Чтобы получить ссылку на ячейку AvenueSizeX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="e9549-109">To get a reference to the AvenueSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e9549-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e9549-110">Cell name:</span></span>  <br/> | <span data-ttu-id="e9549-111">AvenueSizeY</span><span class="sxs-lookup"><span data-stu-id="e9549-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="e9549-112">Чтобы получить ссылку на ячейку AvenueSizeX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e9549-112">To get a reference to the AvenueSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e9549-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e9549-113">Section index:</span></span>  <br/> |<span data-ttu-id="e9549-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e9549-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e9549-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e9549-115">Row index:</span></span>  <br/> |<span data-ttu-id="e9549-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="e9549-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="e9549-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e9549-117">Cell index:</span></span>  <br/> |<span data-ttu-id="e9549-118">**visPLOAvenueSizeX**</span><span class="sxs-lookup"><span data-stu-id="e9549-118">**visPLOAvenueSizeX**</span></span> <br/> |
   

