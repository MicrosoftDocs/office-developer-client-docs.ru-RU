---
title: PaperSource Cell (PrintProperties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60068
localization_priority: Normal
ms.assetid: 771a2ab4-578d-51c3-fabd-138f7952bb11
description: Определяет источник бумаги для страницы.
ms.openlocfilehash: eb6e7daccb1743c43a30b34598e47187496e4aac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406761"
---
# <a name="papersource-cell-printproperties-section"></a><span data-ttu-id="acfdc-103">PaperSource Cell (PrintProperties Section)</span><span class="sxs-lookup"><span data-stu-id="acfdc-103">PaperSource Cell (PrintProperties Section)</span></span>

<span data-ttu-id="acfdc-104">Определяет источник бумаги для страницы.</span><span class="sxs-lookup"><span data-stu-id="acfdc-104">Determines the paper source for the page.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="acfdc-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="acfdc-105">Remarks</span></span>

<span data-ttu-id="acfdc-106">Этот параметр соответствует параметру **источник бумаги** в диалоговом окне " **Настройка печати** " (на вкладке " **конструктор** " щелкните стрелку **Параметры страницы** , а затем на вкладке **Настройка печати** нажмите кнопку **Настройка**).</span><span class="sxs-lookup"><span data-stu-id="acfdc-106">This setting corresponds to the **Paper Source** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click **Setup**).</span></span>
  
<span data-ttu-id="acfdc-107">Числовые значения в этой ячейке сопоставляются с константами (с префиксом ДМБИН), определенными для выбранных ячеек в файле Microsoft Windows вингди. h; Например, значение 7 соответствует DMBIN_AUTO.</span><span class="sxs-lookup"><span data-stu-id="acfdc-107">The numeric values in this cell map to constants (prefixed with DMBIN) defined for bin selections in the Microsoft Windows wingdi.h file; for example, the value 7 represents DMBIN_AUTO.</span></span> 
  
<span data-ttu-id="acfdc-108">Чтобы получить ссылку на ячейку PaperSource по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="acfdc-108">To get a reference to the PaperSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="acfdc-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="acfdc-109">Cell name:</span></span>  <br/> |<span data-ttu-id="acfdc-110">PaperSource</span><span class="sxs-lookup"><span data-stu-id="acfdc-110">PaperSource</span></span>  <br/> |
   
<span data-ttu-id="acfdc-111">Чтобы получить ссылку на ячейку PaperSource по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="acfdc-111">To get a reference to the PaperSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="acfdc-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="acfdc-112">Section index:</span></span>  <br/> |<span data-ttu-id="acfdc-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="acfdc-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="acfdc-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="acfdc-114">Row index:</span></span>  <br/> |<span data-ttu-id="acfdc-115">**висровпринтпропертиес**</span><span class="sxs-lookup"><span data-stu-id="acfdc-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="acfdc-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="acfdc-116">Cell index:</span></span>  <br/> |<span data-ttu-id="acfdc-117">**виспринтпропертиеспаперсаурце**</span><span class="sxs-lookup"><span data-stu-id="acfdc-117">**visPrintPropertiesPaperSource**</span></span> <br/> |
   

