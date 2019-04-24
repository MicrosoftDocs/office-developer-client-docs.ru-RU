---
title: VerticalAlign Cell (Text Block Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1105
localization_priority: Normal
ms.assetid: ff34a23b-2881-864f-42e4-871c4fde0992
description: Определяет вертикальное выравнивание текста в блоке текста.
ms.openlocfilehash: 954a0cf0b80d6b675dcc016997f1923041069eac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356143"
---
# <a name="verticalalign-cell-text-block-format-section"></a><span data-ttu-id="dacd4-103">VerticalAlign Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="dacd4-103">VerticalAlign Cell (Text Block Format Section)</span></span>

<span data-ttu-id="dacd4-104">Определяет вертикальное выравнивание текста в блоке текста.</span><span class="sxs-lookup"><span data-stu-id="dacd4-104">Determines the vertical alignment of text within the text block.</span></span>
  
|<span data-ttu-id="dacd4-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="dacd4-105">**Value**</span></span>|<span data-ttu-id="dacd4-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dacd4-106">**Description**</span></span>|<span data-ttu-id="dacd4-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="dacd4-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="dacd4-108">нуль</span><span class="sxs-lookup"><span data-stu-id="dacd4-108">0</span></span>  <br/> | <span data-ttu-id="dacd4-109">Top</span><span class="sxs-lookup"><span data-stu-id="dacd4-109">Top</span></span>  <br/> |<span data-ttu-id="dacd4-110">**Висверттоп**</span><span class="sxs-lookup"><span data-stu-id="dacd4-110">**visVertTop**</span></span> <br/> |
| <span data-ttu-id="dacd4-111">1,1</span><span class="sxs-lookup"><span data-stu-id="dacd4-111">1</span></span>  <br/> | <span data-ttu-id="dacd4-112">Назван</span><span class="sxs-lookup"><span data-stu-id="dacd4-112">Middle</span></span>  <br/> |<span data-ttu-id="dacd4-113">**Висвертмиддле**</span><span class="sxs-lookup"><span data-stu-id="dacd4-113">**visVertMiddle**</span></span> <br/> |
| <span data-ttu-id="dacd4-114">2</span><span class="sxs-lookup"><span data-stu-id="dacd4-114">2</span></span>  <br/> | <span data-ttu-id="dacd4-115">Конец</span><span class="sxs-lookup"><span data-stu-id="dacd4-115">Bottom</span></span>  <br/> |<span data-ttu-id="dacd4-116">**Висвертботтом**</span><span class="sxs-lookup"><span data-stu-id="dacd4-116">**visVertBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dacd4-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="dacd4-117">Remarks</span></span>

<span data-ttu-id="dacd4-118">Чтобы получить ссылку на ячейку VerticalAlign по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="dacd4-118">To get a reference to the VerticalAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dacd4-119">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="dacd4-119">Cell name:</span></span>  <br/> | <span data-ttu-id="dacd4-120">VerticalAlign</span><span class="sxs-lookup"><span data-stu-id="dacd4-120">VerticalAlign</span></span>  <br/> |
   
<span data-ttu-id="dacd4-121">Чтобы получить ссылку на ячейку VerticalAlign по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="dacd4-121">To get a reference to the VerticalAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dacd4-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="dacd4-122">Section index:</span></span>  <br/> |<span data-ttu-id="dacd4-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dacd4-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dacd4-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="dacd4-124">Row index:</span></span>  <br/> |<span data-ttu-id="dacd4-125">**Висровтекст**</span><span class="sxs-lookup"><span data-stu-id="dacd4-125">**visRowText**</span></span> <br/> |
| <span data-ttu-id="dacd4-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="dacd4-126">Cell index:</span></span>  <br/> |<span data-ttu-id="dacd4-127">**Висткстблквертикалалигн**</span><span class="sxs-lookup"><span data-stu-id="dacd4-127">**visTxtBlkVerticalAlign**</span></span> <br/> |
   

