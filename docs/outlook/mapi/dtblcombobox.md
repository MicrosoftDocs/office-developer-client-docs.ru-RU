---
title: DTBLCOMBOBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCOMBOBOX
api_type:
- COM
ms.assetid: 73b68614-6aca-4669-b879-5631c5d6483c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5256efbff734d4555ac263dd330e3349c789cd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406978"
---
# <a name="dtblcombobox"></a><span data-ttu-id="46fb2-103">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="46fb2-103">DTBLCOMBOBOX</span></span>

  
  
<span data-ttu-id="46fb2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46fb2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46fb2-105">Описание управления полем со combo, который будет использоваться в диалоговом окне, построенного из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="46fb2-105">Describes a combo box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46fb2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="46fb2-106">Header file:</span></span>  <br/> |<span data-ttu-id="46fb2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="46fb2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="46fb2-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="46fb2-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="46fb2-109">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="46fb2-109">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |
   
```cpp
typedef struct _DTBLCOMBOBOX
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPRPropertyName;
  ULONG ulPRTableName;
} DTBLCOMBOBOX, FAR *LPDTBLCOMBOBOX;

```

## <a name="members"></a><span data-ttu-id="46fb2-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="46fb2-110">Members</span></span>

 <span data-ttu-id="46fb2-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="46fb2-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="46fb2-112">Смещение от начала структуры **DTBLCOMBOBOX** к фильтру строк символов, который описывает ограничения (если таковые есть) на символы, которые можно ввести в поле со combo.</span><span class="sxs-lookup"><span data-stu-id="46fb2-112">An offset from the start of the **DTBLCOMBOBOX** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the combo box's edit control.</span></span> <span data-ttu-id="46fb2-113">Фильтр не интерпретируется как регулярное выражение, и к каждому введенному символу применяется один и тот же фильтр.</span><span class="sxs-lookup"><span data-stu-id="46fb2-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="46fb2-114">Фильтр имеет такой формат:</span><span class="sxs-lookup"><span data-stu-id="46fb2-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="46fb2-115">**Символ**</span><span class="sxs-lookup"><span data-stu-id="46fb2-115">**Character**</span></span>|<span data-ttu-id="46fb2-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="46fb2-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="46fb2-117">Любой символ разрешен (например,  `"*"` ).</span><span class="sxs-lookup"><span data-stu-id="46fb2-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="46fb2-118">Определяет набор символов (например,  `"[0123456789]"` ).</span><span class="sxs-lookup"><span data-stu-id="46fb2-118">Defines a set of characters (for example,  `"[0123456789]"`).</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="46fb2-119">Указывает диапазон символов (например,  `"[a-z]"` ).</span><span class="sxs-lookup"><span data-stu-id="46fb2-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="46fb2-120">Указывает, что эти символы не разрешены.</span><span class="sxs-lookup"><span data-stu-id="46fb2-120">Indicates that these characters are not allowed.</span></span> <span data-ttu-id="46fb2-121">(например,  `"[~0-9]"` ).</span><span class="sxs-lookup"><span data-stu-id="46fb2-121">(for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="46fb2-122">Используется для кавычка любых из предыдущих символов (например,  `"[\-\\\[\]]"` знаки -, \, [и ] разрешены).</span><span class="sxs-lookup"><span data-stu-id="46fb2-122">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="46fb2-123">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="46fb2-123">**ulFlags**</span></span>
  
> <span data-ttu-id="46fb2-124">Битоваяmas флагов, используемых для обозначения формата фильтра строки символов.</span><span class="sxs-lookup"><span data-stu-id="46fb2-124">Bitmask of flags used to designate the format of the character string filter.</span></span> <span data-ttu-id="46fb2-125">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="46fb2-125">The following flag can be set:</span></span>
    
<span data-ttu-id="46fb2-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="46fb2-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="46fb2-127">Фильтр имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="46fb2-127">The filter is in Unicode format.</span></span> <span data-ttu-id="46fb2-128">Если флаг MAPI_UNICODE не установлен, фильтр будет в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="46fb2-128">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="46fb2-129">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="46fb2-129">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="46fb2-130">Максимальное количество символов, которые могут быть введены в текстовом поле со полем со полем со значением со значением.</span><span class="sxs-lookup"><span data-stu-id="46fb2-130">Maximum number of characters that can be entered in the combo box's text box.</span></span>
    
 <span data-ttu-id="46fb2-131">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="46fb2-131">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="46fb2-132">Тег свойства для свойства типа PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="46fb2-132">Property tag for a property of type PT_TSTRING.</span></span> 
    
 <span data-ttu-id="46fb2-133">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="46fb2-133">**ulPRTableName**</span></span>
  
