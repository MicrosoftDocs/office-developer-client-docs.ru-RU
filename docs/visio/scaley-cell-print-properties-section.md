---
title: ScaleY Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
localization_priority: Normal
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: Указывает процентное отношение увеличения страницы документа на странице принтера.
ms.openlocfilehash: 0f8e86675a039002b60438eac7df92f4a2b13b98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406992"
---
# <a name="scaley-cell-print-properties-section"></a><span data-ttu-id="e656c-103">ScaleY Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="e656c-103">ScaleY Cell (Print Properties Section)</span></span>

<span data-ttu-id="e656c-104">Указывает процентное отношение увеличения страницы документа на странице принтера.</span><span class="sxs-lookup"><span data-stu-id="e656c-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e656c-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="e656c-105">Remarks</span></span>

<span data-ttu-id="e656c-106">Это значение используется только в том случае, если ячейка onPage имеет значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="e656c-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="e656c-107">Ячейки ScaleX и Scale всегда имеют одинаковое значение, которое соответствует значению, указанному в параметре **изменить** на вкладке **Настройка печати** в диалоговом окне **Параметры страницы** (на вкладке **конструктор** щелкните стрелку **настройки страницы** ).</span><span class="sxs-lookup"><span data-stu-id="e656c-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="e656c-108">Чтобы получить ссылку на ячейку масштабирования по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="e656c-108">To get a reference to the ScaleY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e656c-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e656c-109">Cell name:</span></span>  <br/> |<span data-ttu-id="e656c-110">ScaleY</span><span class="sxs-lookup"><span data-stu-id="e656c-110">ScaleY</span></span>  <br/> |
   
<span data-ttu-id="e656c-111">Чтобы получить ссылку на ячейку масштабирования по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e656c-111">To get a reference to the ScaleY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e656c-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e656c-112">Section index:</span></span>  <br/> |<span data-ttu-id="e656c-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e656c-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e656c-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e656c-114">Row index:</span></span>  <br/> |<span data-ttu-id="e656c-115">**Висровпринтпропертиес**</span><span class="sxs-lookup"><span data-stu-id="e656c-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="e656c-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e656c-116">Cell index:</span></span>  <br/> |<span data-ttu-id="e656c-117">**Виспринтпропертиесскалэй**</span><span class="sxs-lookup"><span data-stu-id="e656c-117">**visPrintPropertiesScaleY**</span></span> <br/> |
   

