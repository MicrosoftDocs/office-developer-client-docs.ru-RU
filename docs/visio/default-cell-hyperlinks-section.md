---
title: Default Cell (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251545
localization_priority: Normal
ms.assetid: 0edea0ea-58dd-15da-6d4f-185d40133452
description: Определяет гиперссылки по умолчанию для фигуры или страницы. Установите для этой ячейки значение TRUE, чтобы установить гиперссылки по умолчанию.
ms.openlocfilehash: 9991bd0e241c5dfd4fda65aeff8b6cc203ad3458
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434356"
---
# <a name="default-cell-hyperlinks-section"></a><span data-ttu-id="b4090-104">Default Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="b4090-104">Default Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="b4090-105">Определяет гиперссылки по умолчанию для фигуры или страницы.</span><span class="sxs-lookup"><span data-stu-id="b4090-105">Determines the default hyperlink for a shape or page.</span></span> <span data-ttu-id="b4090-106">Установите для этой ячейки значение TRUE, чтобы установить гиперссылки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b4090-106">Set the value of this cell to TRUE to set a hyperlink as the default.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b4090-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="b4090-107">Remarks</span></span>

<span data-ttu-id="b4090-108">Вы также можете установить гиперссылки по умолчанию, выбрав  фигуру, щелкнув "Гиперссылка" на вкладке "Вставка", выбрав гиперссылки и выбрав "По **умолчанию".** </span><span class="sxs-lookup"><span data-stu-id="b4090-108">You can also set the default hyperlink by selecting a shape, clicking **Hyperlink** on the **Insert** tab, selecting a hyperlink, and then clicking **Default**.</span></span> <span data-ttu-id="b4090-109">Гиперссылка по умолчанию отображается полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="b4090-109">The default hyperlink appears in bold text.</span></span>
  
<span data-ttu-id="b4090-110">Чтобы получить ссылку на ячейку Default по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="b4090-110">To get a reference to the Default cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4090-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b4090-111">Cell name:</span></span>  <br/> |<span data-ttu-id="b4090-112">Гиперссылка.</span><span class="sxs-lookup"><span data-stu-id="b4090-112">Hyperlink.</span></span> <span data-ttu-id="b4090-113">*Name*  . По умолчанию, где гиперссылка.</span><span class="sxs-lookup"><span data-stu-id="b4090-113">*Name*  .Default           where Hyperlink.</span></span> <span data-ttu-id="b4090-114">*Имя*  — это имя строки</span><span class="sxs-lookup"><span data-stu-id="b4090-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="b4090-115">Чтобы получить ссылку на ячейку Default по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b4090-115">To get a reference to the Default cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4090-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b4090-116">Section index:</span></span>  <br/> |<span data-ttu-id="b4090-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="b4090-117">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="b4090-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b4090-118">Row index:</span></span>  <br/> |<span data-ttu-id="b4090-119">**visRow1stHyperlink**  +   *i,* *где i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b4090-119">**visRow1stHyperlink** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="b4090-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b4090-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b4090-121">**visHLinkDefault**</span><span class="sxs-lookup"><span data-stu-id="b4090-121">**visHLinkDefault**</span></span> <br/> |
   

