---
title: Ячейка PageWidth (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251372
localization_priority: Normal
ms.assetid: b98c5bf3-10c8-7299-2836-3906d6a9135d
description: Определяет ширину печатной страницы в единицах документа.
ms.openlocfilehash: e03696c8f1c921c930d3563e9c73ef4ae613a7c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814356"
---
# <a name="pagewidth-cell-page-properties-section"></a><span data-ttu-id="35e07-103">Ячейка PageWidth (раздел "Свойства страницы")</span><span class="sxs-lookup"><span data-stu-id="35e07-103">PageWidth Cell (Page Properties Section)</span></span>

<span data-ttu-id="35e07-104">Определяет ширину печатной страницы в единицах документа.</span><span class="sxs-lookup"><span data-stu-id="35e07-104">Determines the width of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="35e07-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="35e07-105">Remarks</span></span>

<span data-ttu-id="35e07-106">Можно также задать ширину страницы на вкладке **Размер страницы** диалогового окна **Параметры страницы** (на вкладки " **Конструктор** ", нажмите стрелку **Параметры страницы** ) или вручную изменения размеров страницы с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="35e07-106">You can also set the page width on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) or by manually resizing the page with the mouse.</span></span> <span data-ttu-id="35e07-107">Для этого перетащите края страницы, удерживая нажатой клавишу CTRL.</span><span class="sxs-lookup"><span data-stu-id="35e07-107">To do this, drag the edge of the page while holding down the CTRL key.</span></span> 
  
<span data-ttu-id="35e07-108">Для получения ссылки на ячейки PageWidth по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="35e07-108">To get a reference to the PageWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35e07-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="35e07-109">Cell name:</span></span>  <br/> |<span data-ttu-id="35e07-110">PageWidth</span><span class="sxs-lookup"><span data-stu-id="35e07-110">PageWidth</span></span>  <br/> |
   
<span data-ttu-id="35e07-111">Для получения ссылки на ячейки PageWidth по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="35e07-111">To get a reference to the PageWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35e07-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="35e07-112">Section index:</span></span>  <br/> |<span data-ttu-id="35e07-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="35e07-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="35e07-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="35e07-114">Row index:</span></span>  <br/> |<span data-ttu-id="35e07-115">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="35e07-115">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="35e07-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="35e07-116">Cell index:</span></span>  <br/> |<span data-ttu-id="35e07-117">**visPageWidth**</span><span class="sxs-lookup"><span data-stu-id="35e07-117">**visPageWidth**</span></span> <br/> |
   

