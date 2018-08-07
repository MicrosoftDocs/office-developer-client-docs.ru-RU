---
title: Ячейка Case (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251250
localization_priority: Normal
ms.assetid: cf063c05-5789-e037-700b-1e70df00e254
description: Определяет регистр текста формы. Все инвестиционные регистре (1) и прописными буквами (2) не изменяйте внешний вид текста, который был введен прописными буквами. Текст должен указываться в строчные буквы для этих параметров для отображения эффекта.
ms.openlocfilehash: 9acd786b6fa38aec42990f1fd942174367f1135e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813324"
---
# <a name="case-cell-character-section"></a><span data-ttu-id="0cb8f-105">Ячейка Case (раздел "Символ")</span><span class="sxs-lookup"><span data-stu-id="0cb8f-105">Case Cell (Character Section)</span></span>

<span data-ttu-id="0cb8f-106">Определяет регистр текста формы.</span><span class="sxs-lookup"><span data-stu-id="0cb8f-106">Determines the case of a shape's text.</span></span> <span data-ttu-id="0cb8f-107">Все инвестиционные регистре (1) и прописными буквами (2) не изменяйте внешний вид текста, который был введен прописными буквами.</span><span class="sxs-lookup"><span data-stu-id="0cb8f-107">All capital (uppercase) letters (1) and initial capital letters (2) do not change the appearance of text that was entered in all capital letters.</span></span> <span data-ttu-id="0cb8f-108">Текст должен указываться в строчные буквы для этих параметров для отображения эффекта.</span><span class="sxs-lookup"><span data-stu-id="0cb8f-108">The text must be entered in lowercase letters for these options to show an effect.</span></span>
  
|<span data-ttu-id="0cb8f-109">**Значение**</span><span class="sxs-lookup"><span data-stu-id="0cb8f-109">**Value**</span></span>|<span data-ttu-id="0cb8f-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0cb8f-110">**Description**</span></span>|<span data-ttu-id="0cb8f-111">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="0cb8f-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="0cb8f-112">0</span><span class="sxs-lookup"><span data-stu-id="0cb8f-112">0</span></span>  <br/> | <span data-ttu-id="0cb8f-113">Обычный case</span><span class="sxs-lookup"><span data-stu-id="0cb8f-113">Normal case</span></span>  <br/> |<span data-ttu-id="0cb8f-114">**visCaseNormal**</span><span class="sxs-lookup"><span data-stu-id="0cb8f-114">**visCaseNormal**</span></span> <br/> |
| <span data-ttu-id="0cb8f-115">1</span><span class="sxs-lookup"><span data-stu-id="0cb8f-115">1</span></span>  <br/> | <span data-ttu-id="0cb8f-116">Все инвестиционные регистре</span><span class="sxs-lookup"><span data-stu-id="0cb8f-116">All capital (uppercase) letters</span></span>  <br/> |<span data-ttu-id="0cb8f-117">**visCaseAllCaps**</span><span class="sxs-lookup"><span data-stu-id="0cb8f-117">**visCaseAllCaps**</span></span> <br/> |
| <span data-ttu-id="0cb8f-118">2</span><span class="sxs-lookup"><span data-stu-id="0cb8f-118">2</span></span>  <br/> | <span data-ttu-id="0cb8f-119">Прописными буквами только</span><span class="sxs-lookup"><span data-stu-id="0cb8f-119">Initial capital letters only</span></span>  <br/> |<span data-ttu-id="0cb8f-120">**visCaseInitialCaps**</span><span class="sxs-lookup"><span data-stu-id="0cb8f-120">**visCaseInitialCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cb8f-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="0cb8f-121">Remarks</span></span>

<span data-ttu-id="0cb8f-122">Для получения ссылки на ячейки вариантов по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0cb8f-122">To get a reference to the Case cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0cb8f-123">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="0cb8f-123">Cell name:</span></span>  <br/> | <span data-ttu-id="0cb8f-124">Char.Case [ *i* ] где *i* = < 1 > 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="0cb8f-124">Char.Case[  *i*  ]            where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="0cb8f-125">Для получения ссылки на ячейки вариантов по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="0cb8f-125">To get a reference to the Case cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0cb8f-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0cb8f-126">Section index:</span></span>  <br/> |<span data-ttu-id="0cb8f-127">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="0cb8f-127">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="0cb8f-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0cb8f-128">Row index:</span></span>  <br/> |<span data-ttu-id="0cb8f-129">**visRowCharacter** +  *i* где *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="0cb8f-129">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="0cb8f-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0cb8f-130">Cell index:</span></span>  <br/> |<span data-ttu-id="0cb8f-131">**visCharacterCase**</span><span class="sxs-lookup"><span data-stu-id="0cb8f-131">**visCharacterCase**</span></span> <br/> |
   

