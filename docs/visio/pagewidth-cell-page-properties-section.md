---
title: PageWidth Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251372
localization_priority: Normal
ms.assetid: b98c5bf3-10c8-7299-2836-3906d6a9135d
description: Определяет ширину печатной страницы в единицах документа.
ms.openlocfilehash: 6d887cb4335d2725101db54ba2b1483ccf01cff4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434272"
---
# <a name="pagewidth-cell-page-properties-section"></a><span data-ttu-id="1b116-103">PageWidth Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="1b116-103">PageWidth Cell (Page Properties Section)</span></span>

<span data-ttu-id="1b116-104">Определяет ширину печатной страницы в единицах документа.</span><span class="sxs-lookup"><span data-stu-id="1b116-104">Determines the width of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1b116-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="1b116-105">Remarks</span></span>

<span data-ttu-id="1b116-106">Вы также можете задать ширину страницы на вкладке " **Размер страницы** " диалогового окна **Параметры страницы** (на вкладке **Макет** щелкните стрелку **настройки страницы** ) или вручную измените размер страницы с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="1b116-106">You can also set the page width on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) or by manually resizing the page with the mouse.</span></span> <span data-ttu-id="1b116-107">Для этого перетащите край страницы, удерживая нажатой клавишу CTRL.</span><span class="sxs-lookup"><span data-stu-id="1b116-107">To do this, drag the edge of the page while holding down the CTRL key.</span></span> 
  
<span data-ttu-id="1b116-108">Чтобы получить ссылку на ячейку PageWidth по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="1b116-108">To get a reference to the PageWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b116-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="1b116-109">Cell name:</span></span>  <br/> |<span data-ttu-id="1b116-110">PageWidth</span><span class="sxs-lookup"><span data-stu-id="1b116-110">PageWidth</span></span>  <br/> |
   
<span data-ttu-id="1b116-111">Чтобы получить ссылку на ячейку PageWidth по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="1b116-111">To get a reference to the PageWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b116-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="1b116-112">Section index:</span></span>  <br/> |<span data-ttu-id="1b116-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1b116-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1b116-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="1b116-114">Row index:</span></span>  <br/> |<span data-ttu-id="1b116-115">**Висровпаже**</span><span class="sxs-lookup"><span data-stu-id="1b116-115">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="1b116-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="1b116-116">Cell index:</span></span>  <br/> |<span data-ttu-id="1b116-117">**Виспажевидс**</span><span class="sxs-lookup"><span data-stu-id="1b116-117">**visPageWidth**</span></span> <br/> |
   

