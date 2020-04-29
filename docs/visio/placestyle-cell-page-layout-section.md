---
title: PlaceStyle Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dcd5a35-bd3d-447f-e4aa-986091d129de
description: Определяет, как фигуры размещаются на странице при разметке фигур с помощью диалогового окна "Настройка макета" (на вкладке Конструктор в группе Макет выберите пункт изменить макет страницы, а затем щелкните Дополнительные параметры макета).
ms.openlocfilehash: b3159b765922d6656d12dd42a377322e4a91fc04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420803"
---
# <a name="placestyle-cell-page-layout-section"></a><span data-ttu-id="d6a00-103">PlaceStyle Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="d6a00-103">PlaceStyle Cell (Page Layout Section)</span></span>

<span data-ttu-id="d6a00-104">Определяет, как фигуры размещаются на странице при разметке фигур с помощью диалогового окна " **Настройка макета** " (на вкладке **конструктор** в группе **Макет** выберите пункт **изменить макет страницы**, а затем щелкните **Дополнительные параметры макета**).</span><span class="sxs-lookup"><span data-stu-id="d6a00-104">Determines how shapes are placed on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d6a00-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="d6a00-105">Remarks</span></span>

<span data-ttu-id="d6a00-106">Значение этой ячейки также можно задать в диалоговом окне " **Настройка макета** ".</span><span class="sxs-lookup"><span data-stu-id="d6a00-106">You can also set the value of this cell in the **Configure Layout** dialog box.</span></span> 
  
<span data-ttu-id="d6a00-107">Чтобы получить ссылку на ячейку PlaceStyle по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="d6a00-107">To get a reference to the PlaceStyle cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6a00-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d6a00-108">Cell name:</span></span>  <br/> |<span data-ttu-id="d6a00-109">PlaceStyle</span><span class="sxs-lookup"><span data-stu-id="d6a00-109">PlaceStyle</span></span>  <br/> |
   
<span data-ttu-id="d6a00-110">Чтобы получить ссылку на ячейку PlaceStyle по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d6a00-110">To get a reference to the PlaceStyle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6a00-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d6a00-111">Section index:</span></span>  <br/> |<span data-ttu-id="d6a00-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d6a00-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d6a00-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d6a00-113">Row index:</span></span>  <br/> |<span data-ttu-id="d6a00-114">**висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="d6a00-114">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="d6a00-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d6a00-115">Cell index:</span></span>  <br/> |<span data-ttu-id="d6a00-116">**висплоплацестиле**</span><span class="sxs-lookup"><span data-stu-id="d6a00-116">**visPLOPlaceStyle**</span></span> <br/> |
   

