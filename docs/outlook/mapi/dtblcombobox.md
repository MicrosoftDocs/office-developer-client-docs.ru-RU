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
ms.openlocfilehash: 3a5188ea9f83d05722c6b5ab81d9e796b33ef254
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808346"
---
# <a name="dtblcombobox"></a><span data-ttu-id="b2d72-103">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="b2d72-103">DTBLCOMBOBOX</span></span>

  
  
<span data-ttu-id="b2d72-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b2d72-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b2d72-105">Поле со списком, который будет использоваться в диалоговое окно, построенная на основе таблицы Отображаемое описание.</span><span class="sxs-lookup"><span data-stu-id="b2d72-105">Describes a combo box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b2d72-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b2d72-106">Header file:</span></span>  <br/> |<span data-ttu-id="b2d72-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b2d72-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b2d72-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="b2d72-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="b2d72-109">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="b2d72-109">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |
   
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

## <a name="members"></a><span data-ttu-id="b2d72-110">Members</span><span class="sxs-lookup"><span data-stu-id="b2d72-110">Members</span></span>

 <span data-ttu-id="b2d72-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="b2d72-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="b2d72-112">Смещение от начала структуры **DTBLCOMBOBOX** в фильтр символ строка, описывающая ограничения, если оно нужно символов, которое можно ввести в поле со списком редактирования элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b2d72-112">An offset from the start of the **DTBLCOMBOBOX** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the combo box's edit control.</span></span> <span data-ttu-id="b2d72-113">Фильтр не обрабатывается как регулярное выражение и тот же фильтр применяется к каждый символ, введенный.</span><span class="sxs-lookup"><span data-stu-id="b2d72-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="b2d72-114">Формат фильтр выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b2d72-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="b2d72-115">**Символ**</span><span class="sxs-lookup"><span data-stu-id="b2d72-115">**Character**</span></span>|<span data-ttu-id="b2d72-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b2d72-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="b2d72-117">Допускается любой символ (например, `"*"`).</span><span class="sxs-lookup"><span data-stu-id="b2d72-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="b2d72-118">Определяет набор символов (например, `"[0123456789]"`).</span><span class="sxs-lookup"><span data-stu-id="b2d72-118">Defines a set of characters (for example,  `"[0123456789]"`).</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="b2d72-119">Указывает диапазон символов (например, `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="b2d72-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="b2d72-120">Указывает, что эти символы не допускается.</span><span class="sxs-lookup"><span data-stu-id="b2d72-120">Indicates that these characters are not allowed.</span></span> <span data-ttu-id="b2d72-121">(например, `"[~0-9]"`).</span><span class="sxs-lookup"><span data-stu-id="b2d72-121">(for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="b2d72-122">Используется для любой из предыдущих символы кавычек (например, `"[\-\\\[\]]"` означает, что-, \, [, и] могут знаков).</span><span class="sxs-lookup"><span data-stu-id="b2d72-122">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="b2d72-123">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="b2d72-123">**ulFlags**</span></span>
  
> <span data-ttu-id="b2d72-124">Битовая маска флаги, используемые для обозначения формата фильтра строку знаков.</span><span class="sxs-lookup"><span data-stu-id="b2d72-124">Bitmask of flags used to designate the format of the character string filter.</span></span> <span data-ttu-id="b2d72-125">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="b2d72-125">The following flag can be set:</span></span>
    
<span data-ttu-id="b2d72-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b2d72-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b2d72-127">Фильтр — в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="b2d72-127">The filter is in Unicode format.</span></span> <span data-ttu-id="b2d72-128">Если флаг MAPI_UNICODE не установлен, в формате ANSI — фильтра.</span><span class="sxs-lookup"><span data-stu-id="b2d72-128">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="b2d72-129">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="b2d72-129">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="b2d72-130">Максимальное число символов, которые можно ввести в поле со списком текстовое поле.</span><span class="sxs-lookup"><span data-stu-id="b2d72-130">Maximum number of characters that can be entered in the combo box's text box.</span></span>
    
 <span data-ttu-id="b2d72-131">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="b2d72-131">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="b2d72-132">Свойство tag для свойства типа PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="b2d72-132">Property tag for a property of type PT_TSTRING.</span></span> 
    
 <span data-ttu-id="b2d72-133">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="b2d72-133">**ulPRTableName**</span></span>
  
> <span data-ttu-id="b2d72-134">Свойство тег для свойства PT_OBJECT тип, на котором можно открыть интерфейс **IMAPITable** путем вызова **OpenProperty** .</span><span class="sxs-lookup"><span data-stu-id="b2d72-134">Property tag for a property of type PT_OBJECT on which an **IMAPITable** interface can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="b2d72-135">Таблица должна иметь один столбец со свойством, которое совпадает с типом свойство, определяемое члена **ulPRPropertyName** .</span><span class="sxs-lookup"><span data-stu-id="b2d72-135">The table must have one column with a property that is the same type as the property identified by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="b2d72-136">Строки таблицы используются для заполнения списка.</span><span class="sxs-lookup"><span data-stu-id="b2d72-136">The rows of the table are used to populate the list.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b2d72-137">Замечания</span><span class="sxs-lookup"><span data-stu-id="b2d72-137">Remarks</span></span>

<span data-ttu-id="b2d72-138">Структура **DTBLCOMBOBOX** описывает элемент управления, содержащий список и поле выбора поле со списком.</span><span class="sxs-lookup"><span data-stu-id="b2d72-138">A **DTBLCOMBOBOX** structure describes a combo box a control that consists of a list and a selection field.</span></span> <span data-ttu-id="b2d72-139">В списке представлены сведения, с которого пользователь может выбрать, и поле выбора отображает текущее выделение.</span><span class="sxs-lookup"><span data-stu-id="b2d72-139">The list presents the information from which a user can select, and the selection field displays the current selection.</span></span> <span data-ttu-id="b2d72-140">В поле выбора является элементом управления, который также можно использовать для ввода текста еще не в списке.</span><span class="sxs-lookup"><span data-stu-id="b2d72-140">The selection field is an edit control that can also be used to enter text not already in the list.</span></span> 
  
<span data-ttu-id="b2d72-141">Элементы тега два свойства работают вместе для координации отображения списка с помощью элемента управления поля ввода.</span><span class="sxs-lookup"><span data-stu-id="b2d72-141">The two property tag members work together to coordinate the list display with the edit control.</span></span> <span data-ttu-id="b2d72-142">Когда MAPI сначала отображает поле со списком, он вызывает метод **OpenProperty** реализации **IMAPIProp** , связанный с таблицей отображения для получения таблицы, представленного элементом **ulPRTableName** .</span><span class="sxs-lookup"><span data-stu-id="b2d72-142">When MAPI first displays the combo box, it calls the **OpenProperty** method of the **IMAPIProp** implementation that is associated with the display table to retrieve the table represented by the **ulPRTableName** member.</span></span> <span data-ttu-id="b2d72-143">Эта таблица имеет столбец, который содержит значения для свойства, представленного элементом **ulPRPropertyName** один столбец.</span><span class="sxs-lookup"><span data-stu-id="b2d72-143">This table has one column a column that contains values for the property represented by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="b2d72-144">Таким образом этот столбец должен быть того же типа как свойство **ulPRPropertyName** и обоих столбцов должно быть строк символов.</span><span class="sxs-lookup"><span data-stu-id="b2d72-144">Therefore, this column must be of the same type as the **ulPRPropertyName** property and both columns must be character strings.</span></span> 
  
<span data-ttu-id="b2d72-145">Значения для столбца отображаются в разделе список поле со списком.</span><span class="sxs-lookup"><span data-stu-id="b2d72-145">The values for the column are displayed in the list section of the combo box.</span></span> <span data-ttu-id="b2d72-146">Таким образом, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) не является допустимым свойством тег для **ulPRPropertyName**.</span><span class="sxs-lookup"><span data-stu-id="b2d72-146">Therefore, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) is not a valid property tag for **ulPRPropertyName**.</span></span> <span data-ttu-id="b2d72-147">Если пользователь выбирает один из строки или ввод новых данных в текстовом поле, свойство **ulPRPropertyName** задано значение выбранного или введенная.</span><span class="sxs-lookup"><span data-stu-id="b2d72-147">When a user either selects one of the rows or enters new data into the text box, the **ulPRPropertyName** property is set to the selected or entered value.</span></span> 
  
<span data-ttu-id="b2d72-148">Чтобы отобразить начальное значение для элемента управления поля ввода, MAPI вызывает [IMAPIProp::GetProps](imapiprop-getprops.md) для извлечения значения свойств для отображения таблицы.</span><span class="sxs-lookup"><span data-stu-id="b2d72-148">To display an initial value for the edit control, MAPI calls [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve the property values for the display table.</span></span> <span data-ttu-id="b2d72-149">Если один из извлеченные свойства соответствует свойству, представленному член **ulPRPropertyName** , его значение становится начального значения.</span><span class="sxs-lookup"><span data-stu-id="b2d72-149">If one of the retrieved properties matches the property represented by the **ulPRPropertyName** member, its value becomes the initial value.</span></span> 
  
<span data-ttu-id="b2d72-150">Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b2d72-150">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="b2d72-151">Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.</span><span class="sxs-lookup"><span data-stu-id="b2d72-151">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b2d72-152">См. также</span><span class="sxs-lookup"><span data-stu-id="b2d72-152">See also</span></span>



[<span data-ttu-id="b2d72-153">DTCTL</span><span class="sxs-lookup"><span data-stu-id="b2d72-153">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="b2d72-154">Каноническое свойство PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="b2d72-154">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="b2d72-155">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="b2d72-155">MAPI Structures</span></span>](mapi-structures.md)

