---
title: Ячейка BlockSizeY (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm110
localization_priority: Normal
ms.assetid: be51e18e-ea49-0788-1a17-866090afb9f4
description: Определяет размер вертикального блока должна помещаться область, в которой каждый фигур на странице документа при расположении фигур с помощью диалогового окна "Настройка макета" (на вкладке конструктор в группе макет нажмите кнопку Изменить расположение и нажмите кнопку Дополнительные параметры расположения).
ms.openlocfilehash: 283723bf902c07cfb044ab73107491df3c170a4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813290"
---
# <a name="blocksizey-cell-page-layout-section"></a><span data-ttu-id="27e28-103">Ячейка BlockSizeY (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="27e28-103">BlockSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="27e28-104">Определяет размер вертикального блока должна помещаться область, в которой каждый фигур на странице документа при расположении фигур с помощью диалогового окна " **Настройка макета** " (на вкладке **Конструктор** в группе **Макет** выберите **Изменить расположение** и нажмите кнопку **Дополнительные параметры расположения**).</span><span class="sxs-lookup"><span data-stu-id="27e28-104">Determines the vertical block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="27e28-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="27e28-105">Remarks</span></span>

<span data-ttu-id="27e28-106">Также можно задать это значение в диалоговом окне **Макет и маршрутизация интервалы** (на вкладку **Конструктор** , щелкните стрелку в группе **Параметры страницы** , перейдите на вкладку **Макет и маршрутизации** и нажмите кнопку **интервала**).</span><span class="sxs-lookup"><span data-stu-id="27e28-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="27e28-107">Чтобы получить ссылку на ячейку BlockSizeY по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="27e28-107">To get a reference to the BlockSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="27e28-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="27e28-108">Cell name:</span></span>  <br/> | <span data-ttu-id="27e28-109">BlockSizeY</span><span class="sxs-lookup"><span data-stu-id="27e28-109">BlockSizeY</span></span>  <br/> |
   
<span data-ttu-id="27e28-110">Для получения ссылки на ячейки BlockSizeY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="27e28-110">To get a reference to the BlockSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="27e28-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="27e28-111">Section index:</span></span>  <br/> |<span data-ttu-id="27e28-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="27e28-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="27e28-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="27e28-113">Row index:</span></span>  <br/> |<span data-ttu-id="27e28-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="27e28-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="27e28-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="27e28-115">Cell index:</span></span>  <br/> |<span data-ttu-id="27e28-116">**visPLOBlockSizeY**</span><span class="sxs-lookup"><span data-stu-id="27e28-116">**visPLOBlockSizeY**</span></span> <br/> |
   

