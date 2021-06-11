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
description: Содержит высоту напечатанной страницы в единицах рисования.
ms.openlocfilehash: ac24bee517f29da333a445f276447c1aa682f01c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427082"
---
# <a name="pageheight-cell-page-properties-section"></a><span data-ttu-id="0e62c-103">PageHeight Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="0e62c-103">PageHeight Cell (Page Properties Section)</span></span>

<span data-ttu-id="0e62c-104">Содержит высоту напечатанной страницы в единицах рисования.</span><span class="sxs-lookup"><span data-stu-id="0e62c-104">Contains the height of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0e62c-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="0e62c-105">Remarks</span></span>

<span data-ttu-id="0e62c-106">Вы также можете установить высоту страницы на  вкладке **Размер** страницы  диалогового окна установки страницы (на вкладке Дизайн, нажмите стрелку **Установки** страницы) или вручную переостановив размер страницы с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="0e62c-106">You can also set the page height on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow), or by manually resizing the page with the mouse.</span></span> 
  
<span data-ttu-id="0e62c-107">Чтобы получить ссылку на ячейку PageHeight по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="0e62c-107">To get a reference to the PageHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e62c-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="0e62c-108">Cell name:</span></span>  <br/> |<span data-ttu-id="0e62c-109">PageHeight</span><span class="sxs-lookup"><span data-stu-id="0e62c-109">PageHeight</span></span>  <br/> |
   
<span data-ttu-id="0e62c-110">Чтобы получить ссылку на ячейку PageHeight по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="0e62c-110">To get a reference to the PageHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e62c-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0e62c-111">Section index:</span></span>  <br/> |<span data-ttu-id="0e62c-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0e62c-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0e62c-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0e62c-113">Row index:</span></span>  <br/> |<span data-ttu-id="0e62c-114">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="0e62c-114">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="0e62c-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0e62c-115">Cell index:</span></span>  <br/> |<span data-ttu-id="0e62c-116">**visPageHeight**</span><span class="sxs-lookup"><span data-stu-id="0e62c-116">**visPageHeight**</span></span> <br/> |
   

