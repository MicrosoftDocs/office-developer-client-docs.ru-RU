---
title: OutputFormat Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251617
localization_priority: Normal
ms.assetid: 17238019-c800-5d3a-32f6-fb0008d4e25f
description: Определяет формат вывода для рисунка. Страницы документа обычно форматируются для печати (по умолчанию); Тем не менее, вы можете выбрать другие форматы вывода.
ms.openlocfilehash: 09fa34095772936ab1c6a3025ed1884a533f55e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359286"
---
# <a name="outputformat-cell-document-properties-section"></a><span data-ttu-id="3890d-104">OutputFormat Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="3890d-104">OutputFormat Cell (Document Properties Section)</span></span>

<span data-ttu-id="3890d-105">Определяет формат вывода для рисунка.</span><span class="sxs-lookup"><span data-stu-id="3890d-105">Determines the output format for a drawing.</span></span> <span data-ttu-id="3890d-106">Страницы документа обычно форматируются для печати (по умолчанию); Тем не менее, вы можете выбрать другие форматы вывода.</span><span class="sxs-lookup"><span data-stu-id="3890d-106">Drawing pages are usually formatted for printing (default); however, you can choose other output formats.</span></span>
  
|<span data-ttu-id="3890d-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="3890d-107">**Value**</span></span>|<span data-ttu-id="3890d-108">**Формат вывода**</span><span class="sxs-lookup"><span data-stu-id="3890d-108">**Output format**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3890d-109">нуль</span><span class="sxs-lookup"><span data-stu-id="3890d-109">0</span></span>  <br/> | <span data-ttu-id="3890d-110">Печать (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3890d-110">Printing (default)</span></span>  <br/> |
| <span data-ttu-id="3890d-111">1,1</span><span class="sxs-lookup"><span data-stu-id="3890d-111">1</span></span>  <br/> | <span data-ttu-id="3890d-112">Показ слайдов PowerPoint</span><span class="sxs-lookup"><span data-stu-id="3890d-112">PowerPoint slide show</span></span>  <br/> |
| <span data-ttu-id="3890d-113">2</span><span class="sxs-lookup"><span data-stu-id="3890d-113">2</span></span>  <br/> | <span data-ttu-id="3890d-114">Вывод HTML или GIF</span><span class="sxs-lookup"><span data-stu-id="3890d-114">HTML or GIF output</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3890d-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="3890d-115">Remarks</span></span>

<span data-ttu-id="3890d-116">Чтобы получить ссылку на ячейку OutputFormat по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="3890d-116">To get a reference to the OutputFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3890d-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="3890d-117">Cell name:</span></span>  <br/> | <span data-ttu-id="3890d-118">OutputFormat</span><span class="sxs-lookup"><span data-stu-id="3890d-118">OutputFormat</span></span>  <br/> |
   
<span data-ttu-id="3890d-119">Чтобы получить ссылку на ячейку OutputFormat по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="3890d-119">To get a reference to the OutputFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3890d-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3890d-120">Section index:</span></span>  <br/> |<span data-ttu-id="3890d-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3890d-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3890d-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3890d-122">Row index:</span></span>  <br/> |<span data-ttu-id="3890d-123">**Висровдок**</span><span class="sxs-lookup"><span data-stu-id="3890d-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="3890d-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3890d-124">Cell index:</span></span>  <br/> |<span data-ttu-id="3890d-125">**Висдокаутпутформат**</span><span class="sxs-lookup"><span data-stu-id="3890d-125">**visDocOutputFormat**</span></span> <br/> |
   

