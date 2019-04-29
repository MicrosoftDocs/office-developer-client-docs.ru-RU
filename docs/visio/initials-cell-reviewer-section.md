---
title: Initials Cell (Reviewer Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60045
localization_priority: Normal
ms.assetid: 8f5d34f0-4c4b-5265-83c1-5b86b73d464f
description: Содержит инициалы рецензента документов.
ms.openlocfilehash: ddca3697dfcf1f422efacbe395c18f1a6b8ac48c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411507"
---
# <a name="initials-cell-reviewer-section"></a><span data-ttu-id="d317a-103">Initials Cell (Reviewer Section)</span><span class="sxs-lookup"><span data-stu-id="d317a-103">Initials Cell (Reviewer Section)</span></span>

<span data-ttu-id="d317a-104">Содержит инициалы рецензента документов.</span><span class="sxs-lookup"><span data-stu-id="d317a-104">Contains the initials of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d317a-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="d317a-105">Remarks</span></span>

<span data-ttu-id="d317a-106">Это значение по умолчанию задается в поле **инициалы** на вкладке **Общие** диалогового окна **Параметры Visio** (перейдите на вкладку **файл** , щелкните **Параметры**, а затем выберите **Общие** ).</span><span class="sxs-lookup"><span data-stu-id="d317a-106">This value defaults to the initials in the **Initials** box on the **General** tab in the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General** ).</span></span> 
  
<span data-ttu-id="d317a-107">Чтобы получить ссылку на ячейку инициалов по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="d317a-107">To get a reference to the Initials cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d317a-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d317a-108">Cell name:</span></span>  <br/> | <span data-ttu-id="d317a-109">Review. инициалы [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d317a-109">Reviewer.Initials [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d317a-110">Чтобы получить ссылку на ячейку инициалов по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d317a-110">To get a reference to the Initials cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d317a-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d317a-111">Section index:</span></span>  <br/> |<span data-ttu-id="d317a-112">**Виссектионревиевер**</span><span class="sxs-lookup"><span data-stu-id="d317a-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="d317a-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d317a-113">Row index:</span></span>  <br/> |<span data-ttu-id="d317a-114">**висровревиевер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d317a-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d317a-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d317a-115">Cell index:</span></span>  <br/> |<span data-ttu-id="d317a-116">**Висревиеверинитиалс**</span><span class="sxs-lookup"><span data-stu-id="d317a-116">**visReviewerInitials**</span></span> <br/> |
   

