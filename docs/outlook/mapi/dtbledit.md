---
title: DTBLEDIT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLEDIT
api_type:
- COM
ms.assetid: ec3566a0-75ad-466d-a61e-f7d61ccb946d
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: d0418ac2ec5d01d58c63e4ad48a1066cc386e946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808357"
---
# <a name="dtbledit"></a><span data-ttu-id="3ec41-103">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="3ec41-103">DTBLEDIT</span></span>

  
  
<span data-ttu-id="3ec41-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3ec41-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3ec41-105">Описывает элемент управления редактирования, которая будет использоваться в диалоговое окно, построенная на основе таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="3ec41-105">Describes an edit control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3ec41-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3ec41-106">Header file:</span></span>  <br/> |<span data-ttu-id="3ec41-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3ec41-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3ec41-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="3ec41-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="3ec41-109">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="3ec41-109">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |
   
```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a><span data-ttu-id="3ec41-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="3ec41-110">Members</span></span>

 <span data-ttu-id="3ec41-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="3ec41-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="3ec41-112">Смещение от начала структуры **DTBLEDIT** в фильтр символ строка, описывающая ограничения, если оно нужно символов, которые можно ввести в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="3ec41-112">An offset from the start of the **DTBLEDIT** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the edit control.</span></span> <span data-ttu-id="3ec41-113">Фильтр не обрабатывается как регулярное выражение и тот же фильтр применяется к каждый символ, введенный.</span><span class="sxs-lookup"><span data-stu-id="3ec41-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="3ec41-114">Формат фильтр выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3ec41-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="3ec41-115">**Символ**</span><span class="sxs-lookup"><span data-stu-id="3ec41-115">**Character**</span></span>|<span data-ttu-id="3ec41-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3ec41-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="3ec41-117">Допускается любой символ (например, `"*"`).</span><span class="sxs-lookup"><span data-stu-id="3ec41-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="3ec41-118">Определяет набор символов (например, `"[0123456789]".`)</span><span class="sxs-lookup"><span data-stu-id="3ec41-118">Defines a set of characters (for example,  `"[0123456789]".`)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="3ec41-119">Указывает диапазон символов (например, `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="3ec41-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="3ec41-120">Указывает, что эти символы не разрешены (например, `"[~0-9]"`).</span><span class="sxs-lookup"><span data-stu-id="3ec41-120">Indicates that these characters are not allowed (for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="3ec41-121">Используется для любой из предыдущих символы кавычек (например, `"[\-\\\[\]]"` означает, что-, \, [, и] могут знаков).</span><span class="sxs-lookup"><span data-stu-id="3ec41-121">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="3ec41-122">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="3ec41-122">**ulFlags**</span></span>
  
> <span data-ttu-id="3ec41-123">Битовая маска флаги, используемые для обозначения формата фильтра знаков.</span><span class="sxs-lookup"><span data-stu-id="3ec41-123">Bitmask of flags used to designate the format of the character filter.</span></span> <span data-ttu-id="3ec41-124">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="3ec41-124">The following flag can be set:</span></span>
    
<span data-ttu-id="3ec41-125">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3ec41-125">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="3ec41-126">Фильтр — в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="3ec41-126">The filter is in Unicode format.</span></span> <span data-ttu-id="3ec41-127">Если флаг MAPI_UNICODE не установлен, в формате ANSI — фильтра.</span><span class="sxs-lookup"><span data-stu-id="3ec41-127">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="3ec41-128">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="3ec41-128">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="3ec41-129">Максимальное число символов, которые пользователь может ввести в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="3ec41-129">Maximum number of characters that the user can type into the text box.</span></span>
    
 <span data-ttu-id="3ec41-130">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="3ec41-130">**ulPropTag**</span></span>
  
> <span data-ttu-id="3ec41-131">Свойство tag для свойства типа PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="3ec41-131">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="3ec41-132">Элемент **ulPropTag** определяет свойство строки, данные которого отображается и редактируется в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="3ec41-132">The **ulPropTag** member identifies the string property whose data is displayed and edited in the edit control.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3ec41-133">Замечания</span><span class="sxs-lookup"><span data-stu-id="3ec41-133">Remarks</span></span>

<span data-ttu-id="3ec41-134">Структура **DTBLEDIT** описывает элемент управления редактирования область на диалоговое окно, которое содержит буквенно-цифровой информации.</span><span class="sxs-lookup"><span data-stu-id="3ec41-134">A **DTBLEDIT** structure describes an edit control an area on a dialog box that contains alphanumeric information.</span></span> <span data-ttu-id="3ec41-135">Почти все диалоговые окна имеют по крайней мере один элемент управления.</span><span class="sxs-lookup"><span data-stu-id="3ec41-135">Almost all dialog boxes have at least one edit control.</span></span> <span data-ttu-id="3ec41-136">Редактирование элементов управления может быть изменяемым пользователем, или только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3ec41-136">Edit controls can be modifiable by a user or read-only.</span></span> 
  
<span data-ttu-id="3ec41-137">Элементы управления поля ввода также может быть одной строки или multiline.</span><span class="sxs-lookup"><span data-stu-id="3ec41-137">Edit controls can also be single line or multiline.</span></span> <span data-ttu-id="3ec41-138">Элементы управления многострочный текст обычно содержат полосы прокрутки, связанных с ними.</span><span class="sxs-lookup"><span data-stu-id="3ec41-138">Multiline edit controls typically have a scroll bar associated with them.</span></span> 
  
<span data-ttu-id="3ec41-139">Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3ec41-139">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="3ec41-140">Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.</span><span class="sxs-lookup"><span data-stu-id="3ec41-140">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3ec41-141">См. также</span><span class="sxs-lookup"><span data-stu-id="3ec41-141">See also</span></span>



[<span data-ttu-id="3ec41-142">DTCTL</span><span class="sxs-lookup"><span data-stu-id="3ec41-142">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="3ec41-143">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="3ec41-143">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="3ec41-144">Каноническое свойство PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="3ec41-144">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="3ec41-145">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="3ec41-145">MAPI Structures</span></span>](mapi-structures.md)

