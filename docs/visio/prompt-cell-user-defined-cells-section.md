---
title: Запрос ячейки (раздел пользовательские ячейки)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm840
localization_priority: Normal
ms.assetid: d0f91e7d-2373-cfef-e105-fb17e77c7f2d
description: Задает описательную подсказку или комментарий для пользовательской ячейки. Приложение автоматически заключает текст подсказки в кавычки (), чтобы указать, что это текстовая строка. Если ввести знак равенства (=) и опустить кавычки, можно ввести формулу в этой ячейке, которое оценивается как приложение.
ms.openlocfilehash: a7f8757af3e324a89f49bf5d19185b7a22173ff5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814503"
---
# <a name="prompt-cell-user-defined-cells-section"></a><span data-ttu-id="bc31b-105">Запрос ячейки (раздел пользовательские ячейки)</span><span class="sxs-lookup"><span data-stu-id="bc31b-105">Prompt Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="bc31b-106">Задает описательную подсказку или комментарий для пользовательской ячейки.</span><span class="sxs-lookup"><span data-stu-id="bc31b-106">Specifies a descriptive prompt or comment for the user-defined cell.</span></span> <span data-ttu-id="bc31b-107">Приложение автоматически заключает текст подсказки в кавычки (» «) для указания текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="bc31b-107">The application automatically encloses the prompt text in quotation marks (" ") to indicate that it is a text string.</span></span> <span data-ttu-id="bc31b-108">Если ввести знак равенства (=) и опустить кавычки, можно ввести формулу в этой ячейке, которое оценивается как приложение.</span><span class="sxs-lookup"><span data-stu-id="bc31b-108">If you type an equal sign (=) and omit the quotation marks, you can enter a formula in this cell that the application evaluates.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bc31b-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="bc31b-109">Remarks</span></span>

<span data-ttu-id="bc31b-110">Для получения ссылки на ячейки приглашениями по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="bc31b-110">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bc31b-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="bc31b-111">Cell name:</span></span>  <br/> | <span data-ttu-id="bc31b-112">Пользователь.</span><span class="sxs-lookup"><span data-stu-id="bc31b-112">User.</span></span>  <span data-ttu-id="bc31b-113">*Имя* . Запрос where пользователя.</span><span class="sxs-lookup"><span data-stu-id="bc31b-113">*Name*  .Prompt            where User.</span></span>  <span data-ttu-id="bc31b-114">*Имя* — это имя строки</span><span class="sxs-lookup"><span data-stu-id="bc31b-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="bc31b-115">Для получения ссылки на ячейки приглашениями по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="bc31b-115">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bc31b-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="bc31b-116">Section index:</span></span>  <br/> |<span data-ttu-id="bc31b-117">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="bc31b-117">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="bc31b-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="bc31b-118">Row index:</span></span>  <br/> |<span data-ttu-id="bc31b-119">**visRowUser +** *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bc31b-119">**visRowUser +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bc31b-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="bc31b-120">Cell index:</span></span>  <br/> |<span data-ttu-id="bc31b-121">**visUserPrompt**</span><span class="sxs-lookup"><span data-stu-id="bc31b-121">**visUserPrompt**</span></span> <br/> |
   

