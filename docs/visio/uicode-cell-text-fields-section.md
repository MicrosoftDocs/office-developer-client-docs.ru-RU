---
title: UICode Cell (Text Fields Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1075
localization_priority: Normal
ms.assetid: 1d9717c1-4310-0d62-874f-4df77cd81627
description: Определяет код вставленного поля в версиях Visio более ранних версий, чем Visio 2000.
ms.openlocfilehash: 293451b61def59ccfdf849dc597def9521fd22e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422217"
---
# <a name="uicode-cell-text-fields-section"></a><span data-ttu-id="fbbe3-103">UICode Cell (Text Fields Section)</span><span class="sxs-lookup"><span data-stu-id="fbbe3-103">UICode Cell (Text Fields Section)</span></span>

<span data-ttu-id="fbbe3-104">Определяет код вставленного поля в версиях Visio более ранних версий, чем Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="fbbe3-104">Determines the code of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fbbe3-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="fbbe3-105">Remarks</span></span>

<span data-ttu-id="fbbe3-106">Эта ячейка не появляется в окне ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="fbbe3-106">This cell does not appear in the ShapeSheet window.</span></span> <span data-ttu-id="fbbe3-107">Используйте эту ячейку, если необходимо решить проблемы с обратной возможностью, например сохранить рисунок Visio версии 2000 в формате файла Visio версии 5.0.</span><span class="sxs-lookup"><span data-stu-id="fbbe3-107">Use this cell if you need to deal with backward capability issues, such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="fbbe3-108">Чтобы получить ссылку на ячейку UICode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="fbbe3-108">To get a reference to the UICode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fbbe3-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="fbbe3-109">Cell name:</span></span>  <br/> | <span data-ttu-id="fbbe3-110">Fields.UICod[  *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="fbbe3-110">Fields.UICod[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="fbbe3-111">Чтобы получить ссылку на ячейку UICode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="fbbe3-111">To get a reference to the UICode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fbbe3-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fbbe3-112">Section index:</span></span>  <br/> |<span data-ttu-id="fbbe3-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="fbbe3-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="fbbe3-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fbbe3-114">Row index:</span></span>  <br/> |<span data-ttu-id="fbbe3-115">**visRowField**  +   *i,* *где i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fbbe3-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="fbbe3-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fbbe3-116">Cell index:</span></span>  <br/> |<span data-ttu-id="fbbe3-117">**visFieldUICode**</span><span class="sxs-lookup"><span data-stu-id="fbbe3-117">**visFieldUICode**</span></span> <br/> |
   

