---
title: Format Cell (Text Fields Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm400
localization_priority: Normal
ms.assetid: ab937a00-84c2-6c1c-9080-b7c95ead4f63
description: Задает форматирование текстового поля, которое является строкой, числом, датой или временем, длительностью или валютой.
ms.openlocfilehash: c1c7fc7e9c699b7642369fbb979c005829b06cb8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431521"
---
# <a name="format-cell-text-fields-section"></a><span data-ttu-id="051c2-103">Format Cell (Text Fields Section)</span><span class="sxs-lookup"><span data-stu-id="051c2-103">Format Cell (Text Fields Section)</span></span>

<span data-ttu-id="051c2-104">Задает форматирование текстового поля, которое является строкой, числом, датой или временем, длительностью или валютой.</span><span class="sxs-lookup"><span data-stu-id="051c2-104">Specifies the formatting of a text field that is a string, a number, a date or time, a duration, or a currency.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="051c2-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="051c2-105">Remarks</span></span>

<span data-ttu-id="051c2-106">Если значение ячейки Type равно 0, 2, 5, 6 или 7 (строка, число, дата или время, продолжительность или валюта соответственно), укажите формат, соответствующий типу данных.</span><span class="sxs-lookup"><span data-stu-id="051c2-106">If the value of the Type cell is 0, 2, 5, 6, or 7 (string, number, date or time, duration, or currency, respectively), specify a format picture appropriate for the data type.</span></span> <span data-ttu-id="051c2-107">Например, рисунок формата "# #/4 UU" форматирует число 12,43 в.</span><span class="sxs-lookup"><span data-stu-id="051c2-107">For example, the format picture "# #/4 UU" formats the number 12.43 in.</span></span> <span data-ttu-id="051c2-108">как 12 2/4 дюймов.</span><span class="sxs-lookup"><span data-stu-id="051c2-108">as 12 2/4 INCHES.</span></span> <span data-ttu-id="051c2-109">Дополнительные сведения о том, как указать формат рисунка, можно узнать в статье [Форматирование рисунков](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="051c2-109">For more information about specifying a format picture, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="051c2-110">Число (Type = 2) может представлять размерность, скалярную величину, угол, дату, время или денежную единицу.</span><span class="sxs-lookup"><span data-stu-id="051c2-110">A number (Type = 2) can represent a dimension, scalar, angle, date, time, or currency.</span></span> <span data-ttu-id="051c2-111">Чтобы гарантировать, что введенный номер всегда вычисляется как дата, время или валюта, используйте функцию DATETIME или CY в ячейке Format вместо формата изображения.</span><span class="sxs-lookup"><span data-stu-id="051c2-111">To ensure that an input number is always evaluated as a date, time, or currency, use the DATETIME or CY function in the Format cell instead of a format picture.</span></span>
  
<span data-ttu-id="051c2-112">Чтобы получить ссылку на ячейку Format по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="051c2-112">To get a reference to the Format cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="051c2-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="051c2-113">Cell name:</span></span>  <br/> | <span data-ttu-id="051c2-114">Fields. Format [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="051c2-114">Fields.Format[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="051c2-115">Чтобы получить ссылку на ячейку Format по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="051c2-115">To get a reference to the Format cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="051c2-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="051c2-116">Section index:</span></span>  <br/> |<span data-ttu-id="051c2-117">**Виссектионтекстфиелд**</span><span class="sxs-lookup"><span data-stu-id="051c2-117">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="051c2-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="051c2-118">Row index:</span></span>  <br/> |<span data-ttu-id="051c2-119">**висровфиелд** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="051c2-119">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="051c2-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="051c2-120">Cell index:</span></span>  <br/> |<span data-ttu-id="051c2-121">**Висфиелдформат**</span><span class="sxs-lookup"><span data-stu-id="051c2-121">**visFieldFormat**</span></span> <br/> |
   

