---
title: BulletString Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm135
localization_priority: Normal
ms.assetid: 38285824-30ad-0cf2-07cb-0103ab3a415a
description: Позволяет создавать пользовательские стили маркеров.
ms.openlocfilehash: b7a1d7f845c7b9945670240361a4ac66efa80786
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337564"
---
# <a name="bulletstring-cell-paragraph-section"></a><span data-ttu-id="b7023-103">BulletString Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="b7023-103">BulletString Cell (Paragraph Section)</span></span>

<span data-ttu-id="b7023-104">Позволяет создавать пользовательские стили маркеров.</span><span class="sxs-lookup"><span data-stu-id="b7023-104">Allows you to create a custom bullet style.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b7023-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7023-105">Remarks</span></span>

<span data-ttu-id="b7023-106">Введите стиль в виде строки (в кавычках).</span><span class="sxs-lookup"><span data-stu-id="b7023-106">Enter the style as a string (within quotation marks).</span></span> <span data-ttu-id="b7023-107">Например, можно ввести строку "УО".</span><span class="sxs-lookup"><span data-stu-id="b7023-107">For example, you could enter the string, "ooo."</span></span>
  
<span data-ttu-id="b7023-108">Можно также задать значение этой ячейки, щелкнув фигуру правой кнопкой мыши, выбрав пункт **Формат**, пункт **текст**, а затем выбрав вкладку **маркеры** .</span><span class="sxs-lookup"><span data-stu-id="b7023-108">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="b7023-109">Чтобы получить ссылку на ячейку BulletString по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="b7023-109">To get a reference to the BulletString cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7023-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b7023-110">Cell name:</span></span>  <br/> |<span data-ttu-id="b7023-111">Para. Буллетстр [ *i* ], где *i* = <1>, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="b7023-111">Para.BulletStr[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="b7023-112">Чтобы получить ссылку на ячейку BulletString по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b7023-112">To get a reference to the BulletString cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7023-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b7023-113">Section index:</span></span>  <br/> |<span data-ttu-id="b7023-114">**Виссектионпараграф**</span><span class="sxs-lookup"><span data-stu-id="b7023-114">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="b7023-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b7023-115">Row index:</span></span>  <br/> |<span data-ttu-id="b7023-116">**висровпараграф** +  *i* , где *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="b7023-116">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="b7023-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b7023-117">Cell index:</span></span>  <br/> |<span data-ttu-id="b7023-118">**Висбуллетстринг**</span><span class="sxs-lookup"><span data-stu-id="b7023-118">**visBulletString**</span></span> <br/> |
   

