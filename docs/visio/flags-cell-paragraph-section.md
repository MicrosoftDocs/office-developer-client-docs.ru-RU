---
title: Flags Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033782
localization_priority: Normal
ms.assetid: 898bf89d-d00f-9769-a89d-787ef708eca5
description: Указывает, находится ли текстовое направление слева направо или справа налево.
ms.openlocfilehash: af1e79b13d3d8bab2e7271eb79e68cf931871806
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413117"
---
# <a name="flags-cell-paragraph-section"></a><span data-ttu-id="5a162-103">Flags Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="5a162-103">Flags Cell (Paragraph Section)</span></span>

<span data-ttu-id="5a162-104">Указывает, находится ли текстовое направление слева направо или справа налево.</span><span class="sxs-lookup"><span data-stu-id="5a162-104">Indicates whether the text direction is left to right or right to left.</span></span>
  
|<span data-ttu-id="5a162-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5a162-105">**Value**</span></span>|<span data-ttu-id="5a162-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5a162-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5a162-107">0</span><span class="sxs-lookup"><span data-stu-id="5a162-107">0</span></span>  <br/> |<span data-ttu-id="5a162-108">Текстовое направление слева направо (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="5a162-108">The text direction is left to right (the default).</span></span>  <br/> |
|<span data-ttu-id="5a162-109">1</span><span class="sxs-lookup"><span data-stu-id="5a162-109">1</span></span>  <br/> |<span data-ttu-id="5a162-110">Направление текста справа налево.</span><span class="sxs-lookup"><span data-stu-id="5a162-110">The text direction is right to left.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a162-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="5a162-111">Remarks</span></span>

<span data-ttu-id="5a162-112">Значение в этой ячейке  соответствует параметру Direction на  вкладке **Абзац** в диалоговом окне Текст (на вкладке Home нажмите стрелку **Шрифта),** которая появляется только в том случае, если язык, использующий сложный текст скриптов, был добавлен в диалоговом окне **Microsoft Office Языковые** предпочтения. </span><span class="sxs-lookup"><span data-stu-id="5a162-112">The value in this cell corresponds to the **Direction** setting on the **Paragraph** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow), which appears only if a language that uses complex scripts text has been added in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="5a162-113">(Нажмите **кнопку Начните,** нажмите кнопку Все **программы,** **нажмите Microsoft Office,** **нажмите Microsoft Office Инструменты**, а затем **нажмите кнопку Microsoft Office Языковые предпочтения**.)</span><span class="sxs-lookup"><span data-stu-id="5a162-113">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.)</span></span> 
  
<span data-ttu-id="5a162-114">Чтобы получить ссылку на ячейку Флаги по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="5a162-114">To get a reference to the Flags cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a162-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="5a162-115">Cell name:</span></span>  <br/> |<span data-ttu-id="5a162-116">Para.Flags[i] где *i* = <1>, 2, 3... </span><span class="sxs-lookup"><span data-stu-id="5a162-116">Para.Flags[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5a162-117">Чтобы получить ссылку на ячейку Флаги по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="5a162-117">To get a reference to the Flags cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a162-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5a162-118">Section index:</span></span>  <br/> |<span data-ttu-id="5a162-119">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="5a162-119">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="5a162-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5a162-120">Row index:</span></span>  <br/> |<span data-ttu-id="5a162-121">**visRowParagraph**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="5a162-121">**visRowParagraph** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="5a162-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5a162-122">Cell index:</span></span>  <br/> |<span data-ttu-id="5a162-123">**visFlags**</span><span class="sxs-lookup"><span data-stu-id="5a162-123">**visFlags**</span></span> <br/> |
   

