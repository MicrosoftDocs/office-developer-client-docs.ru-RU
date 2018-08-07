---
title: Ячейка Default (раздел "Гиперссылки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251545
localization_priority: Normal
ms.assetid: 0edea0ea-58dd-15da-6d4f-185d40133452
description: Определяет гиперссылку по умолчанию для фигуры или страницы. Задайте значение в этой ячейке значение TRUE, чтобы установить гиперссылки по умолчанию.
ms.openlocfilehash: a8bfc045559a2c2904ae4a97c489248fb6c446c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813570"
---
# <a name="default-cell-hyperlinks-section"></a><span data-ttu-id="0f310-104">Ячейка Default (раздел "Гиперссылки")</span><span class="sxs-lookup"><span data-stu-id="0f310-104">Default Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="0f310-105">Определяет гиперссылку по умолчанию для фигуры или страницы.</span><span class="sxs-lookup"><span data-stu-id="0f310-105">Determines the default hyperlink for a shape or page.</span></span> <span data-ttu-id="0f310-106">Задайте значение в этой ячейке значение TRUE, чтобы установить гиперссылки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f310-106">Set the value of this cell to TRUE to set a hyperlink as the default.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0f310-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="0f310-107">Remarks</span></span>

<span data-ttu-id="0f310-108">Также можно настроить гиперссылку по умолчанию, выделение фигуры, щелкнув вкладку **Вставка** **гиперссылки** , выбрав гиперссылки и затем выбрав **по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="0f310-108">You can also set the default hyperlink by selecting a shape, clicking **Hyperlink** on the **Insert** tab, selecting a hyperlink, and then clicking **Default**.</span></span> <span data-ttu-id="0f310-109">Ссылка на по умолчанию отображается полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="0f310-109">The default hyperlink appears in bold text.</span></span>
  
<span data-ttu-id="0f310-110">Для получения ссылки на ячейки по умолчанию по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0f310-110">To get a reference to the Default cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0f310-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="0f310-111">Cell name:</span></span>  <br/> |<span data-ttu-id="0f310-112">Гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="0f310-112">Hyperlink.</span></span> <span data-ttu-id="0f310-113">*Имя* . Значение по умолчанию где гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="0f310-113">*Name*  .Default           where Hyperlink.</span></span> <span data-ttu-id="0f310-114">*Имя* — это имя строки</span><span class="sxs-lookup"><span data-stu-id="0f310-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="0f310-115">Для получения ссылки на ячейки по умолчанию по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="0f310-115">To get a reference to the Default cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0f310-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0f310-116">Section index:</span></span>  <br/> |<span data-ttu-id="0f310-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="0f310-117">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="0f310-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0f310-118">Row index:</span></span>  <br/> |<span data-ttu-id="0f310-119">**visRow1stHyperlink** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0f310-119">**visRow1stHyperlink** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="0f310-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0f310-120">Cell index:</span></span>  <br/> |<span data-ttu-id="0f310-121">**visHLinkDefault**</span><span class="sxs-lookup"><span data-stu-id="0f310-121">**visHLinkDefault**</span></span> <br/> |
   