> <span data-ttu-id="46fb2-134">Тег свойства для свойства типа PT_OBJECT, в котором интерфейс **IMAPITable** можно открыть с помощью вызова **OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="46fb2-134">Property tag for a property of type PT_OBJECT on which an **IMAPITable** interface can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="46fb2-135">В таблице должен быть один столбец со свойством того же типа, что и свойство, определенное членом **ulPRPropertyName.**</span><span class="sxs-lookup"><span data-stu-id="46fb2-135">The table must have one column with a property that is the same type as the property identified by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="46fb2-136">Строки таблицы используются для заполнения списка.</span><span class="sxs-lookup"><span data-stu-id="46fb2-136">The rows of the table are used to populate the list.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="46fb2-137">Примечания</span><span class="sxs-lookup"><span data-stu-id="46fb2-137">Remarks</span></span>

<span data-ttu-id="46fb2-138">Структура **DTBLCOMBOBOX** описывает поле со списком, которое состоит из списка и поля выбора.</span><span class="sxs-lookup"><span data-stu-id="46fb2-138">A **DTBLCOMBOBOX** structure describes a combo box a control that consists of a list and a selection field.</span></span> <span data-ttu-id="46fb2-139">В списке представлены сведения, из которых пользователь может выбрать, а в поле выбора отображается текущий выбор.</span><span class="sxs-lookup"><span data-stu-id="46fb2-139">The list presents the information from which a user can select, and the selection field displays the current selection.</span></span> <span data-ttu-id="46fb2-140">Поле выбора — это редактируемая область, которую также можно использовать для ввода текста, который еще не находится в списке.</span><span class="sxs-lookup"><span data-stu-id="46fb2-140">The selection field is an edit control that can also be used to enter text not already in the list.</span></span> 
  
<span data-ttu-id="46fb2-141">Два члена тега свойства работают вместе для координации отображения списка с помощью управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="46fb2-141">The two property tag members work together to coordinate the list display with the edit control.</span></span> <span data-ttu-id="46fb2-142">При первом отображении окна со combo MAPI вызывает метод **OpenProperty** реализации **IMAPIProp,** связанный с таблицей отображения, чтобы получить таблицу, представленную членом **ulPRTableName.**</span><span class="sxs-lookup"><span data-stu-id="46fb2-142">When MAPI first displays the combo box, it calls the **OpenProperty** method of the **IMAPIProp** implementation that is associated with the display table to retrieve the table represented by the **ulPRTableName** member.</span></span> <span data-ttu-id="46fb2-143">В этой таблице имеется один столбец, содержащий значения свойства, представленного членом **ulPRPropertyName.**</span><span class="sxs-lookup"><span data-stu-id="46fb2-143">This table has one column a column that contains values for the property represented by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="46fb2-144">Поэтому этот столбец должен иметь тот же тип, что и свойство **ulPRPropertyName,** а оба столбца должны быть строками символов.</span><span class="sxs-lookup"><span data-stu-id="46fb2-144">Therefore, this column must be of the same type as the **ulPRPropertyName** property and both columns must be character strings.</span></span> 
  
<span data-ttu-id="46fb2-145">Значения столбца отображаются в разделе списка в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="46fb2-145">The values for the column are displayed in the list section of the combo box.</span></span> <span data-ttu-id="46fb2-146">Таким образом, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) не является допустимым тегом свойства **для ulPRPropertyName**.</span><span class="sxs-lookup"><span data-stu-id="46fb2-146">Therefore, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) is not a valid property tag for **ulPRPropertyName**.</span></span> <span data-ttu-id="46fb2-147">Когда пользователь выбирает одну из строк или вводит новые данные в текстовое поле, для свойства **ulPRPropertyName** устанавливается выбранное или введенное значение.</span><span class="sxs-lookup"><span data-stu-id="46fb2-147">When a user either selects one of the rows or enters new data into the text box, the **ulPRPropertyName** property is set to the selected or entered value.</span></span> 
  
<span data-ttu-id="46fb2-148">Чтобы отобразить начальное значение для управления редактированием, MAPI вызывает [IMAPIProp::GetProps](imapiprop-getprops.md) для получения значений свойств для таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="46fb2-148">To display an initial value for the edit control, MAPI calls [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve the property values for the display table.</span></span> <span data-ttu-id="46fb2-149">Если одно из извлеченных свойств соответствует свойству, представленного членом **ulPRPropertyName,** его значение становится исходным значением.</span><span class="sxs-lookup"><span data-stu-id="46fb2-149">If one of the retrieved properties matches the property represented by the **ulPRPropertyName** member, its value becomes the initial value.</span></span> 
  
<span data-ttu-id="46fb2-150">Обзор таблиц отображения см. в [таблице отображения.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="46fb2-150">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="46fb2-151">Сведения о реализации таблицы отображения см. в таблице ["Реализация таблицы отображения".](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="46fb2-151">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="46fb2-152">См. также</span><span class="sxs-lookup"><span data-stu-id="46fb2-152">See also</span></span>



[<span data-ttu-id="46fb2-153">DTCTL</span><span class="sxs-lookup"><span data-stu-id="46fb2-153">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="46fb2-154">Каноническое свойство PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="46fb2-154">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="46fb2-155">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="46fb2-155">MAPI Structures</span></span>](mapi-structures.md)

