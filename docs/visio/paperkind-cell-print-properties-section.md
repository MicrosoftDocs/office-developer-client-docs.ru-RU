---
title: PaperKind Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
localization_priority: Normal
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: Определяет тип бумаги, на которой будет печататься страница.
ms.openlocfilehash: 694aa1fb8b52f5ae323c47e9aab8715b4a48dfb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327064"
---
# <a name="paperkind-cell-print-properties-section"></a><span data-ttu-id="41986-103">PaperKind Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="41986-103">PaperKind Cell (Print Properties Section)</span></span>

<span data-ttu-id="41986-104">Определяет тип бумаги, на которой будет печататься страница.</span><span class="sxs-lookup"><span data-stu-id="41986-104">Specifies the type of paper on which to print the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="41986-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="41986-105">Remarks</span></span>

<span data-ttu-id="41986-106">Этот параметр соответствует параметру **Размер бумаги** в диалоговом окне " **Настройка печати** " (на вкладке " **конструктор** " щелкните стрелку **настройки страницы** , а затем на вкладке **Настройка печати** нажмите кнопку **установить** ).</span><span class="sxs-lookup"><span data-stu-id="41986-106">This setting corresponds to the **Paper Size** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click the **Setup** button).</span></span> 
  
<span data-ttu-id="41986-107">Числовые значения в этой ячейке сопоставляются с константами (с префиксом ДМПАПЕР), определенными для выбора бумаги в файле Microsoft Windows вингди. h.</span><span class="sxs-lookup"><span data-stu-id="41986-107">The numeric values in this cell map to constants (prefixed with DMPAPER) defined for paper selections in the Microsoft Windows wingdi.h file.</span></span> 
  
<span data-ttu-id="41986-108">Чтобы получить ссылку на ячейку PaperKind по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="41986-108">To get a reference to the PaperKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41986-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="41986-109">Cell name:</span></span>  <br/> |<span data-ttu-id="41986-110">PaperKind</span><span class="sxs-lookup"><span data-stu-id="41986-110">PaperKind</span></span>  <br/> |
   
<span data-ttu-id="41986-111">Чтобы получить ссылку на ячейку PaperKind по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="41986-111">To get a reference to the PaperKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41986-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="41986-112">Section index:</span></span>  <br/> |<span data-ttu-id="41986-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="41986-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="41986-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="41986-114">Row index:</span></span>  <br/> |<span data-ttu-id="41986-115">**Висровпринтпропертиес**</span><span class="sxs-lookup"><span data-stu-id="41986-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="41986-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="41986-116">Cell index:</span></span>  <br/> |<span data-ttu-id="41986-117">**Виспринтпропертиеспаперкинд**</span><span class="sxs-lookup"><span data-stu-id="41986-117">**visPrintPropertiesPaperKind**</span></span> <br/> |
   

