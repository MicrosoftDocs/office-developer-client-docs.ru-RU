---
title: UICategory Cell (Text Fields Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1070
localization_priority: Normal
ms.assetid: 365f7005-ba34-2311-4c5c-16344962fc3f
description: Определяет категорию вставленного поля в версиях Visio более ранних версий, чем Visio 2000.
ms.openlocfilehash: c67ced9e4f731e66bce0589929ac90fb9bb8d67c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434027"
---
# <a name="uicategory-cell-text-fields-section"></a><span data-ttu-id="c6621-103">UICategory Cell (Text Fields Section)</span><span class="sxs-lookup"><span data-stu-id="c6621-103">UICategory Cell (Text Fields Section)</span></span>

<span data-ttu-id="c6621-104">Определяет категорию вставленного поля в версиях Visio более ранних версий, чем Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="c6621-104">Determines the category of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c6621-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="c6621-105">Remarks</span></span>

<span data-ttu-id="c6621-106">Эта ячейка не появляется в окне ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="c6621-106">This cell does not appear in the ShapeSheet window.</span></span> <span data-ttu-id="c6621-107">Используйте эту ячейку, если необходимо решить проблемы с обратной возможностью, например сохранить рисунок Visio версии 2000 в формате файла Visio версии 5.0.</span><span class="sxs-lookup"><span data-stu-id="c6621-107">Use this cell if you need to deal with backward capability issues such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="c6621-108">Чтобы получить ссылку на ячейку UICategory по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="c6621-108">To get a reference to the UICategory cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c6621-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c6621-109">Cell name:</span></span>  <br/> | <span data-ttu-id="c6621-110">Fields.UICat[  *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c6621-110">Fields.UICat[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c6621-111">Чтобы получить ссылку на ячейку UICategory по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c6621-111">To get a reference to the UICategory cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c6621-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c6621-112">Section index:</span></span>  <br/> |<span data-ttu-id="c6621-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="c6621-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="c6621-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c6621-114">Row index:</span></span>  <br/> |<span data-ttu-id="c6621-115">**visRowField**  +   *i,* *где i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c6621-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c6621-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c6621-116">Cell index:</span></span>  <br/> |<span data-ttu-id="c6621-117">**visFieldUICategory**</span><span class="sxs-lookup"><span data-stu-id="c6621-117">**visFieldUICategory**</span></span> <br/> |
   

