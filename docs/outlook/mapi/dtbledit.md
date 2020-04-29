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
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b07ea265b5dcc6b9a9abb15c6be7ac9e0f94e8ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404682"
---
# <a name="dtbledit"></a><span data-ttu-id="b20da-103">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="b20da-103">DTBLEDIT</span></span>

  
  
<span data-ttu-id="b20da-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b20da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b20da-105">Описывает элемент управления "поле ввода", который будет использоваться в диалоговом окне, созданном из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="b20da-105">Describes an edit control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b20da-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b20da-106">Header file:</span></span>  <br/> |<span data-ttu-id="b20da-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b20da-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b20da-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="b20da-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="b20da-109">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="b20da-109">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |
   
```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a><span data-ttu-id="b20da-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="b20da-110">Members</span></span>

 <span data-ttu-id="b20da-111">**улблпсзчарсалловед**</span><span class="sxs-lookup"><span data-stu-id="b20da-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="b20da-112">Смещение от начала структуры **дтбледит** к фильтру строк символов, описывающему ограничения (при их наличии) до символов, которые можно ввести в элемент управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="b20da-112">An offset from the start of the **DTBLEDIT** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the edit control.</span></span> <span data-ttu-id="b20da-113">Фильтр не интерпретируется как регулярное выражение, и к каждому введенному символу применяется один и тот же фильтр.</span><span class="sxs-lookup"><span data-stu-id="b20da-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="b20da-114">Фильтр имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="b20da-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="b20da-115">**Символ**</span><span class="sxs-lookup"><span data-stu-id="b20da-115">**Character**</span></span>|<span data-ttu-id="b20da-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b20da-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="b20da-117">Разрешен любой символ (например, `"*"`).</span><span class="sxs-lookup"><span data-stu-id="b20da-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="b20da-118">Определяет набор символов (например, `"[0123456789]".`);</span><span class="sxs-lookup"><span data-stu-id="b20da-118">Defines a set of characters (for example,  `"[0123456789]".`)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="b20da-119">Указывает диапазон символов (например, `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="b20da-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="b20da-120">Указывает, что эти символы не допускаются (например, `"[~0-9]"`).</span><span class="sxs-lookup"><span data-stu-id="b20da-120">Indicates that these characters are not allowed (for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="b20da-121">Используется для заключения в кавычки любого из предыдущих символов (например `"[\-\\\[\]]"` , допустимые \, символы-, [, и]).</span><span class="sxs-lookup"><span data-stu-id="b20da-121">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="b20da-122">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="b20da-122">**ulFlags**</span></span>
  
> <span data-ttu-id="b20da-123">Битовая маска флагов, используемых для обозначения формата фильтра символов.</span><span class="sxs-lookup"><span data-stu-id="b20da-123">Bitmask of flags used to designate the format of the character filter.</span></span> <span data-ttu-id="b20da-124">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="b20da-124">The following flag can be set:</span></span>
    
<span data-ttu-id="b20da-125">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b20da-125">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="b20da-126">Фильтр имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="b20da-126">The filter is in Unicode format.</span></span> <span data-ttu-id="b20da-127">Если флаг MAPI_UNICODE не установлен, фильтр имеет формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="b20da-127">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="b20da-128">**улнумчарсалловед**</span><span class="sxs-lookup"><span data-stu-id="b20da-128">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="b20da-129">Максимальное количество символов, которое пользователь может ввести в текстовое поле.</span><span class="sxs-lookup"><span data-stu-id="b20da-129">Maximum number of characters that the user can type into the text box.</span></span>
    
 <span data-ttu-id="b20da-130">**улпроптаг**</span><span class="sxs-lookup"><span data-stu-id="b20da-130">**ulPropTag**</span></span>
  
> <span data-ttu-id="b20da-131">Тег свойства для свойства типа PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="b20da-131">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="b20da-132">Элемент **улпроптаг** Идентифицирует свойство String, данные которого отображаются и редактируются в элементе управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="b20da-132">The **ulPropTag** member identifies the string property whose data is displayed and edited in the edit control.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b20da-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="b20da-133">Remarks</span></span>

<span data-ttu-id="b20da-134">Структура **дтбледит** описывает элемент управления "поле ввода" в диалоговом окне, который содержит буквенно-цифровые сведения.</span><span class="sxs-lookup"><span data-stu-id="b20da-134">A **DTBLEDIT** structure describes an edit control an area on a dialog box that contains alphanumeric information.</span></span> <span data-ttu-id="b20da-135">Почти во всех диалоговых окнах есть по крайней мере один элемент управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="b20da-135">Almost all dialog boxes have at least one edit control.</span></span> <span data-ttu-id="b20da-136">Элементы управления редактирования могут быть изменяемыми пользователем или доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b20da-136">Edit controls can be modifiable by a user or read-only.</span></span> 
  
<span data-ttu-id="b20da-137">Элементы управления редактированием также могут быть одной строкой или многострочной.</span><span class="sxs-lookup"><span data-stu-id="b20da-137">Edit controls can also be single line or multiline.</span></span> <span data-ttu-id="b20da-138">Многострочные элементы управления редактирования обычно связаны с полосой прокрутки.</span><span class="sxs-lookup"><span data-stu-id="b20da-138">Multiline edit controls typically have a scroll bar associated with them.</span></span> 
  
<span data-ttu-id="b20da-139">Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b20da-139">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="b20da-140">Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="b20da-140">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b20da-141">См. также</span><span class="sxs-lookup"><span data-stu-id="b20da-141">See also</span></span>



[<span data-ttu-id="b20da-142">DTCTL</span><span class="sxs-lookup"><span data-stu-id="b20da-142">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="b20da-143">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="b20da-143">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="b20da-144">Каноническое свойство PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="b20da-144">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="b20da-145">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="b20da-145">MAPI Structures</span></span>](mapi-structures.md)

