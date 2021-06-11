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
description: Указывает описательный запрос или комментарий для ячейки, определяемой пользователем. Приложение автоматически заключит быстрый текст в кавычках (), чтобы указать, что это строка текста. Если введите равный знак (=) и опустить кавычка, можно ввести формулу в этой ячейке, которую оценивает приложение.
ms.openlocfilehash: 7684025e03bd3f4f68893179b1df00cc0cb535e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435728"
---
# <a name="prompt-cell-user-defined-cells-section"></a><span data-ttu-id="03ef3-105">Prompt Cell (User-Defined Cells Section)</span><span class="sxs-lookup"><span data-stu-id="03ef3-105">Prompt Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="03ef3-106">Указывает описательный запрос или комментарий для ячейки, определяемой пользователем.</span><span class="sxs-lookup"><span data-stu-id="03ef3-106">Specifies a descriptive prompt or comment for the user-defined cell.</span></span> <span data-ttu-id="03ef3-107">Приложение автоматически заключит быстрый текст в кавычках (""), чтобы указать, что это строка текста.</span><span class="sxs-lookup"><span data-stu-id="03ef3-107">The application automatically encloses the prompt text in quotation marks (" ") to indicate that it is a text string.</span></span> <span data-ttu-id="03ef3-108">Если введите равный знак (=) и опустить кавычка, можно ввести формулу в этой ячейке, которую оценивает приложение.</span><span class="sxs-lookup"><span data-stu-id="03ef3-108">If you type an equal sign (=) and omit the quotation marks, you can enter a formula in this cell that the application evaluates.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="03ef3-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="03ef3-109">Remarks</span></span>

<span data-ttu-id="03ef3-110">Чтобы получить ссылку на ячейку Prompt по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="03ef3-110">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="03ef3-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="03ef3-111">Cell name:</span></span>  <br/> | <span data-ttu-id="03ef3-112">Пользователь.</span><span class="sxs-lookup"><span data-stu-id="03ef3-112">User.</span></span>  <span data-ttu-id="03ef3-113">*Имя*  . Подсказка, где пользователь.</span><span class="sxs-lookup"><span data-stu-id="03ef3-113">*Name*  .Prompt            where User.</span></span>  <span data-ttu-id="03ef3-114">*Имя*  — это имя строки</span><span class="sxs-lookup"><span data-stu-id="03ef3-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="03ef3-115">Чтобы получить ссылку на ячейку Prompt по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="03ef3-115">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="03ef3-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="03ef3-116">Section index:</span></span>  <br/> |<span data-ttu-id="03ef3-117">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="03ef3-117">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="03ef3-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="03ef3-118">Row index:</span></span>  <br/> |<span data-ttu-id="03ef3-119">**visRowUser +** *i, где i* = 0, 1, 2... </span><span class="sxs-lookup"><span data-stu-id="03ef3-119">**visRowUser +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="03ef3-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="03ef3-120">Cell index:</span></span>  <br/> |<span data-ttu-id="03ef3-121">**visUserPrompt**</span><span class="sxs-lookup"><span data-stu-id="03ef3-121">**visUserPrompt**</span></span> <br/> |
   

