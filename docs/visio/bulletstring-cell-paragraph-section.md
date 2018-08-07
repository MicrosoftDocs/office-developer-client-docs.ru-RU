---
title: Ячейка BulletString (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm135
localization_priority: Normal
ms.assetid: 38285824-30ad-0cf2-07cb-0103ab3a415a
description: Позволяет создавать пользовательские стили маркеров.
ms.openlocfilehash: bd55e2c061d8e99e0d9e9fd5d9be459b3daae524
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813325"
---
# <a name="bulletstring-cell-paragraph-section"></a><span data-ttu-id="ef33e-103">Ячейка BulletString (раздел "Абзац")</span><span class="sxs-lookup"><span data-stu-id="ef33e-103">BulletString Cell (Paragraph Section)</span></span>

<span data-ttu-id="ef33e-104">Позволяет создавать пользовательские стили маркеров.</span><span class="sxs-lookup"><span data-stu-id="ef33e-104">Allows you to create a custom bullet style.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ef33e-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="ef33e-105">Remarks</span></span>

<span data-ttu-id="ef33e-106">Укажите стиль как строку (в кавычках).</span><span class="sxs-lookup"><span data-stu-id="ef33e-106">Enter the style as a string (within quotation marks).</span></span> <span data-ttu-id="ef33e-107">Например можно ввести строку «ООО».</span><span class="sxs-lookup"><span data-stu-id="ef33e-107">For example, you could enter the string, "ooo."</span></span>
  
<span data-ttu-id="ef33e-108">Вы может также необходимо задать значение ячейки, щелкнув правой кнопкой мыши фигуру, с указанием **формате**, нажав кнопку **текст**и затем выбрав вкладку **маркеры** .</span><span class="sxs-lookup"><span data-stu-id="ef33e-108">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="ef33e-109">Чтобы получить ссылку на ячейку BulletString по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="ef33e-109">To get a reference to the BulletString cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ef33e-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="ef33e-110">Cell name:</span></span>  <br/> |<span data-ttu-id="ef33e-111">Para.BulletStr [ *i* ] где *i* = < 1 > 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="ef33e-111">Para.BulletStr[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="ef33e-112">Для получения ссылки на ячейки BulletString по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="ef33e-112">To get a reference to the BulletString cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ef33e-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ef33e-113">Section index:</span></span>  <br/> |<span data-ttu-id="ef33e-114">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="ef33e-114">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="ef33e-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ef33e-115">Row index:</span></span>  <br/> |<span data-ttu-id="ef33e-116">**visRowParagraph** +  *i* где *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="ef33e-116">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="ef33e-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ef33e-117">Cell index:</span></span>  <br/> |<span data-ttu-id="ef33e-118">**visBulletString**</span><span class="sxs-lookup"><span data-stu-id="ef33e-118">**visBulletString**</span></span> <br/> |
   

