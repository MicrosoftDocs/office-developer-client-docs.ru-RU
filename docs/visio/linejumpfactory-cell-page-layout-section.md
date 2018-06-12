---
title: Ячейка LineJumpFactorY (раздел макет страницы)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm550
localization_priority: Normal
ms.assetid: 5a14be0d-9e3c-23c4-7782-bda5470d1243
description: Определяет размер строки пересечения на вертикальной динамической соединители на странице относительно значения ячейки LineToLineY. Значение ячейки можно в диапазоне от 0 до 10, но рекомендуется дробная значения от 0 до 1.
ms.openlocfilehash: deba4c27585644604e7bac1dbfe284bc3977835e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814098"
---
# <a name="linejumpfactory-cell-page-layout-section"></a><span data-ttu-id="8b214-104">Ячейка LineJumpFactorY (раздел макет страницы)</span><span class="sxs-lookup"><span data-stu-id="8b214-104">LineJumpFactorY Cell (Page Layout Section)</span></span>

<span data-ttu-id="8b214-105">Определяет размер строки пересечения на вертикальной динамической соединители на странице относительно значения ячейки LineToLineY.</span><span class="sxs-lookup"><span data-stu-id="8b214-105">Determines the size of line jumps on vertical dynamic connectors on the page, relative to the value of the LineToLineY cell.</span></span> <span data-ttu-id="8b214-106">Значение ячейки можно в диапазоне от 0 до 10, но рекомендуется дробная значения от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="8b214-106">The value of this cell can range from 0 to 10 but fractional values from 0 to 1 are suggested.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8b214-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="8b214-107">Remarks</span></span>

<span data-ttu-id="8b214-108">Значение ячейки также можно настроить на вкладке **Макет и маршрутизации** в диалоговом окне " **Параметры страницы** " (на вкладки " **Конструктор** ", нажмите кнопку со стрелкой **Параметры страницы** и нажмите кнопку **Макет и маршрутизации**).</span><span class="sxs-lookup"><span data-stu-id="8b214-108">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="8b214-109">Чтобы получить ссылку на ячейку LineJumpFactorY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="8b214-109">To get a reference to the LineJumpFactorY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b214-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="8b214-110">Cell name:</span></span>  <br/> |<span data-ttu-id="8b214-111">LineJumpFactorY</span><span class="sxs-lookup"><span data-stu-id="8b214-111">LineJumpFactorY</span></span>  <br/> |
   
<span data-ttu-id="8b214-112">Для получения ссылки на ячейки LineJumpFactorY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="8b214-112">To get a reference to the LineJumpFactorY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b214-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8b214-113">Section index:</span></span>  <br/> |<span data-ttu-id="8b214-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8b214-114">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8b214-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8b214-115">Row index:</span></span>  <br/> |<span data-ttu-id="8b214-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="8b214-116">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="8b214-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8b214-117">Cell index:</span></span>  <br/> |<span data-ttu-id="8b214-118">**visPLOJumpFactorY**</span><span class="sxs-lookup"><span data-stu-id="8b214-118">**visPLOJumpFactorY**</span></span> <br/> |
   

