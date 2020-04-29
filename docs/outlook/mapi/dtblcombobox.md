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
# <a name="dtblcombobox"></a><span data-ttu-id="a0820-103">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="a0820-103">DTBLCOMBOBOX</span></span>

  
  
<span data-ttu-id="a0820-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0820-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0820-105">Описывает элемент управления "поле со списком", который будет использоваться в диалоговом окне, созданном из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="a0820-105">Describes a combo box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0820-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a0820-106">Header file:</span></span>  <br/> |<span data-ttu-id="a0820-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="a0820-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a0820-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="a0820-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="a0820-109">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="a0820-109">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |
   
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

## <a name="members"></a><span data-ttu-id="a0820-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="a0820-110">Members</span></span>

 <span data-ttu-id="a0820-111">**улблпсзчарсалловед**</span><span class="sxs-lookup"><span data-stu-id="a0820-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="a0820-112">Смещение от начала структуры **дтблкомбобокс** к фильтру строк символов, описывающему ограничения (при их наличии) до символов, которые можно ввести в поле редактирования поля со списком.</span><span class="sxs-lookup"><span data-stu-id="a0820-112">An offset from the start of the **DTBLCOMBOBOX** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the combo box's edit control.</span></span> <span data-ttu-id="a0820-113">Фильтр не интерпретируется как регулярное выражение, и к каждому введенному символу применяется один и тот же фильтр.</span><span class="sxs-lookup"><span data-stu-id="a0820-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="a0820-114">Фильтр имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="a0820-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="a0820-115">**Символ**</span><span class="sxs-lookup"><span data-stu-id="a0820-115">**Character**</span></span>|<span data-ttu-id="a0820-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a0820-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="a0820-117">Разрешен любой символ (например, `"*"`).</span><span class="sxs-lookup"><span data-stu-id="a0820-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="a0820-118">Определяет набор символов (например, `"[0123456789]"`).</span><span class="sxs-lookup"><span data-stu-id="a0820-118">Defines a set of characters (for example,  `"[0123456789]"`).</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="a0820-119">Указывает диапазон символов (например, `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="a0820-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="a0820-120">Указывает, что эти символы не допускаются.</span><span class="sxs-lookup"><span data-stu-id="a0820-120">Indicates that these characters are not allowed.</span></span> <span data-ttu-id="a0820-121">(например, `"[~0-9]"`).</span><span class="sxs-lookup"><span data-stu-id="a0820-121">(for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="a0820-122">Используется для заключения в кавычки любого из предыдущих символов (например `"[\-\\\[\]]"` , допустимые \, символы-, [, и]).</span><span class="sxs-lookup"><span data-stu-id="a0820-122">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="a0820-123">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="a0820-123">**ulFlags**</span></span>
  
> <span data-ttu-id="a0820-124">Битовая маска флагов, используемых для обозначения формата фильтра строк символов.</span><span class="sxs-lookup"><span data-stu-id="a0820-124">Bitmask of flags used to designate the format of the character string filter.</span></span> <span data-ttu-id="a0820-125">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a0820-125">The following flag can be set:</span></span>
    
<span data-ttu-id="a0820-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a0820-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a0820-127">Фильтр имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="a0820-127">The filter is in Unicode format.</span></span> <span data-ttu-id="a0820-128">Если флаг MAPI_UNICODE не установлен, фильтр имеет формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="a0820-128">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="a0820-129">**улнумчарсалловед**</span><span class="sxs-lookup"><span data-stu-id="a0820-129">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="a0820-130">Максимальное число символов, которое можно ввести в текстовом поле поля со списком.</span><span class="sxs-lookup"><span data-stu-id="a0820-130">Maximum number of characters that can be entered in the combo box's text box.</span></span>
    
 <span data-ttu-id="a0820-131">**улпрпропертинаме**</span><span class="sxs-lookup"><span data-stu-id="a0820-131">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="a0820-132">Тег свойства для свойства типа PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="a0820-132">Property tag for a property of type PT_TSTRING.</span></span> 
    
 <span data-ttu-id="a0820-133">**улпртабленаме**</span><span class="sxs-lookup"><span data-stu-id="a0820-133">**ulPRTableName**</span></span>
  
> <span data-ttu-id="a0820-134">Тег свойства для свойства типа PT_OBJECT, в котором можно открыть интерфейс **IMAPITable** с помощью вызова **опенпроперти** .</span><span class="sxs-lookup"><span data-stu-id="a0820-134">Property tag for a property of type PT_OBJECT on which an **IMAPITable** interface can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="a0820-135">У таблицы должен быть один столбец со свойством, имеющим тот же тип, что и свойство, определяемое элементом **улпрпропертинаме** .</span><span class="sxs-lookup"><span data-stu-id="a0820-135">The table must have one column with a property that is the same type as the property identified by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="a0820-136">Строки таблицы используются для заполнения списка.</span><span class="sxs-lookup"><span data-stu-id="a0820-136">The rows of the table are used to populate the list.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a0820-137">Примечания</span><span class="sxs-lookup"><span data-stu-id="a0820-137">Remarks</span></span>

<span data-ttu-id="a0820-138">Структура **дтблкомбобокс** описывает элемент управления "поле со списком", состоящий из списка и поля выбора.</span><span class="sxs-lookup"><span data-stu-id="a0820-138">A **DTBLCOMBOBOX** structure describes a combo box a control that consists of a list and a selection field.</span></span> <span data-ttu-id="a0820-139">В списке представлены сведения, которые пользователь может выбрать, а в поле Выбор отображается текущий выделенный фрагмент.</span><span class="sxs-lookup"><span data-stu-id="a0820-139">The list presents the information from which a user can select, and the selection field displays the current selection.</span></span> <span data-ttu-id="a0820-140">Поле Selection является элементом управления редактирования, который можно использовать для ввода текста, которого еще нет в списке.</span><span class="sxs-lookup"><span data-stu-id="a0820-140">The selection field is an edit control that can also be used to enter text not already in the list.</span></span> 
  
<span data-ttu-id="a0820-141">Два элемента тега свойства взаимодействуют для координации отображения списка с помощью элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="a0820-141">The two property tag members work together to coordinate the list display with the edit control.</span></span> <span data-ttu-id="a0820-142">При первом отображении поля со списком с помощью MAPI вызывается метод **опенпроперти** реализации **IMAPIProp** , связанный с таблицей отображения для получения таблицы, представленной элементом **улпртабленаме** .</span><span class="sxs-lookup"><span data-stu-id="a0820-142">When MAPI first displays the combo box, it calls the **OpenProperty** method of the **IMAPIProp** implementation that is associated with the display table to retrieve the table represented by the **ulPRTableName** member.</span></span> <span data-ttu-id="a0820-143">В этой таблице есть один столбец, содержащий значения для свойства, представленного элементом **улпрпропертинаме** .</span><span class="sxs-lookup"><span data-stu-id="a0820-143">This table has one column a column that contains values for the property represented by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="a0820-144">Таким образом, этот столбец должен иметь тот же тип, что и свойство **улпрпропертинаме** , и оба столбца должны быть строками символов.</span><span class="sxs-lookup"><span data-stu-id="a0820-144">Therefore, this column must be of the same type as the **ulPRPropertyName** property and both columns must be character strings.</span></span> 
  
<span data-ttu-id="a0820-145">Значения для столбца отображаются в разделе "список" в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="a0820-145">The values for the column are displayed in the list section of the combo box.</span></span> <span data-ttu-id="a0820-146">Таким образом, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) не является допустимым тегом свойства для **улпрпропертинаме**.</span><span class="sxs-lookup"><span data-stu-id="a0820-146">Therefore, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) is not a valid property tag for **ulPRPropertyName**.</span></span> <span data-ttu-id="a0820-147">Когда пользователь выбирает одну из строк или вводит новые данные в текстовое поле, свойству **улпрпропертинаме** присваивается выбранное или введенное значение.</span><span class="sxs-lookup"><span data-stu-id="a0820-147">When a user either selects one of the rows or enters new data into the text box, the **ulPRPropertyName** property is set to the selected or entered value.</span></span> 
  
<span data-ttu-id="a0820-148">Для отображения начального значения для элемента управления "поле ввода" MAPI вызывает [IMAPIProp::/PROPS](imapiprop-getprops.md) для получения значений свойств для таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="a0820-148">To display an initial value for the edit control, MAPI calls [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve the property values for the display table.</span></span> <span data-ttu-id="a0820-149">Если одно из извлеченных свойств соответствует свойству, представленному элементом **улпрпропертинаме** , его значение становится начальным.</span><span class="sxs-lookup"><span data-stu-id="a0820-149">If one of the retrieved properties matches the property represented by the **ulPRPropertyName** member, its value becomes the initial value.</span></span> 
  
<span data-ttu-id="a0820-150">Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="a0820-150">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="a0820-151">Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="a0820-151">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a0820-152">См. также</span><span class="sxs-lookup"><span data-stu-id="a0820-152">See also</span></span>



[<span data-ttu-id="a0820-153">DTCTL</span><span class="sxs-lookup"><span data-stu-id="a0820-153">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="a0820-154">Каноническое свойство PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="a0820-154">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="a0820-155">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="a0820-155">MAPI Structures</span></span>](mapi-structures.md)

