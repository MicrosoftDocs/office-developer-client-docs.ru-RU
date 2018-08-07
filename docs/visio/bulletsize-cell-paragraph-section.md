---
title: Ячейка BulletSize (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033780
localization_priority: Normal
ms.assetid: 6ff5d07b-17e2-f6ca-1860-5d498a9ebf06
description: Указывает размер маркера.
ms.openlocfilehash: e1b6bd1b4535a70bf99b9cd90af3e0d52128da01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813299"
---
# <a name="bulletsize-cell-paragraph-section"></a><span data-ttu-id="37a96-103">Ячейка BulletSize (раздел "Абзац")</span><span class="sxs-lookup"><span data-stu-id="37a96-103">BulletSize Cell (Paragraph Section)</span></span>

<span data-ttu-id="37a96-104">Указывает размер маркера.</span><span class="sxs-lookup"><span data-stu-id="37a96-104">Specifies the size of a bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="37a96-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="37a96-105">Remarks</span></span>

<span data-ttu-id="37a96-106">Это значение можно указать либо встроенные или настраиваемые элементы, как процент или определенного значения.</span><span class="sxs-lookup"><span data-stu-id="37a96-106">This value can be specified for either predefined or custom bullets, as either a percentage or a specific value.</span></span> 
  
<span data-ttu-id="37a96-107">Если значение равно нулю (0), маркер имеет тот же размер шрифта, как и для первого знака абзаца.</span><span class="sxs-lookup"><span data-stu-id="37a96-107">If the value is zero (0), the bullet is the same font size as that of the first character in the paragraph.</span></span> <span data-ttu-id="37a96-108">Если значение равно процент, маркера изменяется в процентном соотношении от размер шрифта первого знака абзаца.</span><span class="sxs-lookup"><span data-stu-id="37a96-108">If the value is a percentage, the bullet is sized as a percentage of the font size of the first character in the paragraph.</span></span> <span data-ttu-id="37a96-109">Отрицательными числами обрабатывается как процентных значений.</span><span class="sxs-lookup"><span data-stu-id="37a96-109">Negative numbers are treated as percentages.</span></span>
  
<span data-ttu-id="37a96-110">Чтобы получить ссылку на ячейку BulletSize по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="37a96-110">To get a reference to the BulletSize cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37a96-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="37a96-111">Cell name:</span></span>  <br/> | <span data-ttu-id="37a96-112">Para.BulletFontSize [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="37a96-112">Para.BulletFontSize[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="37a96-113">Для получения ссылки на ячейки BulletSize по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="37a96-113">To get a reference to the BulletSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37a96-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="37a96-114">Section index:</span></span>  <br/> |<span data-ttu-id="37a96-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="37a96-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="37a96-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="37a96-116">Row index:</span></span>  <br/> |<span data-ttu-id="37a96-117">**visRowParagraph** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="37a96-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="37a96-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="37a96-118">Cell index:</span></span>  <br/> |<span data-ttu-id="37a96-119">**visBulletFontSize**</span><span class="sxs-lookup"><span data-stu-id="37a96-119">**visBulletFontSize**</span></span> <br/> |
   

