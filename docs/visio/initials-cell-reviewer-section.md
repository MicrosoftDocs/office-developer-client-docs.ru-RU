---
title: Ячейка Initials (раздел "Рецензент")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60045
localization_priority: Normal
ms.assetid: 8f5d34f0-4c4b-5265-83c1-5b86b73d464f
description: Содержит инициалы рецензент документа.
ms.openlocfilehash: 65f0082219c8d6adca55af86c027b2ec5642fb5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813973"
---
# <a name="initials-cell-reviewer-section"></a><span data-ttu-id="6ebf4-103">Ячейка Initials (раздел "Рецензент")</span><span class="sxs-lookup"><span data-stu-id="6ebf4-103">Initials Cell (Reviewer Section)</span></span>

<span data-ttu-id="6ebf4-104">Содержит инициалы рецензент документа.</span><span class="sxs-lookup"><span data-stu-id="6ebf4-104">Contains the initials of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6ebf4-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="6ebf4-105">Remarks</span></span>

<span data-ttu-id="6ebf4-106">Значением по умолчанию инициалы в поле **Инициалы** на вкладке **Общие** диалогового окна **Параметры Visio** (перейдите на вкладку **файл** , нажмите кнопку **Параметры**и выберите пункт **Общие** ).</span><span class="sxs-lookup"><span data-stu-id="6ebf4-106">This value defaults to the initials in the **Initials** box on the **General** tab in the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General** ).</span></span> 
  
<span data-ttu-id="6ebf4-107">Для получения ссылки на ячейки инициалы по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6ebf4-107">To get a reference to the Initials cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6ebf4-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="6ebf4-108">Cell name:</span></span>  <br/> | <span data-ttu-id="6ebf4-109">Reviewer.Initials [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="6ebf4-109">Reviewer.Initials [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6ebf4-110">Для получения ссылки на ячейки инициалы по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="6ebf4-110">To get a reference to the Initials cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6ebf4-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6ebf4-111">Section index:</span></span>  <br/> |<span data-ttu-id="6ebf4-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="6ebf4-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="6ebf4-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6ebf4-113">Row index:</span></span>  <br/> |<span data-ttu-id="6ebf4-114">**visRowReviewer** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6ebf4-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6ebf4-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6ebf4-115">Cell index:</span></span>  <br/> |<span data-ttu-id="6ebf4-116">**visReviewerInitials**</span><span class="sxs-lookup"><span data-stu-id="6ebf4-116">**visReviewerInitials**</span></span> <br/> |
   

