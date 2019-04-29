---
title: Name Cell (Reviewer Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030992
localization_priority: Normal
ms.assetid: be39cd0b-56bf-a070-f5d8-c9a440d81ee2
description: Содержит имя рецензента документов.
ms.openlocfilehash: 02f353ab8f2d39cc075211bb13157b93081e9d8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417688"
---
# <a name="name-cell-reviewer-section"></a><span data-ttu-id="a3418-103">Name Cell (Reviewer Section)</span><span class="sxs-lookup"><span data-stu-id="a3418-103">Name Cell (Reviewer Section)</span></span>

<span data-ttu-id="a3418-104">Содержит имя рецензента документов.</span><span class="sxs-lookup"><span data-stu-id="a3418-104">Contains the name of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a3418-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="a3418-105">Remarks</span></span>

 <span data-ttu-id="a3418-106">Это значение по умолчанию равно имени, указанному в поле **имя пользователя** на **вкладке Общие** диалогового **окна Параметры Visio** (перейдите на вкладку **файл** , щелкните **Параметры**, а затем выберите **Общие**).</span><span class="sxs-lookup"><span data-stu-id="a3418-106">This value defaults to the name found in the **User name** box on the **General** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General**).</span></span> 
  
<span data-ttu-id="a3418-107">Чтобы получить ссылку на ячейку Name по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="a3418-107">To get a reference to the Name cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a3418-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="a3418-108">Cell name:</span></span>  <br/> | <span data-ttu-id="a3418-109">Reviewer.Name [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a3418-109">Reviewer.Name [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a3418-110">Чтобы получить ссылку на ячейку Name по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="a3418-110">To get a reference to the Name cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a3418-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a3418-111">Section index:</span></span>  <br/> |<span data-ttu-id="a3418-112">**Виссектионревиевер**</span><span class="sxs-lookup"><span data-stu-id="a3418-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="a3418-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a3418-113">Row index:</span></span>  <br/> |<span data-ttu-id="a3418-114">**висровревиевер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a3418-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a3418-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a3418-115">Cell index:</span></span>  <br/> |<span data-ttu-id="a3418-116">**Висревиевернаме**</span><span class="sxs-lookup"><span data-stu-id="a3418-116">**visReviewerName**</span></span> <br/> |
   

