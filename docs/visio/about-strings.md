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
description: 'Формулы могут содержать строки. Для форматирования выходных данных string, такие как приглашениями ячейки, значение элемента данных фигуры или текстового поля, указать формат рисунка. Можно отформатировать выходные данные пару число единица, строки, даты и времени, длительность и денежных единиц. Например uuformats #/ 10 формата picture0 число единица пары as10 10.9cm 9 и 10 см.'
ms.openlocfilehash: 1fd003ecd5c824042e97a40fa8374aeead254ddc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813112"
---
# <a name="about-strings"></a><span data-ttu-id="fbf8f-106">Сведения о строках</span><span class="sxs-lookup"><span data-stu-id="fbf8f-106">About Strings</span></span>

<span data-ttu-id="fbf8f-107">Формулы могут содержать строки.</span><span class="sxs-lookup"><span data-stu-id="fbf8f-107">Formulas can contain strings.</span></span> <span data-ttu-id="fbf8f-108">Для форматирования выходных данных string, такие как приглашениями ячейки, значение элемента данных фигуры или текстового поля, указать формат рисунка.</span><span class="sxs-lookup"><span data-stu-id="fbf8f-108">To format string output, such as in a prompt cell, a shape data item value, or a text field, you specify a format picture.</span></span> <span data-ttu-id="fbf8f-109">Можно отформатировать выходные данные пару число единица, строки, даты и времени, длительность и денежных единиц.</span><span class="sxs-lookup"><span data-stu-id="fbf8f-109">Output can be formatted as a number-unit pair, string, date-time, duration, or currency.</span></span> <span data-ttu-id="fbf8f-110">Например изображение формата «# 0/10 uu» форматов пару число единица 10.9cm как «10 9 и 10 см».</span><span class="sxs-lookup"><span data-stu-id="fbf8f-110">For example, the format picture "0 #/10 uu" formats the number-unit pair 10.9cm as "10 9/10 centimeters".</span></span>
  
<span data-ttu-id="fbf8f-111">Можно использовать формат изображения в **Формат** ячеек в разделе данных фигуры и в качестве аргумента в функцию **ФОРМАТ** или **FORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="fbf8f-111">You can use format pictures in the **Format** cell of the Shape Data section and as an argument to the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="fbf8f-112">При вставке текстового поля, формат изображения отображается в списке форматов в диалоговом окне **поля** (вкладка "**Вставка** ").</span><span class="sxs-lookup"><span data-stu-id="fbf8f-112">When you insert a text field, format pictures appear in the list of formats in the **Field** dialog box (**Insert** tab).</span></span> 
  
## <a name="using-functions-to-format-strings"></a><span data-ttu-id="fbf8f-113">Использование функций в формате строки</span><span class="sxs-lookup"><span data-stu-id="fbf8f-113">Using functions to format strings</span></span>

<span data-ttu-id="fbf8f-114">В любую формулу, которая разрешается в строку, в том числе формул полей настраиваемого текста можно использовать функцию **ФОРМАТ** или **FORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="fbf8f-114">In any formula that resolves to a string, including custom text field formulas, you can use the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="fbf8f-115">Функция FORMAT возвращает строку Форматированные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="fbf8f-115">The FORMAT function returns a string of the formatted output.</span></span> <span data-ttu-id="fbf8f-116">Функция **FORMATEX** преобразует нетипизированный входные данные для единицы измерения выберите форматированный результата.</span><span class="sxs-lookup"><span data-stu-id="fbf8f-116">The **FORMATEX** function converts untyped input to the units you choose for the formatted result.</span></span> 
  
## <a name="displaying-formatted-shape-data"></a><span data-ttu-id="fbf8f-117">Отображение данных фигур форматированный</span><span class="sxs-lookup"><span data-stu-id="fbf8f-117">Displaying formatted shape data</span></span>

<span data-ttu-id="fbf8f-118">Можно отформатировать отображаемое значение элемента данных фигуры, введя Формат рисунка в формат ячейки.</span><span class="sxs-lookup"><span data-stu-id="fbf8f-118">You can format the displayed value of a shape data item by entering a format picture in the Format cell.</span></span>
  
<span data-ttu-id="fbf8f-119">К примеру фигура временной шкалы проекта может иметь элемент данных фигуры, меры затраты на процесс.</span><span class="sxs-lookup"><span data-stu-id="fbf8f-119">For example, a project timeline shape can have a shape data item that measures the cost of a process.</span></span> <span data-ttu-id="fbf8f-120">По умолчанию значение элемента данных фигуры — это строка.</span><span class="sxs-lookup"><span data-stu-id="fbf8f-120">By default, a shape data item value is a string.</span></span> <span data-ttu-id="fbf8f-121">Форматирование строки «1200», можно ввести «###, ###. 00" Формат ячеек, чтобы пользователь видит currency.</span><span class="sxs-lookup"><span data-stu-id="fbf8f-121">To format the string "1200", you can enter "$###,###.00" in the Format cell so that the user sees a currency.</span></span>
  
<span data-ttu-id="fbf8f-122">Microsoft Visio используются параметры на вкладке **Валюта** в диалоговом окне **Настройка формата** элемента **язык и региональные стандарты** на панели управления для определения символ валюты и тысяч разделителя для отображения.</span><span class="sxs-lookup"><span data-stu-id="fbf8f-122">Microsoft Visio uses the settings on the **Currency** tab in the **Customize Format** dialog box in the **Region and Language** item in Control Panel to determine the currency symbol and thousands separator to display.</span></span> <span data-ttu-id="fbf8f-123">(В **Панели управления**щелкните **язык и региональные стандарты**и нажмите кнопку **Дополнительные параметры**.)</span><span class="sxs-lookup"><span data-stu-id="fbf8f-123">(In **Control Panel**, click **Region and Language**, and then click **Additional Settings**.)</span></span>
  
<span data-ttu-id="fbf8f-124">Для преобразования строки в значение типа currency, чтобы может выполнять вычисления со значением, используйте функцию кг.</span><span class="sxs-lookup"><span data-stu-id="fbf8f-124">To convert a string to a currency value so that you can perform calculations with the value, use the CY function.</span></span>
  
## <a name="using-functions-to-manipulate-text-strings"></a><span data-ttu-id="fbf8f-125">Использование функций для работы с текстовые строки</span><span class="sxs-lookup"><span data-stu-id="fbf8f-125">Using functions to manipulate text strings</span></span>

<span data-ttu-id="fbf8f-126">Можно использовать функции для работы с строки текста, например, для поиска или замены определенных символов в текстовой строке.</span><span class="sxs-lookup"><span data-stu-id="fbf8f-126">You can use functions to manipulate text strings, for example, to locate or replace certain characters in a text string.</span></span> <span data-ttu-id="fbf8f-127">Можно получить сведения о позиции символа в строке или определение начального и конечного символов в текстовой строке.</span><span class="sxs-lookup"><span data-stu-id="fbf8f-127">You can also get information about the position of a character in a string, or identify beginning and ending characters in a text string.</span></span> 
  

