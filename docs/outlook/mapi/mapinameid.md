---
title: MAPINAMEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPINAMEID
api_type:
- COM
ms.assetid: 9a92e9cd-8282-4cf0-93af-4089b3763594
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: baec750a460b3ba9becd2e1dddf967705424ac4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411682"
---
# <a name="mapinameid"></a><span data-ttu-id="56ac4-103">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="56ac4-103">MAPINAMEID</span></span>

  
  
<span data-ttu-id="56ac4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56ac4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56ac4-105">Описывает именуемую собственность.</span><span class="sxs-lookup"><span data-stu-id="56ac4-105">Describes a named property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56ac4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="56ac4-106">Header file:</span></span>  <br/> |<span data-ttu-id="56ac4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="56ac4-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _MAPINAMEID
{
  LPGUID lpguid;
  ULONG ulKind;
  union
  {
    LONG lID;
    LPWSTR lpwstrName;
  } Kind;
} MAPINAMEID, FAR *LPMAPINAMEID;

```

## <a name="members"></a><span data-ttu-id="56ac4-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="56ac4-108">Members</span></span>

 <span data-ttu-id="56ac4-109">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="56ac4-109">**lpguid**</span></span>
  
> <span data-ttu-id="56ac4-110">Указатель на структуру [GUID,](guid.md) определяющей определенный набор свойств; этот член не может иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="56ac4-110">Pointer to a [GUID](guid.md) structure defining a particular property set; this member cannot be NULL.</span></span> <span data-ttu-id="56ac4-111">Допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="56ac4-111">Valid values are as follows:</span></span> 
    
<span data-ttu-id="56ac4-112">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="56ac4-112">PS_PUBLIC_STRINGS</span></span>
  
> 
    
<span data-ttu-id="56ac4-113">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="56ac4-113">PS_MAPI</span></span>
  
> 
    
<span data-ttu-id="56ac4-114">Определяемая клиентом величина</span><span class="sxs-lookup"><span data-stu-id="56ac4-114">A client-defined value</span></span>
  
> 
    
 <span data-ttu-id="56ac4-115">**ulKind**</span><span class="sxs-lookup"><span data-stu-id="56ac4-115">**ulKind**</span></span>
  
> <span data-ttu-id="56ac4-116">Значение, описывающие тип значения в члене **Kind.**</span><span class="sxs-lookup"><span data-stu-id="56ac4-116">Value describing the type of value in the **Kind** member.</span></span> <span data-ttu-id="56ac4-117">Допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="56ac4-117">Valid values are as follows:</span></span> 
    
<span data-ttu-id="56ac4-118">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="56ac4-118">MNID_ID</span></span> 
  
> <span data-ttu-id="56ac4-119">Член **Kind** содержит многое значение, которое представляет имя свойства.</span><span class="sxs-lookup"><span data-stu-id="56ac4-119">The **Kind** member contains an integer value that represents the property name.</span></span> 
    
<span data-ttu-id="56ac4-120">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="56ac4-120">MNID_STRING</span></span> 
  
> <span data-ttu-id="56ac4-121">Член **Kind** содержит строку символов Юникода, представляющую имя свойства.</span><span class="sxs-lookup"><span data-stu-id="56ac4-121">The **Kind** member contains a Unicode character string representing the property name.</span></span> 
    
 <span data-ttu-id="56ac4-122">**Kind**</span><span class="sxs-lookup"><span data-stu-id="56ac4-122">**Kind**</span></span>
  
> <span data-ttu-id="56ac4-123">Объединение, описывающие имя именоваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="56ac4-123">Union describing the name of the named property.</span></span> <span data-ttu-id="56ac4-124">Это может быть либо одно или несколько значений, хранимые в **коде lID,** либо строка юникода, сохраненная в **lpwstrName.**</span><span class="sxs-lookup"><span data-stu-id="56ac4-124">The name can be either an integer value, stored in **lID**, or a Unicode character string, stored in **lpwstrName**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="56ac4-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="56ac4-125">Remarks</span></span>

<span data-ttu-id="56ac4-126">Структура **MAPINAMEID** используется для описания именуемой свойства свойств с идентификаторами 0x8000.</span><span class="sxs-lookup"><span data-stu-id="56ac4-126">The **MAPINAMEID** structure is used to describe named properties properties that have identifiers over 0x8000.</span></span> <span data-ttu-id="56ac4-127">Набор свойств является важной частью именоваемом свойства.</span><span class="sxs-lookup"><span data-stu-id="56ac4-127">A property set is an important part a named property.</span></span> <span data-ttu-id="56ac4-128">Например, PS_PUBLIC_STRINGS или PS_ROUTING_ADDRTYPE это наборы свойств, определенные в MAPI.</span><span class="sxs-lookup"><span data-stu-id="56ac4-128">For example PS_PUBLIC_STRINGS or PS_ROUTING_ADDRTYPE are property sets defined by MAPI.</span></span> 
  
<span data-ttu-id="56ac4-129">Именуемые свойства позволяют клиентам определять настраиваемые свойства в большем пространстве имен, чем доступно в диапазоне идентификаторов свойств, определенных в MAPI.</span><span class="sxs-lookup"><span data-stu-id="56ac4-129">Named properties enable clients to define custom properties in a larger namespace than is available in the MAPI-defined property identifier range.</span></span> <span data-ttu-id="56ac4-130">Имена свойств нельзя использовать для непосредственного получения значений свойств; Сначала их необходимо сопооставить с идентификаторами свойств с помощью метода [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="56ac4-130">Property names cannot be used to obtain property values directly; they must first be mapped to property identifiers through the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> <span data-ttu-id="56ac4-131">Для определенных объектов, таких как сообщения, MAPI резервировать диапазон идентификаторов свойств для настраиваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="56ac4-131">For particular objects such as messages, MAPI reserves a range of property identifiers for custom properties.</span></span> <span data-ttu-id="56ac4-132">Поэтому для этих объектов клиенты не должны использовать именуемые свойства и могут сохранять связанные накладные расходы.</span><span class="sxs-lookup"><span data-stu-id="56ac4-132">Therefore, for these objects, clients do not have to use named properties and can save the associated overhead.</span></span> 
  
<span data-ttu-id="56ac4-133">Дополнительные сведения об именуемом свойстве см. [в под названием "Свойства имен".](mapi-named-properties.md)</span><span class="sxs-lookup"><span data-stu-id="56ac4-133">For more information about named properties, see [Named Properties](mapi-named-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="56ac4-134">См. также</span><span class="sxs-lookup"><span data-stu-id="56ac4-134">See also</span></span>



[<span data-ttu-id="56ac4-135">GUID</span><span class="sxs-lookup"><span data-stu-id="56ac4-135">GUID</span></span>](guid.md)
  
[<span data-ttu-id="56ac4-136">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="56ac4-136">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)


[<span data-ttu-id="56ac4-137">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="56ac4-137">MAPI Structures</span></span>](mapi-structures.md)

