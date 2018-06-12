---
title: Ячейка VerticalAlign (раздел формат блока текст)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1105
localization_priority: Normal
ms.assetid: ff34a23b-2881-864f-42e4-871c4fde0992
description: Определяет вертикальное выравнивание текста в блоке текста.
ms.openlocfilehash: cfd34f17eec597c306b69f76929877013b39015e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815145"
---
# <a name="verticalalign-cell-text-block-format-section"></a><span data-ttu-id="8295f-103">Ячейка VerticalAlign (раздел формат блока текст)</span><span class="sxs-lookup"><span data-stu-id="8295f-103">VerticalAlign Cell (Text Block Format Section)</span></span>

<span data-ttu-id="8295f-104">Определяет вертикальное выравнивание текста в блоке текста.</span><span class="sxs-lookup"><span data-stu-id="8295f-104">Determines the vertical alignment of text within the text block.</span></span>
  
|<span data-ttu-id="8295f-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8295f-105">**Value**</span></span>|<span data-ttu-id="8295f-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8295f-106">**Description**</span></span>|<span data-ttu-id="8295f-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="8295f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="8295f-108">0</span><span class="sxs-lookup"><span data-stu-id="8295f-108">0</span></span>  <br/> | <span data-ttu-id="8295f-109">Вверх</span><span class="sxs-lookup"><span data-stu-id="8295f-109">Top</span></span>  <br/> |<span data-ttu-id="8295f-110">**visVertTop**</span><span class="sxs-lookup"><span data-stu-id="8295f-110">**visVertTop**</span></span> <br/> |
| <span data-ttu-id="8295f-111">1</span><span class="sxs-lookup"><span data-stu-id="8295f-111">1</span></span>  <br/> | <span data-ttu-id="8295f-112">Промежуточное</span><span class="sxs-lookup"><span data-stu-id="8295f-112">Middle</span></span>  <br/> |<span data-ttu-id="8295f-113">**visVertMiddle**</span><span class="sxs-lookup"><span data-stu-id="8295f-113">**visVertMiddle**</span></span> <br/> |
| <span data-ttu-id="8295f-114">2</span><span class="sxs-lookup"><span data-stu-id="8295f-114">2</span></span>  <br/> | <span data-ttu-id="8295f-115">Внизу</span><span class="sxs-lookup"><span data-stu-id="8295f-115">Bottom</span></span>  <br/> |<span data-ttu-id="8295f-116">**visVertBottom**</span><span class="sxs-lookup"><span data-stu-id="8295f-116">**visVertBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8295f-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="8295f-117">Remarks</span></span>

<span data-ttu-id="8295f-118">Чтобы получить ссылку на ячейку VerticalAlign по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="8295f-118">To get a reference to the VerticalAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8295f-119">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="8295f-119">Cell name:</span></span>  <br/> | <span data-ttu-id="8295f-120">VerticalAlign</span><span class="sxs-lookup"><span data-stu-id="8295f-120">VerticalAlign</span></span>  <br/> |
   
<span data-ttu-id="8295f-121">Для получения ссылки на ячейки VerticalAlign по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="8295f-121">To get a reference to the VerticalAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8295f-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8295f-122">Section index:</span></span>  <br/> |<span data-ttu-id="8295f-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8295f-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8295f-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8295f-124">Row index:</span></span>  <br/> |<span data-ttu-id="8295f-125">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="8295f-125">**visRowText**</span></span> <br/> |
| <span data-ttu-id="8295f-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8295f-126">Cell index:</span></span>  <br/> |<span data-ttu-id="8295f-127">**visTxtBlkVerticalAlign**</span><span class="sxs-lookup"><span data-stu-id="8295f-127">**visTxtBlkVerticalAlign**</span></span> <br/> |
   

