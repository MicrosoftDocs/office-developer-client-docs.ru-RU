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
description: Определяет гиперссылку, используемую по умолчанию для фигуры или страницы. ПриСвойте ячейке значение TRUE, чтобы задать гиперссылку по умолчанию.
ms.openlocfilehash: 9991bd0e241c5dfd4fda65aeff8b6cc203ad3458
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360279"
---
# <a name="default-cell-hyperlinks-section"></a><span data-ttu-id="2675c-104">Default Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="2675c-104">Default Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="2675c-105">Определяет гиперссылку, используемую по умолчанию для фигуры или страницы.</span><span class="sxs-lookup"><span data-stu-id="2675c-105">Determines the default hyperlink for a shape or page.</span></span> <span data-ttu-id="2675c-106">ПриСвойте ячейке значение TRUE, чтобы задать гиперссылку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2675c-106">Set the value of this cell to TRUE to set a hyperlink as the default.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2675c-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="2675c-107">Remarks</span></span>

<span data-ttu-id="2675c-108">Вы также можете задать гиперссылку по умолчанию, выбрав фигуру \*\*\*\* , щелкнув элемент гиперссылка на вкладке **Вставка** , выбрав гиперссылку, а затем нажав кнопку **по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="2675c-108">You can also set the default hyperlink by selecting a shape, clicking **Hyperlink** on the **Insert** tab, selecting a hyperlink, and then clicking **Default**.</span></span> <span data-ttu-id="2675c-109">Гиперссылка по умолчанию отображается полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="2675c-109">The default hyperlink appears in bold text.</span></span>
  
<span data-ttu-id="2675c-110">Чтобы получить ссылку на ячейку по умолчанию по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="2675c-110">To get a reference to the Default cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2675c-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="2675c-111">Cell name:</span></span>  <br/> |<span data-ttu-id="2675c-112">Гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="2675c-112">Hyperlink.</span></span> <span data-ttu-id="2675c-113">*Name (имя* ). Гиперссылка, используемая по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2675c-113">*Name*  .Default           where Hyperlink.</span></span> <span data-ttu-id="2675c-114">*Name* — имя строки</span><span class="sxs-lookup"><span data-stu-id="2675c-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="2675c-115">Чтобы получить ссылку на ячейку по умолчанию по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="2675c-115">To get a reference to the Default cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2675c-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2675c-116">Section index:</span></span>  <br/> |<span data-ttu-id="2675c-117">**Виссектионхиперлинк**</span><span class="sxs-lookup"><span data-stu-id="2675c-117">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="2675c-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2675c-118">Row index:</span></span>  <br/> |<span data-ttu-id="2675c-119">**visRow1stHyperlink** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2675c-119">**visRow1stHyperlink** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="2675c-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2675c-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2675c-121">**Вишлинкдефаулт**</span><span class="sxs-lookup"><span data-stu-id="2675c-121">**visHLinkDefault**</span></span> <br/> |
   

