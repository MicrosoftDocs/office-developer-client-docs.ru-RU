---
title: PageHeight Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm760
localization_priority: Normal
ms.assetid: 0184814c-2d67-6ad4-e336-5694612e518d
description: Содержит высоту печатной страницы в единицах документа.
ms.openlocfilehash: ac24bee517f29da333a445f276447c1aa682f01c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427082"
---
# <a name="pageheight-cell-page-properties-section"></a><span data-ttu-id="098dd-103">PageHeight Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="098dd-103">PageHeight Cell (Page Properties Section)</span></span>

<span data-ttu-id="098dd-104">Содержит высоту печатной страницы в единицах документа.</span><span class="sxs-lookup"><span data-stu-id="098dd-104">Contains the height of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="098dd-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="098dd-105">Remarks</span></span>

<span data-ttu-id="098dd-106">Можно также задать высоту страницы на вкладке " **Размер страницы** " диалогового окна **Параметры страницы** (на вкладке **Макет** щелкните стрелку **Параметры страницы** ) или вручную измените размер страницы с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="098dd-106">You can also set the page height on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow), or by manually resizing the page with the mouse.</span></span> 
  
<span data-ttu-id="098dd-107">Чтобы получить ссылку на ячейку PageHeight по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="098dd-107">To get a reference to the PageHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="098dd-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="098dd-108">Cell name:</span></span>  <br/> |<span data-ttu-id="098dd-109">PageHeight</span><span class="sxs-lookup"><span data-stu-id="098dd-109">PageHeight</span></span>  <br/> |
   
<span data-ttu-id="098dd-110">Чтобы получить ссылку на ячейку PageHeight по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="098dd-110">To get a reference to the PageHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="098dd-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="098dd-111">Section index:</span></span>  <br/> |<span data-ttu-id="098dd-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="098dd-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="098dd-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="098dd-113">Row index:</span></span>  <br/> |<span data-ttu-id="098dd-114">**висровпаже**</span><span class="sxs-lookup"><span data-stu-id="098dd-114">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="098dd-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="098dd-115">Cell index:</span></span>  <br/> |<span data-ttu-id="098dd-116">**виспажехеигхт**</span><span class="sxs-lookup"><span data-stu-id="098dd-116">**visPageHeight**</span></span> <br/> |
   

