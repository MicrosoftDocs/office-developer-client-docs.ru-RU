---
title: Сведения о строках
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251826
localization_priority: Normal
ms.assetid: e1174d8f-70cb-4595-7906-889da15367db
description: 'Формулы могут содержать строки. Чтобы отформатировать выходные данные строки, например в ячейке подсказки, значении элемента данных фигуры или текстовом поле, необходимо указать рисунок формата. Выходные данные можно форматировать как числовые, строковые, даты и время, продолжительность и денежные единицы. Например, формат picture0 #/10 ууформатс в качестве значения, состоящий из числового блока 10.9 cm AS10 9/10 сантиметры.'
ms.openlocfilehash: aa95e11db387913edbb40292f7da6a0f4b8a5cf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409519"
---
# <a name="about-strings"></a><span data-ttu-id="7a612-106">Сведения о строках</span><span class="sxs-lookup"><span data-stu-id="7a612-106">About Strings</span></span>

<span data-ttu-id="7a612-107">Формулы могут содержать строки.</span><span class="sxs-lookup"><span data-stu-id="7a612-107">Formulas can contain strings.</span></span> <span data-ttu-id="7a612-108">Чтобы отформатировать выходные данные строки, например в ячейке подсказки, значении элемента данных фигуры или текстовом поле, необходимо указать рисунок формата.</span><span class="sxs-lookup"><span data-stu-id="7a612-108">To format string output, such as in a prompt cell, a shape data item value, or a text field, you specify a format picture.</span></span> <span data-ttu-id="7a612-109">Выходные данные можно форматировать как числовые, строковые, даты и время, продолжительность и денежные единицы.</span><span class="sxs-lookup"><span data-stu-id="7a612-109">Output can be formatted as a number-unit pair, string, date-time, duration, or currency.</span></span> <span data-ttu-id="7a612-110">Например, рисунок формата "0 #/10 uu" форматирует комбинацию цифр 10.9 cm как "10 9/10 сантиметры".</span><span class="sxs-lookup"><span data-stu-id="7a612-110">For example, the format picture "0 #/10 uu" formats the number-unit pair 10.9cm as "10 9/10 centimeters".</span></span>
  
<span data-ttu-id="7a612-111">Вы можете использовать формат "рисунки" в ячейке " **Формат** " раздела "данные фигуры" и в качестве аргумента для функции **Format** или **FORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="7a612-111">You can use format pictures in the **Format** cell of the Shape Data section and as an argument to the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="7a612-112">При вставке текстового поля формат изображений отображается в списке форматов в диалоговом окне " **поле** " (вкладка "**Вставка** ").</span><span class="sxs-lookup"><span data-stu-id="7a612-112">When you insert a text field, format pictures appear in the list of formats in the **Field** dialog box (**Insert** tab).</span></span> 
  
## <a name="using-functions-to-format-strings"></a><span data-ttu-id="7a612-113">Использование функций для форматирования строк</span><span class="sxs-lookup"><span data-stu-id="7a612-113">Using functions to format strings</span></span>

<span data-ttu-id="7a612-114">В любой формуле, которая разрешается в строку, включая формулы настраиваемого текстового поля, можно использовать функцию **Format** или **FORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="7a612-114">In any formula that resolves to a string, including custom text field formulas, you can use the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="7a612-115">Функция FORMAT возвращает строку форматированных выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7a612-115">The FORMAT function returns a string of the formatted output.</span></span> <span data-ttu-id="7a612-116">Функция **FORMATEX** преобразует нетипизированные входные данные в единицы измерения, выбранные для отформатированного результата.</span><span class="sxs-lookup"><span data-stu-id="7a612-116">The **FORMATEX** function converts untyped input to the units you choose for the formatted result.</span></span> 
  
## <a name="displaying-formatted-shape-data"></a><span data-ttu-id="7a612-117">Отображение форматированных данных фигуры</span><span class="sxs-lookup"><span data-stu-id="7a612-117">Displaying formatted shape data</span></span>

<span data-ttu-id="7a612-118">Чтобы отформатировать отображаемое значение элемента данных фигуры, введите Рисунок в ячейке Format (формат).</span><span class="sxs-lookup"><span data-stu-id="7a612-118">You can format the displayed value of a shape data item by entering a format picture in the Format cell.</span></span>
  
<span data-ttu-id="7a612-119">Например, фигура временной шкалы проекта может иметь элемент данных фигуры, который измеряет стоимость процесса.</span><span class="sxs-lookup"><span data-stu-id="7a612-119">For example, a project timeline shape can have a shape data item that measures the cost of a process.</span></span> <span data-ttu-id="7a612-120">По умолчанию значением элемента данных фигуры является строка.</span><span class="sxs-lookup"><span data-stu-id="7a612-120">By default, a shape data item value is a string.</span></span> <span data-ttu-id="7a612-121">Чтобы отформатировать строку "1200", можно ввести "$ # # #, # # #. 00" в ячейке Format, чтобы пользователь видел денежную единицу.</span><span class="sxs-lookup"><span data-stu-id="7a612-121">To format the string "1200", you can enter "$###,###.00" in the Format cell so that the user sees a currency.</span></span>
  
<span data-ttu-id="7a612-122">Microsoft Visio использует параметры на вкладке **Валюта** в диалоговом окне **Настройка формата** в элементе **язык и** региональные параметры панели управления, чтобы определить символ денежной единицы и разделитель групп разрядов для отображения.</span><span class="sxs-lookup"><span data-stu-id="7a612-122">Microsoft Visio uses the settings on the **Currency** tab in the **Customize Format** dialog box in the **Region and Language** item in Control Panel to determine the currency symbol and thousands separator to display.</span></span> <span data-ttu-id="7a612-123">В **панели управления**щелкните **язык и язык**, а затем щелкните **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="7a612-123">(In **Control Panel**, click **Region and Language**, and then click **Additional Settings**.)</span></span>
  
<span data-ttu-id="7a612-124">Чтобы преобразовать строку в денежное значение, чтобы можно было выполнять вычисления со значением, используйте функцию CY.</span><span class="sxs-lookup"><span data-stu-id="7a612-124">To convert a string to a currency value so that you can perform calculations with the value, use the CY function.</span></span>
  
## <a name="using-functions-to-manipulate-text-strings"></a><span data-ttu-id="7a612-125">Использование функций для управления текстовыми строками</span><span class="sxs-lookup"><span data-stu-id="7a612-125">Using functions to manipulate text strings</span></span>

<span data-ttu-id="7a612-126">С помощью функций можно управлять текстовыми строками, например, чтобы искать или заменять определенные символы в текстовой строке.</span><span class="sxs-lookup"><span data-stu-id="7a612-126">You can use functions to manipulate text strings, for example, to locate or replace certain characters in a text string.</span></span> <span data-ttu-id="7a612-127">Кроме того, можно получить сведения о положении символа в строке или указать начальные и конечные символы в текстовой строке.</span><span class="sxs-lookup"><span data-stu-id="7a612-127">You can also get information about the position of a character in a string, or identify beginning and ending characters in a text string.</span></span> 
  

