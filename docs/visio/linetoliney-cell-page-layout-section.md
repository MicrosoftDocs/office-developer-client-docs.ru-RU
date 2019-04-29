---
title: LineToLineY Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm570
localization_priority: Normal
ms.assetid: db9a8232-25c5-7087-2ae9-50470d0cf16e
description: Определяет вертикальный зазор между всеми соединителями на странице документа.
ms.openlocfilehash: e98c3e05ffb1739f9b2739ce4e0ee8012afe2266
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428475"
---
# <a name="linetoliney-cell-page-layout-section"></a><span data-ttu-id="d5948-103">LineToLineY Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="d5948-103">LineToLineY Cell (Page Layout Section)</span></span>

<span data-ttu-id="d5948-104">Определяет вертикальный зазор между всеми соединителями на странице документа.</span><span class="sxs-lookup"><span data-stu-id="d5948-104">Determines the vertical clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d5948-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="d5948-105">Remarks</span></span>

<span data-ttu-id="d5948-106">Значение этой ячейки также можно задать в диалоговом окне **Макет и интервалы маршрутизации** .</span><span class="sxs-lookup"><span data-stu-id="d5948-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="d5948-107">На вкладке **конструктор** щелкните стрелку **Параметры страницы** , выберите **Макет и маршрутизация**, а затем щелкните интервалы. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d5948-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="d5948-108">Чтобы получить ссылку на ячейку LineToLineY по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="d5948-108">To get a reference to the LineToLineY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5948-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d5948-109">Cell name:</span></span>  <br/> |<span data-ttu-id="d5948-110">LineToLineY</span><span class="sxs-lookup"><span data-stu-id="d5948-110">LineToLineY</span></span>  <br/> |
   
<span data-ttu-id="d5948-111">Чтобы получить ссылку на ячейку LineToLineY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d5948-111">To get a reference to the LineToLineY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5948-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d5948-112">Section index:</span></span>  <br/> |<span data-ttu-id="d5948-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d5948-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d5948-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d5948-114">Row index:</span></span>  <br/> |<span data-ttu-id="d5948-115">**Висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="d5948-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="d5948-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d5948-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d5948-117">**Висплолинетолинэй**</span><span class="sxs-lookup"><span data-stu-id="d5948-117">**visPLOLineToLineY**</span></span> <br/> |
   

