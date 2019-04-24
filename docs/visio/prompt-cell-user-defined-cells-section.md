---
title: Prompt Cell (User-Defined Cells Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm840
localization_priority: Normal
ms.assetid: d0f91e7d-2373-cfef-e105-fb17e77c7f2d
description: Задает описательное приглашение или комментарий для пользовательской ячейки. Приложение автоматически заключает текст подсказки в кавычки (), указывая, что это текстовая строка. Если ввести знак равенства (=) и опустить кавычки, в этой ячейке можно ввести формулу, оцениваемую приложением.
ms.openlocfilehash: 7684025e03bd3f4f68893179b1df00cc0cb535e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326889"
---
# <a name="prompt-cell-user-defined-cells-section"></a><span data-ttu-id="bd0ef-105">Prompt Cell (User-Defined Cells Section)</span><span class="sxs-lookup"><span data-stu-id="bd0ef-105">Prompt Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="bd0ef-106">Задает описательное приглашение или комментарий для пользовательской ячейки.</span><span class="sxs-lookup"><span data-stu-id="bd0ef-106">Specifies a descriptive prompt or comment for the user-defined cell.</span></span> <span data-ttu-id="bd0ef-107">Приложение автоматически заключает текст подсказки в кавычки (""), чтобы указать, что это текстовая строка.</span><span class="sxs-lookup"><span data-stu-id="bd0ef-107">The application automatically encloses the prompt text in quotation marks (" ") to indicate that it is a text string.</span></span> <span data-ttu-id="bd0ef-108">Если ввести знак равенства (=) и опустить кавычки, в этой ячейке можно ввести формулу, оцениваемую приложением.</span><span class="sxs-lookup"><span data-stu-id="bd0ef-108">If you type an equal sign (=) and omit the quotation marks, you can enter a formula in this cell that the application evaluates.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bd0ef-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="bd0ef-109">Remarks</span></span>

<span data-ttu-id="bd0ef-110">Чтобы получить ссылку на ячейку приглашения по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="bd0ef-110">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd0ef-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="bd0ef-111">Cell name:</span></span>  <br/> | <span data-ttu-id="bd0ef-112">Пользователем.</span><span class="sxs-lookup"><span data-stu-id="bd0ef-112">User.</span></span>  <span data-ttu-id="bd0ef-113">*Name (имя* ). ПодСказка для пользователя.</span><span class="sxs-lookup"><span data-stu-id="bd0ef-113">*Name*  .Prompt            where User.</span></span>  <span data-ttu-id="bd0ef-114">*Name* — имя строки</span><span class="sxs-lookup"><span data-stu-id="bd0ef-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="bd0ef-115">Чтобы получить ссылку на ячейку приглашения по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="bd0ef-115">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd0ef-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="bd0ef-116">Section index:</span></span>  <br/> |<span data-ttu-id="bd0ef-117">**Виссектионусер**</span><span class="sxs-lookup"><span data-stu-id="bd0ef-117">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="bd0ef-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="bd0ef-118">Row index:</span></span>  <br/> |<span data-ttu-id="bd0ef-119">**висровусер +** \*\* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bd0ef-119">**visRowUser +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bd0ef-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="bd0ef-120">Cell index:</span></span>  <br/> |<span data-ttu-id="bd0ef-121">**Висусерпромпт**</span><span class="sxs-lookup"><span data-stu-id="bd0ef-121">**visUserPrompt**</span></span> <br/> |
   

