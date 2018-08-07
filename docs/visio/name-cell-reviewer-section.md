---
title: Ячейка Name (раздел "Рецензент")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030992
localization_priority: Normal
ms.assetid: be39cd0b-56bf-a070-f5d8-c9a440d81ee2
description: Содержит имя рецензент документа.
ms.openlocfilehash: 6bc1629c51fc4dcb3fe7e2d6576e8f1f096144ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814294"
---
# <a name="name-cell-reviewer-section"></a><span data-ttu-id="4ee45-103">Ячейка Name (раздел "Рецензент")</span><span class="sxs-lookup"><span data-stu-id="4ee45-103">Name Cell (Reviewer Section)</span></span>

<span data-ttu-id="4ee45-104">Содержит имя рецензент документа.</span><span class="sxs-lookup"><span data-stu-id="4ee45-104">Contains the name of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4ee45-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="4ee45-105">Remarks</span></span>

 <span data-ttu-id="4ee45-106">Значение по умолчанию на имя в поле **имя пользователя** на вкладке **Общие** диалогового окна **Параметры Visio** (перейдите на вкладку **файл** , нажмите кнопку **Параметры**и выберите пункт **Общие**).</span><span class="sxs-lookup"><span data-stu-id="4ee45-106">This value defaults to the name found in the **User name** box on the **General** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General**).</span></span> 
  
<span data-ttu-id="4ee45-107">Чтобы получить ссылку на имя ячейки по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="4ee45-107">To get a reference to the Name cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4ee45-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="4ee45-108">Cell name:</span></span>  <br/> | <span data-ttu-id="4ee45-109">Reviewer.Name [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4ee45-109">Reviewer.Name [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4ee45-110">Чтобы получить ссылку на имя ячейки по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="4ee45-110">To get a reference to the Name cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4ee45-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4ee45-111">Section index:</span></span>  <br/> |<span data-ttu-id="4ee45-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="4ee45-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="4ee45-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4ee45-113">Row index:</span></span>  <br/> |<span data-ttu-id="4ee45-114">**visRowReviewer** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4ee45-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4ee45-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4ee45-115">Cell index:</span></span>  <br/> |<span data-ttu-id="4ee45-116">**visReviewerName**</span><span class="sxs-lookup"><span data-stu-id="4ee45-116">**visReviewerName**</span></span> <br/> |
   

