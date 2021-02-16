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
description: 'Формулы могут содержать строки. Для формата вывода строки, например в ячейке запроса, значении элемента данных фигуры или текстовом поле, необходимо указать изображение формата. Выходные данные могут быть отформатированы в виде пары "число-единица", строки, даты и времени, длительности или валюты. Например, формат picture0 #/10 uuformats пары number-unit 10.9cm as10 9/10 cms.'
ms.openlocfilehash: aa95e11db387913edbb40292f7da6a0f4b8a5cf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409519"
---
# <a name="about-strings"></a><span data-ttu-id="6f431-106">О строках</span><span class="sxs-lookup"><span data-stu-id="6f431-106">About Strings</span></span>

<span data-ttu-id="6f431-107">Формулы могут содержать строки.</span><span class="sxs-lookup"><span data-stu-id="6f431-107">Formulas can contain strings.</span></span> <span data-ttu-id="6f431-108">Для формата вывода строки, например в ячейке запроса, значении элемента данных фигуры или текстовом поле, необходимо указать изображение формата.</span><span class="sxs-lookup"><span data-stu-id="6f431-108">To format string output, such as in a prompt cell, a shape data item value, or a text field, you specify a format picture.</span></span> <span data-ttu-id="6f431-109">Выходные данные могут быть отформатированы в виде пары "число-единица", строки, даты и времени, длительности или валюты.</span><span class="sxs-lookup"><span data-stu-id="6f431-109">Output can be formatted as a number-unit pair, string, date-time, duration, or currency.</span></span> <span data-ttu-id="6f431-110">Например, изображение формата "0 #/10 uu" форматирование пары число-единица 10,9cm как "10 9/10 cms".</span><span class="sxs-lookup"><span data-stu-id="6f431-110">For example, the format picture "0 #/10 uu" formats the number-unit pair 10.9cm as "10 9/10 centimeters".</span></span>
  
<span data-ttu-id="6f431-111">Вы можете использовать изображения формата в ячейке **Format** раздела "Данные фигуры" и в качестве аргумента функции **FORMAT** или **FORMATEX.**</span><span class="sxs-lookup"><span data-stu-id="6f431-111">You can use format pictures in the **Format** cell of the Shape Data section and as an argument to the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="6f431-112">При вставке текстового поля изображения формата отображаются  в списке форматов в диалоговом окне "Поле" (вкладка **"Вставка").**</span><span class="sxs-lookup"><span data-stu-id="6f431-112">When you insert a text field, format pictures appear in the list of formats in the **Field** dialog box (**Insert** tab).</span></span> 
  
## <a name="using-functions-to-format-strings"></a><span data-ttu-id="6f431-113">Использование функций для формата строк</span><span class="sxs-lookup"><span data-stu-id="6f431-113">Using functions to format strings</span></span>

<span data-ttu-id="6f431-114">В любой формуле, разрешаемой в строку, включая формулы настраиваемой текстовой поля, можно использовать функцию **FORMAT** или **FORMATEX.**</span><span class="sxs-lookup"><span data-stu-id="6f431-114">In any formula that resolves to a string, including custom text field formulas, you can use the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="6f431-115">Функция FORMAT возвращает строку отформатированные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="6f431-115">The FORMAT function returns a string of the formatted output.</span></span> <span data-ttu-id="6f431-116">Функция **FORMATEX** преобразует нетипизированные входные данные в единицы, выбираемые для форматируемого результата.</span><span class="sxs-lookup"><span data-stu-id="6f431-116">The **FORMATEX** function converts untyped input to the units you choose for the formatted result.</span></span> 
  
## <a name="displaying-formatted-shape-data"></a><span data-ttu-id="6f431-117">Отображение отформатированные данные фигуры</span><span class="sxs-lookup"><span data-stu-id="6f431-117">Displaying formatted shape data</span></span>

<span data-ttu-id="6f431-118">Вы можете отформатирование отображаемого значения элемента данных фигуры, введите изображение формата в ячейке Format.</span><span class="sxs-lookup"><span data-stu-id="6f431-118">You can format the displayed value of a shape data item by entering a format picture in the Format cell.</span></span>
  
<span data-ttu-id="6f431-119">Например, фигура временной шкалы проекта может иметь элемент данных фигуры, который измеряет стоимость процесса.</span><span class="sxs-lookup"><span data-stu-id="6f431-119">For example, a project timeline shape can have a shape data item that measures the cost of a process.</span></span> <span data-ttu-id="6f431-120">По умолчанию значение элемента данных фигуры является строкой.</span><span class="sxs-lookup"><span data-stu-id="6f431-120">By default, a shape data item value is a string.</span></span> <span data-ttu-id="6f431-121">Для формата строки "1200" можно ввести "$###,####.00" в ячейке Format, чтобы пользователь видел валюту.</span><span class="sxs-lookup"><span data-stu-id="6f431-121">To format the string "1200", you can enter "$###,###.00" in the Format cell so that the user sees a currency.</span></span>
  
<span data-ttu-id="6f431-122">Microsoft Visio использует параметры на вкладке  **"Валюта"** в  диалоговом окне "Настройка формата" в элементе "Область и язык" панели управления, чтобы определить символ валюты и отобразимый в ней знак тысяч.</span><span class="sxs-lookup"><span data-stu-id="6f431-122">Microsoft Visio uses the settings on the **Currency** tab in the **Customize Format** dialog box in the **Region and Language** item in Control Panel to determine the currency symbol and thousands separator to display.</span></span> <span data-ttu-id="6f431-123">(На **панели управления щелкните** **"Регион" и "Язык"** и выберите **"Дополнительные параметры".**</span><span class="sxs-lookup"><span data-stu-id="6f431-123">(In **Control Panel**, click **Region and Language**, and then click **Additional Settings**.)</span></span>
  
<span data-ttu-id="6f431-124">Чтобы преобразовать строку в значение валюты, чтобы можно было выполнять вычисления со значением, используйте функцию CY.</span><span class="sxs-lookup"><span data-stu-id="6f431-124">To convert a string to a currency value so that you can perform calculations with the value, use the CY function.</span></span>
  
## <a name="using-functions-to-manipulate-text-strings"></a><span data-ttu-id="6f431-125">Использование функций для управления текстовыми строками</span><span class="sxs-lookup"><span data-stu-id="6f431-125">Using functions to manipulate text strings</span></span>

<span data-ttu-id="6f431-126">Функции можно использовать для управления текстовыми строками, например для поиска или замены определенных символов в текстовой строке.</span><span class="sxs-lookup"><span data-stu-id="6f431-126">You can use functions to manipulate text strings, for example, to locate or replace certain characters in a text string.</span></span> <span data-ttu-id="6f431-127">Вы также можете получить сведения о положении символа в строке или определить начало и конец символов в текстовой строке.</span><span class="sxs-lookup"><span data-stu-id="6f431-127">You can also get information about the position of a character in a string, or identify beginning and ending characters in a text string.</span></span> 
  

