---
title: Ячейка PlaceStyle (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dcd5a35-bd3d-447f-e4aa-986091d129de
description: Определяет способ расположения на странице при размещении фигур с помощью диалоговое окно Настройка макета (на вкладке конструктор в группе макет нажмите кнопку Изменить расположение и нажмите кнопку Дополнительные параметры расположения).
ms.openlocfilehash: 251bee427c732fe782c85c4991df07a1deb2a4dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814376"
---
# <a name="placestyle-cell-page-layout-section"></a><span data-ttu-id="109f9-103">Ячейка PlaceStyle (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="109f9-103">PlaceStyle Cell (Page Layout Section)</span></span>

<span data-ttu-id="109f9-104">Определяет способ расположения на странице при размещении фигур с помощью диалоговое окно **Настройка макета** (на вкладке **Конструктор** в группе **Макет** нажмите кнопку **Изменить расположение**и нажмите кнопку **Дополнительные параметры расположения**).</span><span class="sxs-lookup"><span data-stu-id="109f9-104">Determines how shapes are placed on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="109f9-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="109f9-105">Remarks</span></span>

<span data-ttu-id="109f9-106">Также можно задать значение данной ячейки в диалоговом окне " **Настройка макета** ".</span><span class="sxs-lookup"><span data-stu-id="109f9-106">You can also set the value of this cell in the **Configure Layout** dialog box.</span></span> 
  
<span data-ttu-id="109f9-107">Чтобы получить ссылку на ячейку PlaceStyle по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="109f9-107">To get a reference to the PlaceStyle cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="109f9-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="109f9-108">Cell name:</span></span>  <br/> |<span data-ttu-id="109f9-109">PlaceStyle</span><span class="sxs-lookup"><span data-stu-id="109f9-109">PlaceStyle</span></span>  <br/> |
   
<span data-ttu-id="109f9-110">Для получения ссылки на ячейки PlaceStyle по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="109f9-110">To get a reference to the PlaceStyle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="109f9-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="109f9-111">Section index:</span></span>  <br/> |<span data-ttu-id="109f9-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="109f9-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="109f9-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="109f9-113">Row index:</span></span>  <br/> |<span data-ttu-id="109f9-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="109f9-114">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="109f9-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="109f9-115">Cell index:</span></span>  <br/> |<span data-ttu-id="109f9-116">**visPLOPlaceStyle**</span><span class="sxs-lookup"><span data-stu-id="109f9-116">**visPLOPlaceStyle**</span></span> <br/> |
   

