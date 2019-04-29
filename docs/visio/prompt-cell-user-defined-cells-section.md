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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435728"
---
# <a name="prompt-cell-user-defined-cells-section"></a><span data-ttu-id="f47a9-105">Prompt Cell (User-Defined Cells Section)</span><span class="sxs-lookup"><span data-stu-id="f47a9-105">Prompt Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="f47a9-106">Задает описательное приглашение или комментарий для пользовательской ячейки.</span><span class="sxs-lookup"><span data-stu-id="f47a9-106">Specifies a descriptive prompt or comment for the user-defined cell.</span></span> <span data-ttu-id="f47a9-107">Приложение автоматически заключает текст подсказки в кавычки (""), чтобы указать, что это текстовая строка.</span><span class="sxs-lookup"><span data-stu-id="f47a9-107">The application automatically encloses the prompt text in quotation marks (" ") to indicate that it is a text string.</span></span> <span data-ttu-id="f47a9-108">Если ввести знак равенства (=) и опустить кавычки, в этой ячейке можно ввести формулу, оцениваемую приложением.</span><span class="sxs-lookup"><span data-stu-id="f47a9-108">If you type an equal sign (=) and omit the quotation marks, you can enter a formula in this cell that the application evaluates.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f47a9-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="f47a9-109">Remarks</span></span>

<span data-ttu-id="f47a9-110">Чтобы получить ссылку на ячейку приглашения по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f47a9-110">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f47a9-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f47a9-111">Cell name:</span></span>  <br/> | <span data-ttu-id="f47a9-112">Пользователем.</span><span class="sxs-lookup"><span data-stu-id="f47a9-112">User.</span></span>  <span data-ttu-id="f47a9-113">*Name (имя* ). ПодСказка для пользователя.</span><span class="sxs-lookup"><span data-stu-id="f47a9-113">*Name*  .Prompt            where User.</span></span>  <span data-ttu-id="f47a9-114">*Name* — имя строки</span><span class="sxs-lookup"><span data-stu-id="f47a9-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="f47a9-115">Чтобы получить ссылку на ячейку приглашения по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f47a9-115">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f47a9-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f47a9-116">Section index:</span></span>  <br/> |<span data-ttu-id="f47a9-117">**Виссектионусер**</span><span class="sxs-lookup"><span data-stu-id="f47a9-117">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="f47a9-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f47a9-118">Row index:</span></span>  <br/> |<span data-ttu-id="f47a9-119">**висровусер +** \*\* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f47a9-119">**visRowUser +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f47a9-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f47a9-120">Cell index:</span></span>  <br/> |<span data-ttu-id="f47a9-121">**Висусерпромпт**</span><span class="sxs-lookup"><span data-stu-id="f47a9-121">**visUserPrompt**</span></span> <br/> |
   

