---
title: Value Cell (Text Fields Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1095
localization_priority: Normal
ms.assetid: 3ca662c8-1ce4-89a9-3264-1ba533fcd444
description: Содержит функцию для поля.
ms.openlocfilehash: d5a09dd0d59341125db897484f74addff22328de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430947"
---
# <a name="value-cell-text-fields-section"></a><span data-ttu-id="194f7-103">Value Cell (Text Fields Section)</span><span class="sxs-lookup"><span data-stu-id="194f7-103">Value Cell (Text Fields Section)</span></span>

<span data-ttu-id="194f7-104">Содержит функцию для поля.</span><span class="sxs-lookup"><span data-stu-id="194f7-104">Contains the function for a field.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="194f7-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="194f7-105">Remarks</span></span>

<span data-ttu-id="194f7-106">Значение этой ячейки можно задать с помощью диалогового окна " **поле** " (на вкладке **Вставка** в группе **текст** выберите **поле**).</span><span class="sxs-lookup"><span data-stu-id="194f7-106">You can set the value of this cell using the **Field** dialog box (on the **Insert** tab, in the **Text** group, click **Field**).</span></span>
  
<span data-ttu-id="194f7-107">Чтобы получить ссылку на ячейку значения по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="194f7-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="194f7-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="194f7-108">Cell name:</span></span>  <br/> |<span data-ttu-id="194f7-109">Fields. Value [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="194f7-109">Fields.Value[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="194f7-110">Чтобы получить ссылку на ячейку value по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="194f7-110">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="194f7-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="194f7-111">Section index:</span></span>  <br/> |<span data-ttu-id="194f7-112">**виссектионтекстфиелд**</span><span class="sxs-lookup"><span data-stu-id="194f7-112">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="194f7-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="194f7-113">Row index:</span></span>  <br/> |<span data-ttu-id="194f7-114">**висровфиелд** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="194f7-114">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="194f7-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="194f7-115">Cell index:</span></span>  <br/> |<span data-ttu-id="194f7-116">**висфиелдцелл**</span><span class="sxs-lookup"><span data-stu-id="194f7-116">**visFieldCell**</span></span> <br/> |
   

