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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425794"
---
# <a name="verticalalign-cell-text-block-format-section"></a><span data-ttu-id="a01a3-103">VerticalAlign Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="a01a3-103">VerticalAlign Cell (Text Block Format Section)</span></span>

<span data-ttu-id="a01a3-104">Определяет вертикальное выравнивание текста в блоке текста.</span><span class="sxs-lookup"><span data-stu-id="a01a3-104">Determines the vertical alignment of text within the text block.</span></span>
  
|<span data-ttu-id="a01a3-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a01a3-105">**Value**</span></span>|<span data-ttu-id="a01a3-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a01a3-106">**Description**</span></span>|<span data-ttu-id="a01a3-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="a01a3-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="a01a3-108">нуль</span><span class="sxs-lookup"><span data-stu-id="a01a3-108">0</span></span>  <br/> | <span data-ttu-id="a01a3-109">Top</span><span class="sxs-lookup"><span data-stu-id="a01a3-109">Top</span></span>  <br/> |<span data-ttu-id="a01a3-110">**Висверттоп**</span><span class="sxs-lookup"><span data-stu-id="a01a3-110">**visVertTop**</span></span> <br/> |
| <span data-ttu-id="a01a3-111">1,1</span><span class="sxs-lookup"><span data-stu-id="a01a3-111">1</span></span>  <br/> | <span data-ttu-id="a01a3-112">Назван</span><span class="sxs-lookup"><span data-stu-id="a01a3-112">Middle</span></span>  <br/> |<span data-ttu-id="a01a3-113">**Висвертмиддле**</span><span class="sxs-lookup"><span data-stu-id="a01a3-113">**visVertMiddle**</span></span> <br/> |
| <span data-ttu-id="a01a3-114">2</span><span class="sxs-lookup"><span data-stu-id="a01a3-114">2</span></span>  <br/> | <span data-ttu-id="a01a3-115">Конец</span><span class="sxs-lookup"><span data-stu-id="a01a3-115">Bottom</span></span>  <br/> |<span data-ttu-id="a01a3-116">**Висвертботтом**</span><span class="sxs-lookup"><span data-stu-id="a01a3-116">**visVertBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a01a3-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="a01a3-117">Remarks</span></span>

<span data-ttu-id="a01a3-118">Чтобы получить ссылку на ячейку VerticalAlign по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="a01a3-118">To get a reference to the VerticalAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a01a3-119">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="a01a3-119">Cell name:</span></span>  <br/> | <span data-ttu-id="a01a3-120">VerticalAlign</span><span class="sxs-lookup"><span data-stu-id="a01a3-120">VerticalAlign</span></span>  <br/> |
   
<span data-ttu-id="a01a3-121">Чтобы получить ссылку на ячейку VerticalAlign по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="a01a3-121">To get a reference to the VerticalAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a01a3-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a01a3-122">Section index:</span></span>  <br/> |<span data-ttu-id="a01a3-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a01a3-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a01a3-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a01a3-124">Row index:</span></span>  <br/> |<span data-ttu-id="a01a3-125">**Висровтекст**</span><span class="sxs-lookup"><span data-stu-id="a01a3-125">**visRowText**</span></span> <br/> |
| <span data-ttu-id="a01a3-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a01a3-126">Cell index:</span></span>  <br/> |<span data-ttu-id="a01a3-127">**Висткстблквертикалалигн**</span><span class="sxs-lookup"><span data-stu-id="a01a3-127">**visTxtBlkVerticalAlign**</span></span> <br/> |
   

