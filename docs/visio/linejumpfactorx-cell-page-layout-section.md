---
title: Ячейка LineJumpFactorX (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm545
localization_priority: Normal
ms.assetid: 0649672f-f496-ce80-6dc3-3affc9b6f913
description: Определяет размер строки пересечения на горизонтальную динамических соединители на странице относительно значения ячейки LineToLineX. Значение ячейки можно в диапазоне от 0 до 10, но рекомендуется дробная значения от 0 до 1.
ms.openlocfilehash: fb6205407070485a0e234ee594e84979bca40891
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814074"
---
# <a name="linejumpfactorx-cell-page-layout-section"></a><span data-ttu-id="a726a-104">Ячейка LineJumpFactorX (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="a726a-104">LineJumpFactorX Cell (Page Layout Section)</span></span>

<span data-ttu-id="a726a-105">Определяет размер строки пересечения на горизонтальную динамических соединители на странице относительно значения ячейки LineToLineX.</span><span class="sxs-lookup"><span data-stu-id="a726a-105">Determines the size of line jumps on horizontal dynamic connectors on the page, relative to the value of the LineToLineX cell.</span></span> <span data-ttu-id="a726a-106">Значение ячейки можно в диапазоне от 0 до 10, но рекомендуется дробная значения от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="a726a-106">The value of this cell can range from 0 to 10 but fractional values from 0 to 1 are suggested.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a726a-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="a726a-107">Remarks</span></span>

<span data-ttu-id="a726a-108">Значение ячейки также можно настроить на вкладке **Макет и маршрутизации** в диалоговом окне " **Параметры страницы** " (на вкладки " **Конструктор** ", нажмите кнопку со стрелкой **Параметры страницы** и нажмите кнопку **Макет и маршрутизации**).</span><span class="sxs-lookup"><span data-stu-id="a726a-108">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="a726a-109">Чтобы получить ссылку на ячейку LineJumpFactorX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="a726a-109">To get a reference to the LineJumpFactorX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a726a-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="a726a-110">Cell name:</span></span>  <br/> |<span data-ttu-id="a726a-111">LineJumpFactorX</span><span class="sxs-lookup"><span data-stu-id="a726a-111">LineJumpFactorX</span></span>  <br/> |
   
<span data-ttu-id="a726a-112">Для получения ссылки на ячейки LineJumpFactorX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="a726a-112">To get a reference to the LineJumpFactorX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a726a-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a726a-113">Section index:</span></span>  <br/> |<span data-ttu-id="a726a-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a726a-114">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a726a-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a726a-115">Row index:</span></span>  <br/> |<span data-ttu-id="a726a-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="a726a-116">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="a726a-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a726a-117">Cell index:</span></span>  <br/> |<span data-ttu-id="a726a-118">**visPLOJumpFactorX**</span><span class="sxs-lookup"><span data-stu-id="a726a-118">**visPLOJumpFactorX**</span></span> <br/> |
   

