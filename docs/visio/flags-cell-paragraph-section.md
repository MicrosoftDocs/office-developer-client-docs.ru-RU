---
title: Ячейка Flags (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033782
localization_priority: Normal
ms.assetid: 898bf89d-d00f-9769-a89d-787ef708eca5
description: Указывает, будет ли направление — слева направо или справа налево.
ms.openlocfilehash: b471d08556bedf68ce75595b9c211758297e8352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813764"
---
# <a name="flags-cell-paragraph-section"></a><span data-ttu-id="ef70b-103">Ячейка Flags (раздел "Абзац")</span><span class="sxs-lookup"><span data-stu-id="ef70b-103">Flags Cell (Paragraph Section)</span></span>

<span data-ttu-id="ef70b-104">Указывает, будет ли направление — слева направо или справа налево.</span><span class="sxs-lookup"><span data-stu-id="ef70b-104">Indicates whether the text direction is left to right or right to left.</span></span>
  
|<span data-ttu-id="ef70b-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ef70b-105">**Value**</span></span>|<span data-ttu-id="ef70b-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ef70b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef70b-107">0</span><span class="sxs-lookup"><span data-stu-id="ef70b-107">0</span></span>  <br/> |<span data-ttu-id="ef70b-108">Направление текста слева направо (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="ef70b-108">The text direction is left to right (the default).</span></span>  <br/> |
|<span data-ttu-id="ef70b-109">1</span><span class="sxs-lookup"><span data-stu-id="ef70b-109">1</span></span>  <br/> |<span data-ttu-id="ef70b-110">Направление текста справа налево.</span><span class="sxs-lookup"><span data-stu-id="ef70b-110">The text direction is right to left.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef70b-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="ef70b-111">Remarks</span></span>

<span data-ttu-id="ef70b-112">Значение в этой ячейке соответствует параметру **направление** на вкладке **абзаца** в диалоговое окно " **Text** " (на вкладке **Главная** щелкните стрелку **шрифта** ), которая появляется только в том случае, если язык, который используется сложных сценариев текст был добавлено в диалоговом окне **Языковые параметры Microsoft Office** .</span><span class="sxs-lookup"><span data-stu-id="ef70b-112">The value in this cell corresponds to the **Direction** setting on the **Paragraph** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow), which appears only if a language that uses complex scripts text has been added in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="ef70b-113">(Нажмите кнопку **Пуск**, последовательно выберите пункты **Все программы**, нажмите кнопку **Microsoft Office**, средства **Microsoft Office**и затем выберите **Языковые параметры Microsoft Office**.)</span><span class="sxs-lookup"><span data-stu-id="ef70b-113">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.)</span></span> 
  
<span data-ttu-id="ef70b-114">Для получения ссылки на ячейки флаги по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ef70b-114">To get a reference to the Flags cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ef70b-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="ef70b-115">Cell name:</span></span>  <br/> |<span data-ttu-id="ef70b-116">Para.Flags [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ef70b-116">Para.Flags[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ef70b-117">Для получения ссылки на ячейки флаги по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="ef70b-117">To get a reference to the Flags cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ef70b-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ef70b-118">Section index:</span></span>  <br/> |<span data-ttu-id="ef70b-119">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="ef70b-119">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="ef70b-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ef70b-120">Row index:</span></span>  <br/> |<span data-ttu-id="ef70b-121">**visRowParagraph** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ef70b-121">**visRowParagraph** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="ef70b-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ef70b-122">Cell index:</span></span>  <br/> |<span data-ttu-id="ef70b-123">**visFlags**</span><span class="sxs-lookup"><span data-stu-id="ef70b-123">**visFlags**</span></span> <br/> |
   

