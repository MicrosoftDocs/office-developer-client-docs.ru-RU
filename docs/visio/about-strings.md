---
title: О строках
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251826
localization_priority: Normal
ms.assetid: e1174d8f-70cb-4595-7906-889da15367db
description: 'Формулы могут содержать строки. Для формата вывода строки, например в оперативной ячейке, значении элемента данных фигуры или текстового поля, необходимо указать изображение формата. Вывод может быть отформатирован в виде пары номеров, строки, даты, продолжительности или валюты. Например, форматное изображение0 #/10 uuformats пары number-unit 10.9cm as10 9/10 сантиметров.'
ms.openlocfilehash: aa95e11db387913edbb40292f7da6a0f4b8a5cf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409519"
---
# <a name="about-strings"></a><span data-ttu-id="c7bb6-106">О строках</span><span class="sxs-lookup"><span data-stu-id="c7bb6-106">About Strings</span></span>

<span data-ttu-id="c7bb6-107">Формулы могут содержать строки.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-107">Formulas can contain strings.</span></span> <span data-ttu-id="c7bb6-108">Для формата вывода строки, например в оперативной ячейке, значении элемента данных фигуры или текстового поля, необходимо указать изображение формата.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-108">To format string output, such as in a prompt cell, a shape data item value, or a text field, you specify a format picture.</span></span> <span data-ttu-id="c7bb6-109">Вывод может быть отформатирован в виде пары номеров, строки, даты, продолжительности или валюты.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-109">Output can be formatted as a number-unit pair, string, date-time, duration, or currency.</span></span> <span data-ttu-id="c7bb6-110">Например, форматное изображение "0 #/10 uu" форматов пары number-unit 10.9cm как "10 9/10 сантиметров".</span><span class="sxs-lookup"><span data-stu-id="c7bb6-110">For example, the format picture "0 #/10 uu" formats the number-unit pair 10.9cm as "10 9/10 centimeters".</span></span>
  
<span data-ttu-id="c7bb6-111">Изображения формата можно использовать в ячейке **Format** в разделе Данные фигуры и в качестве аргумента для **функции FORMAT** **ИЛИ FORMATEX.**</span><span class="sxs-lookup"><span data-stu-id="c7bb6-111">You can use format pictures in the **Format** cell of the Shape Data section and as an argument to the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="c7bb6-112">При вставке текстового поля в списке форматов в диалоговом окне **Field** **(вставить** вкладку) отображаются форматные изображения.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-112">When you insert a text field, format pictures appear in the list of formats in the **Field** dialog box (**Insert** tab).</span></span> 
  
## <a name="using-functions-to-format-strings"></a><span data-ttu-id="c7bb6-113">Использование функций для формата строк</span><span class="sxs-lookup"><span data-stu-id="c7bb6-113">Using functions to format strings</span></span>

<span data-ttu-id="c7bb6-114">В любой формуле, разрешаемой строке, включая настраиваемые формулы текстового поля, можно использовать функцию **FORMAT** **или FORMATEX.**</span><span class="sxs-lookup"><span data-stu-id="c7bb6-114">In any formula that resolves to a string, including custom text field formulas, you can use the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="c7bb6-115">Функция FORMAT возвращает строку отформатированного вывода.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-115">The FORMAT function returns a string of the formatted output.</span></span> <span data-ttu-id="c7bb6-116">Функция **FORMATEX** преобразует нетипированный ввод в единицы, которые вы выбираете для форматируемого результата.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-116">The **FORMATEX** function converts untyped input to the units you choose for the formatted result.</span></span> 
  
## <a name="displaying-formatted-shape-data"></a><span data-ttu-id="c7bb6-117">Отображение отформатированные данные фигуры</span><span class="sxs-lookup"><span data-stu-id="c7bb6-117">Displaying formatted shape data</span></span>

<span data-ttu-id="c7bb6-118">Вы можете форматирование отображаемого значения элемента данных фигуры, введите изображение формата в ячейке Format.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-118">You can format the displayed value of a shape data item by entering a format picture in the Format cell.</span></span>
  
<span data-ttu-id="c7bb6-119">Например, форма временной шкалы проекта может иметь элемент данных фигуры, который измеряет стоимость процесса.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-119">For example, a project timeline shape can have a shape data item that measures the cost of a process.</span></span> <span data-ttu-id="c7bb6-120">По умолчанию значение элемента данных фигуры — это строка.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-120">By default, a shape data item value is a string.</span></span> <span data-ttu-id="c7bb6-121">Для формата строки "1200" можно ввести "$#####.00" в ячейке Format, чтобы пользователь увидел валюту.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-121">To format the string "1200", you can enter "$###,###.00" in the Format cell so that the user sees a currency.</span></span>
  
<span data-ttu-id="c7bb6-122">Microsoft Visio использует параметры на вкладке **Currency** в диалоговом  окне **Настройка** формата в элементе Область и язык в панели управления, чтобы определить символ валюты и отобразить тысячи сепараторов.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-122">Microsoft Visio uses the settings on the **Currency** tab in the **Customize Format** dialog box in the **Region and Language** item in Control Panel to determine the currency symbol and thousands separator to display.</span></span> <span data-ttu-id="c7bb6-123">(В **панели управления** щелкните Регион и **язык,** а затем нажмите **кнопку Дополнительные Параметры.)**</span><span class="sxs-lookup"><span data-stu-id="c7bb6-123">(In **Control Panel**, click **Region and Language**, and then click **Additional Settings**.)</span></span>
  
<span data-ttu-id="c7bb6-124">Чтобы преобразовать строку в значение валюты, чтобы можно было выполнять вычисления со значением, используйте функцию CY.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-124">To convert a string to a currency value so that you can perform calculations with the value, use the CY function.</span></span>
  
## <a name="using-functions-to-manipulate-text-strings"></a><span data-ttu-id="c7bb6-125">Использование функций для управления текстовыми строками</span><span class="sxs-lookup"><span data-stu-id="c7bb6-125">Using functions to manipulate text strings</span></span>

<span data-ttu-id="c7bb6-126">Можно использовать функции для управления текстовыми строками, например, для поиска или замены определенных символов в текстовой строке.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-126">You can use functions to manipulate text strings, for example, to locate or replace certain characters in a text string.</span></span> <span data-ttu-id="c7bb6-127">Вы также можете получить сведения о положении символа в строке или определить начало и окончание символов в текстовой строке.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-127">You can also get information about the position of a character in a string, or identify beginning and ending characters in a text string.</span></span> 
  

