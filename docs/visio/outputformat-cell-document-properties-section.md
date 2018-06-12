---
title: Ячейка OutputFormat (раздел свойств документа)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251617
localization_priority: Normal
ms.assetid: 17238019-c800-5d3a-32f6-fb0008d4e25f
description: Определяет формат выходных данных для рисунка. Страницы документа обычно форматирования для печати (по умолчанию); Тем не менее вы можете других форматов вывода.
ms.openlocfilehash: 7103fa5c2bc721add3496b7a497989d6632d58f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814321"
---
# <a name="outputformat-cell-document-properties-section"></a><span data-ttu-id="799ac-104">Ячейка OutputFormat (раздел свойств документа)</span><span class="sxs-lookup"><span data-stu-id="799ac-104">OutputFormat Cell (Document Properties Section)</span></span>

<span data-ttu-id="799ac-105">Определяет формат выходных данных для рисунка.</span><span class="sxs-lookup"><span data-stu-id="799ac-105">Determines the output format for a drawing.</span></span> <span data-ttu-id="799ac-106">Страницы документа обычно форматирования для печати (по умолчанию); Тем не менее вы можете других форматов вывода.</span><span class="sxs-lookup"><span data-stu-id="799ac-106">Drawing pages are usually formatted for printing (default); however, you can choose other output formats.</span></span>
  
|<span data-ttu-id="799ac-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="799ac-107">**Value**</span></span>|<span data-ttu-id="799ac-108">**Формат выходных данных**</span><span class="sxs-lookup"><span data-stu-id="799ac-108">**Output format**</span></span>|
|:-----|:-----|
| <span data-ttu-id="799ac-109">0</span><span class="sxs-lookup"><span data-stu-id="799ac-109">0</span></span>  <br/> | <span data-ttu-id="799ac-110">Печать (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="799ac-110">Printing (default)</span></span>  <br/> |
| <span data-ttu-id="799ac-111">1</span><span class="sxs-lookup"><span data-stu-id="799ac-111">1</span></span>  <br/> | <span data-ttu-id="799ac-112">Слайд-шоу PowerPoint</span><span class="sxs-lookup"><span data-stu-id="799ac-112">PowerPoint slide show</span></span>  <br/> |
| <span data-ttu-id="799ac-113">2</span><span class="sxs-lookup"><span data-stu-id="799ac-113">2</span></span>  <br/> | <span data-ttu-id="799ac-114">Выходные данные HTML или GIF</span><span class="sxs-lookup"><span data-stu-id="799ac-114">HTML or GIF output</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="799ac-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="799ac-115">Remarks</span></span>

<span data-ttu-id="799ac-116">Чтобы получить ссылку на ячейку OutputFormat по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="799ac-116">To get a reference to the OutputFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="799ac-117">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="799ac-117">Cell name:</span></span>  <br/> | <span data-ttu-id="799ac-118">OutputFormat</span><span class="sxs-lookup"><span data-stu-id="799ac-118">OutputFormat</span></span>  <br/> |
   
<span data-ttu-id="799ac-119">Для получения ссылки на ячейки OutputFormat по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="799ac-119">To get a reference to the OutputFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="799ac-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="799ac-120">Section index:</span></span>  <br/> |<span data-ttu-id="799ac-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="799ac-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="799ac-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="799ac-122">Row index:</span></span>  <br/> |<span data-ttu-id="799ac-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="799ac-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="799ac-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="799ac-124">Cell index:</span></span>  <br/> |<span data-ttu-id="799ac-125">**visDocOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="799ac-125">**visDocOutputFormat**</span></span> <br/> |
   

