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
description: Определяет код вставленного поля в более ранних версиях Visio, чем Visio 2000.
ms.openlocfilehash: 293451b61def59ccfdf849dc597def9521fd22e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422217"
---
# <a name="uicode-cell-text-fields-section"></a><span data-ttu-id="ec15d-103">UICode Cell (Text Fields Section)</span><span class="sxs-lookup"><span data-stu-id="ec15d-103">UICode Cell (Text Fields Section)</span></span>

<span data-ttu-id="ec15d-104">Определяет код вставленного поля в более ранних версиях Visio, чем Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="ec15d-104">Determines the code of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ec15d-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="ec15d-105">Remarks</span></span>

<span data-ttu-id="ec15d-106">Эта ячейка не отображается в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="ec15d-106">This cell does not appear in the ShapeSheet window.</span></span> <span data-ttu-id="ec15d-107">Используйте эту ячейку, если вам нужно разобраться с проблемами обратной связи, например сохранить документ Visio версии 2000 в формате файлов Visio версии 5,0.</span><span class="sxs-lookup"><span data-stu-id="ec15d-107">Use this cell if you need to deal with backward capability issues, such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="ec15d-108">Чтобы получить ссылку на ячейку UICode по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="ec15d-108">To get a reference to the UICode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ec15d-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ec15d-109">Cell name:</span></span>  <br/> | <span data-ttu-id="ec15d-110">Fields. Уикод [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ec15d-110">Fields.UICod[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ec15d-111">Чтобы получить ссылку на ячейку UICode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ec15d-111">To get a reference to the UICode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ec15d-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ec15d-112">Section index:</span></span>  <br/> |<span data-ttu-id="ec15d-113">**Виссектионтекстфиелд**</span><span class="sxs-lookup"><span data-stu-id="ec15d-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="ec15d-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ec15d-114">Row index:</span></span>  <br/> |<span data-ttu-id="ec15d-115">**висровфиелд** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ec15d-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ec15d-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ec15d-116">Cell index:</span></span>  <br/> |<span data-ttu-id="ec15d-117">**Висфиелдуикоде**</span><span class="sxs-lookup"><span data-stu-id="ec15d-117">**visFieldUICode**</span></span> <br/> |
   

