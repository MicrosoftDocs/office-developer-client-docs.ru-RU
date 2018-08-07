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
ms.openlocfilehash: c3a21e8a6e69cae9d8b757a60fe56d63e079b3ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809875"
---
# <a name="mapinameid"></a><span data-ttu-id="42eff-103">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="42eff-103">MAPINAMEID</span></span>

  
  
<span data-ttu-id="42eff-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="42eff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="42eff-105">Описывает именованное свойство.</span><span class="sxs-lookup"><span data-stu-id="42eff-105">Describes a named property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42eff-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="42eff-106">Header file:</span></span>  <br/> |<span data-ttu-id="42eff-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="42eff-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="42eff-108">Members</span><span class="sxs-lookup"><span data-stu-id="42eff-108">Members</span></span>

 <span data-ttu-id="42eff-109">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="42eff-109">**lpguid**</span></span>
  
> <span data-ttu-id="42eff-110">Установите указатель на структуру [идентификатор GUID](guid.md) , определяющий определенное свойство; Этот член не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="42eff-110">Pointer to a [GUID](guid.md) structure defining a particular property set; this member cannot be NULL.</span></span> <span data-ttu-id="42eff-111">Допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="42eff-111">Valid values are as follows:</span></span> 
    
<span data-ttu-id="42eff-112">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="42eff-112">PS_PUBLIC_STRINGS</span></span>
  
> 
    
<span data-ttu-id="42eff-113">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="42eff-113">PS_MAPI</span></span>
  
> 
    
<span data-ttu-id="42eff-114">Определенное значение клиента</span><span class="sxs-lookup"><span data-stu-id="42eff-114">A client-defined value</span></span>
  
> 
    
 <span data-ttu-id="42eff-115">**ulKind**</span><span class="sxs-lookup"><span data-stu-id="42eff-115">**ulKind**</span></span>
  
> <span data-ttu-id="42eff-116">Значение, указывающее тип значения в **Тип** элемента.</span><span class="sxs-lookup"><span data-stu-id="42eff-116">Value describing the type of value in the **Kind** member.</span></span> <span data-ttu-id="42eff-117">Допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="42eff-117">Valid values are as follows:</span></span> 
    
<span data-ttu-id="42eff-118">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="42eff-118">MNID_ID</span></span> 
  
> <span data-ttu-id="42eff-119">Член **типа** содержит целое число, представляющее имя свойства.</span><span class="sxs-lookup"><span data-stu-id="42eff-119">The **Kind** member contains an integer value that represents the property name.</span></span> 
    
<span data-ttu-id="42eff-120">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="42eff-120">MNID_STRING</span></span> 
  
> <span data-ttu-id="42eff-121">Член **типа** содержит строку символ Unicode, представляющую имя свойства.</span><span class="sxs-lookup"><span data-stu-id="42eff-121">The **Kind** member contains a Unicode character string representing the property name.</span></span> 
    
 <span data-ttu-id="42eff-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="42eff-122">**Kind**</span></span>
  
> <span data-ttu-id="42eff-123">Объединение, описывающую имя именованное свойство.</span><span class="sxs-lookup"><span data-stu-id="42eff-123">Union describing the name of the named property.</span></span> <span data-ttu-id="42eff-124">Имя может быть целое число, хранящиеся в **крышку**, или строка символов Юникод, хранящиеся в **lpwstrName**.</span><span class="sxs-lookup"><span data-stu-id="42eff-124">The name can be either an integer value, stored in **lID**, or a Unicode character string, stored in **lpwstrName**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="42eff-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="42eff-125">Remarks</span></span>

<span data-ttu-id="42eff-126">Структура **MAPINAMEID** используется для описания свойства именованных свойств, имеющие идентификаторы свыше 0x8000.</span><span class="sxs-lookup"><span data-stu-id="42eff-126">The **MAPINAMEID** structure is used to describe named properties properties that have identifiers over 0x8000.</span></span> <span data-ttu-id="42eff-127">Набор свойств — важная часть именованное свойство.</span><span class="sxs-lookup"><span data-stu-id="42eff-127">A property set is an important part a named property.</span></span> <span data-ttu-id="42eff-128">К примеру PS_PUBLIC_STRINGS или PS_ROUTING_ADDRTYPE, наборы свойств, определенные в MAPI.</span><span class="sxs-lookup"><span data-stu-id="42eff-128">For example PS_PUBLIC_STRINGS or PS_ROUTING_ADDRTYPE are property sets defined by MAPI.</span></span> 
  
<span data-ttu-id="42eff-129">Именованные свойства для предоставления клиентам для определения пользовательских свойств в пространстве имен больше, чем доступно в диапазоне идентификатор MAPI определенные свойства.</span><span class="sxs-lookup"><span data-stu-id="42eff-129">Named properties enable clients to define custom properties in a larger namespace than is available in the MAPI-defined property identifier range.</span></span> <span data-ttu-id="42eff-130">Имена свойств не может использоваться для получения значения свойств напрямую. они сначала должны сопоставляться с идентификаторами свойство через метод [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="42eff-130">Property names cannot be used to obtain property values directly; they must first be mapped to property identifiers through the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> <span data-ttu-id="42eff-131">Для определенных объектов, такие как сообщения MAPI оставляет за собой диапазон идентификаторов свойств для настраиваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="42eff-131">For particular objects such as messages, MAPI reserves a range of property identifiers for custom properties.</span></span> <span data-ttu-id="42eff-132">Таким образом, для этих объектов клиентов нет необходимости использовать именованные свойства и можно сохранить связанные накладные расходы.</span><span class="sxs-lookup"><span data-stu-id="42eff-132">Therefore, for these objects, clients do not have to use named properties and can save the associated overhead.</span></span> 
  
<span data-ttu-id="42eff-133">Дополнительные сведения об именованных свойств в разделе [Свойства с именем](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="42eff-133">For more information about named properties, see [Named Properties](mapi-named-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="42eff-134">См. также</span><span class="sxs-lookup"><span data-stu-id="42eff-134">See also</span></span>



[<span data-ttu-id="42eff-135">GUID</span><span class="sxs-lookup"><span data-stu-id="42eff-135">GUID</span></span>](guid.md)
  
[<span data-ttu-id="42eff-136">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="42eff-136">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)


[<span data-ttu-id="42eff-137">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="42eff-137">MAPI Structures</span></span>](mapi-structures.md)

