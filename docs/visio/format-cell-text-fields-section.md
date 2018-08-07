---
title: Ячейка Format (раздел "Текстовые поля")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm400
localization_priority: Normal
ms.assetid: ab937a00-84c2-6c1c-9080-b7c95ead4f63
description: Задает форматирование текстового поля, который является строка, число, дату или время, длительность или currency.
ms.openlocfilehash: 767b658a9431dfab23d2df9bcfa6c83b52f48d75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813818"
---
# <a name="format-cell-text-fields-section"></a><span data-ttu-id="9101f-103">Ячейка Format (раздел "Текстовые поля")</span><span class="sxs-lookup"><span data-stu-id="9101f-103">Format Cell (Text Fields Section)</span></span>

<span data-ttu-id="9101f-104">Задает форматирование текстового поля, который является строка, число, дату или время, длительность или currency.</span><span class="sxs-lookup"><span data-stu-id="9101f-104">Specifies the formatting of a text field that is a string, a number, a date or time, a duration, or a currency.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9101f-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="9101f-105">Remarks</span></span>

<span data-ttu-id="9101f-106">Если значение ячейки типа равно 0, 2, 5, 6 или 7 (строка, номер, дата или время, длительность и валюта, соответственно), укажите формат рисунка, соответствующий типу данных.</span><span class="sxs-lookup"><span data-stu-id="9101f-106">If the value of the Type cell is 0, 2, 5, 6, or 7 (string, number, date or time, duration, or currency, respectively), specify a format picture appropriate for the data type.</span></span> <span data-ttu-id="9101f-107">Например формат рисунка «# #/ 4 UU» форматов номеров в 12.43.</span><span class="sxs-lookup"><span data-stu-id="9101f-107">For example, the format picture "# #/4 UU" formats the number 12.43 in.</span></span> <span data-ttu-id="9101f-108">как 12 2/4 ДЮЙМА.</span><span class="sxs-lookup"><span data-stu-id="9101f-108">as 12 2/4 INCHES.</span></span> <span data-ttu-id="9101f-109">Дополнительные сведения о задании формат рисунка можно [о формате изображений](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="9101f-109">For more information about specifying a format picture, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="9101f-110">Число (тип = 2) может представлять измерением scalar, угол, даты, времени и денежных единиц.</span><span class="sxs-lookup"><span data-stu-id="9101f-110">A number (Type = 2) can represent a dimension, scalar, angle, date, time, or currency.</span></span> <span data-ttu-id="9101f-111">Чтобы убедиться, что ввода номера всегда вычисляется как дата, время или валюты, используйте функцию даты и времени или Квартал в ячейке формат вместо формат рисунка.</span><span class="sxs-lookup"><span data-stu-id="9101f-111">To ensure that an input number is always evaluated as a date, time, or currency, use the DATETIME or CY function in the Format cell instead of a format picture.</span></span>
  
<span data-ttu-id="9101f-112">Для получения ссылки на ячейки формат по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="9101f-112">To get a reference to the Format cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9101f-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="9101f-113">Cell name:</span></span>  <br/> | <span data-ttu-id="9101f-114">Fields.Format [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="9101f-114">Fields.Format[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9101f-115">Для получения ссылки на ячейки формат по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="9101f-115">To get a reference to the Format cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9101f-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9101f-116">Section index:</span></span>  <br/> |<span data-ttu-id="9101f-117">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="9101f-117">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="9101f-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9101f-118">Row index:</span></span>  <br/> |<span data-ttu-id="9101f-119">**visRowField** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9101f-119">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9101f-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9101f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="9101f-121">**visFieldFormat**</span><span class="sxs-lookup"><span data-stu-id="9101f-121">**visFieldFormat**</span></span> <br/> |
   

