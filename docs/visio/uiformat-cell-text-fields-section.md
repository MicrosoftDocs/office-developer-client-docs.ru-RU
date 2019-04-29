---
title: UIFormat Cell (Text Fields Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1080
localization_priority: Normal
ms.assetid: 0dddef20-c58e-2306-ab8e-6cac8e159f61
description: Определяет формат вставленного поля в более ранних версиях Visio, чем Visio 2000.
ms.openlocfilehash: 16cefc5f45d6b5f0f677e35bd5d0937d48fb2680
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426368"
---
# <a name="uiformat-cell-text-fields-section"></a><span data-ttu-id="92bd2-103">UIFormat Cell (Text Fields Section)</span><span class="sxs-lookup"><span data-stu-id="92bd2-103">UIFormat Cell (Text Fields Section)</span></span>

<span data-ttu-id="92bd2-104">Определяет формат вставленного поля в более ранних версиях Visio, чем Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="92bd2-104">Determines the format of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="92bd2-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="92bd2-105">Remarks</span></span>

<span data-ttu-id="92bd2-106">Эта ячейка не отображается в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="92bd2-106">This cell does not appear in the ShapeSheet window.</span></span> <span data-ttu-id="92bd2-107">Используйте эту ячейку, если вам нужно разобраться с проблемами обратной связи, например сохранить документ Visio версии 2000 в формате файлов Visio версии 5,0.</span><span class="sxs-lookup"><span data-stu-id="92bd2-107">Use this cell if you need to deal with backward capability issues, such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="92bd2-108">Чтобы получить ссылку на ячейку UIFormat по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="92bd2-108">To get a reference to the UIFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="92bd2-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="92bd2-109">Cell name:</span></span>  <br/> | <span data-ttu-id="92bd2-110">Fields. Уифмт [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="92bd2-110">Fields.UIFmt[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="92bd2-111">Чтобы получить ссылку на ячейку UIFormat по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="92bd2-111">To get a reference to the UIFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="92bd2-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="92bd2-112">Section index:</span></span>  <br/> |<span data-ttu-id="92bd2-113">**Виссектионтекстфиелд**</span><span class="sxs-lookup"><span data-stu-id="92bd2-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="92bd2-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="92bd2-114">Row index:</span></span>  <br/> |<span data-ttu-id="92bd2-115">**висровфиелд** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="92bd2-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="92bd2-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="92bd2-116">Cell index:</span></span>  <br/> |<span data-ttu-id="92bd2-117">**Висфиелдуиформат**</span><span class="sxs-lookup"><span data-stu-id="92bd2-117">**visFieldUIFormat**</span></span> <br/> |
   

