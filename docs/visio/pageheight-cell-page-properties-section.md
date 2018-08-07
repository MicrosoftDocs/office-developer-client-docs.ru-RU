---
title: Ячейка PageHeight (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm760
localization_priority: Normal
ms.assetid: 0184814c-2d67-6ad4-e336-5694612e518d
description: Содержит высоту печатной страницы в единицах документа.
ms.openlocfilehash: e198e90e9c70aad1e41ee02d5dcefea68846486c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814332"
---
# <a name="pageheight-cell-page-properties-section"></a><span data-ttu-id="172c1-103">Ячейка PageHeight (раздел "Свойства страницы")</span><span class="sxs-lookup"><span data-stu-id="172c1-103">PageHeight Cell (Page Properties Section)</span></span>

<span data-ttu-id="172c1-104">Содержит высоту печатной страницы в единицах документа.</span><span class="sxs-lookup"><span data-stu-id="172c1-104">Contains the height of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="172c1-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="172c1-105">Remarks</span></span>

<span data-ttu-id="172c1-106">Высота страницы также можно настроить на вкладке **Размер страницы** диалогового окна **Параметры страницы** (на вкладки " **Конструктор** ", нажмите стрелку **Параметры страницы** ), или вручную изменения размеров страницы с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="172c1-106">You can also set the page height on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow), or by manually resizing the page with the mouse.</span></span> 
  
<span data-ttu-id="172c1-107">Для получения ссылки на ячейки PageHeight по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="172c1-107">To get a reference to the PageHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="172c1-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="172c1-108">Cell name:</span></span>  <br/> |<span data-ttu-id="172c1-109">PageHeight</span><span class="sxs-lookup"><span data-stu-id="172c1-109">PageHeight</span></span>  <br/> |
   
<span data-ttu-id="172c1-110">Для получения ссылки на ячейки PageHeight по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="172c1-110">To get a reference to the PageHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="172c1-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="172c1-111">Section index:</span></span>  <br/> |<span data-ttu-id="172c1-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="172c1-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="172c1-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="172c1-113">Row index:</span></span>  <br/> |<span data-ttu-id="172c1-114">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="172c1-114">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="172c1-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="172c1-115">Cell index:</span></span>  <br/> |<span data-ttu-id="172c1-116">**visPageHeight**</span><span class="sxs-lookup"><span data-stu-id="172c1-116">**visPageHeight**</span></span> <br/> |
   

