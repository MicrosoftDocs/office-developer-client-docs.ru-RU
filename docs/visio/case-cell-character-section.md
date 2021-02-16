---
title: Case Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251250
localization_priority: Normal
ms.assetid: cf063c05-5789-e037-700b-1e70df00e254
description: Определяет случай текста фигуры. Все заголовочные (верхние) буквы (1) и начальные буквы (2) не изменяют внешний вид текста, введенного во всех заголовных буквах. Чтобы эти параметры вступили в силу, текст должен быть введен в нижнем регистре.
ms.openlocfilehash: 50ceaa1188caded40d36b8837c346fbbba2e14d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434349"
---
# <a name="case-cell-character-section"></a><span data-ttu-id="86a74-105">Case Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="86a74-105">Case Cell (Character Section)</span></span>

<span data-ttu-id="86a74-106">Определяет случай текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="86a74-106">Determines the case of a shape's text.</span></span> <span data-ttu-id="86a74-107">Все заголовочные (верхние) буквы (1) и начальные буквы (2) не изменяют внешний вид текста, введенного во всех заголовных буквах.</span><span class="sxs-lookup"><span data-stu-id="86a74-107">All capital (uppercase) letters (1) and initial capital letters (2) do not change the appearance of text that was entered in all capital letters.</span></span> <span data-ttu-id="86a74-108">Чтобы эти параметры вступили в силу, текст должен быть введен в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="86a74-108">The text must be entered in lowercase letters for these options to show an effect.</span></span>
  
|<span data-ttu-id="86a74-109">**Значение**</span><span class="sxs-lookup"><span data-stu-id="86a74-109">**Value**</span></span>|<span data-ttu-id="86a74-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="86a74-110">**Description**</span></span>|<span data-ttu-id="86a74-111">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="86a74-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="86a74-112">0</span><span class="sxs-lookup"><span data-stu-id="86a74-112">0</span></span>  <br/> | <span data-ttu-id="86a74-113">Обычный случай</span><span class="sxs-lookup"><span data-stu-id="86a74-113">Normal case</span></span>  <br/> |<span data-ttu-id="86a74-114">**visCaseNormal**</span><span class="sxs-lookup"><span data-stu-id="86a74-114">**visCaseNormal**</span></span> <br/> |
| <span data-ttu-id="86a74-115">1 </span><span class="sxs-lookup"><span data-stu-id="86a74-115">1</span></span>  <br/> | <span data-ttu-id="86a74-116">Все буквы в верхнем регистре</span><span class="sxs-lookup"><span data-stu-id="86a74-116">All capital (uppercase) letters</span></span>  <br/> |<span data-ttu-id="86a74-117">**visCaseAllCaps**</span><span class="sxs-lookup"><span data-stu-id="86a74-117">**visCaseAllCaps**</span></span> <br/> |
| <span data-ttu-id="86a74-118">2 </span><span class="sxs-lookup"><span data-stu-id="86a74-118">2</span></span>  <br/> | <span data-ttu-id="86a74-119">Только начальные буквы</span><span class="sxs-lookup"><span data-stu-id="86a74-119">Initial capital letters only</span></span>  <br/> |<span data-ttu-id="86a74-120">**visCaseInitialCaps**</span><span class="sxs-lookup"><span data-stu-id="86a74-120">**visCaseInitialCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86a74-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="86a74-121">Remarks</span></span>

<span data-ttu-id="86a74-122">Чтобы получить ссылку на ячейку Case по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="86a74-122">To get a reference to the Case cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="86a74-123">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="86a74-123">Cell name:</span></span>  <br/> | <span data-ttu-id="86a74-124">Char.Case[  *i*  ] где  *i*  = <1>, 2, 3, ...</span><span class="sxs-lookup"><span data-stu-id="86a74-124">Char.Case[  *i*  ]            where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="86a74-125">Чтобы получить ссылку на ячейку Case по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="86a74-125">To get a reference to the Case cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="86a74-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="86a74-126">Section index:</span></span>  <br/> |<span data-ttu-id="86a74-127">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="86a74-127">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="86a74-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="86a74-128">Row index:</span></span>  <br/> |<span data-ttu-id="86a74-129">**visRowCharacter**  +   *i* где *i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="86a74-129">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="86a74-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="86a74-130">Cell index:</span></span>  <br/> |<span data-ttu-id="86a74-131">**visCharacterCase**</span><span class="sxs-lookup"><span data-stu-id="86a74-131">**visCharacterCase**</span></span> <br/> |
   

