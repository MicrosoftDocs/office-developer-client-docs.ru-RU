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
# <a name="mapinameid"></a><span data-ttu-id="7f604-103">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="7f604-103">MAPINAMEID</span></span>

  
  
<span data-ttu-id="7f604-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f604-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f604-105">Описывает именованное свойство.</span><span class="sxs-lookup"><span data-stu-id="7f604-105">Describes a named property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f604-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7f604-106">Header file:</span></span>  <br/> |<span data-ttu-id="7f604-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="7f604-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="7f604-108">Members</span><span class="sxs-lookup"><span data-stu-id="7f604-108">Members</span></span>

 <span data-ttu-id="7f604-109">**лпгуид**</span><span class="sxs-lookup"><span data-stu-id="7f604-109">**lpguid**</span></span>
  
> <span data-ttu-id="7f604-110">Указатель на структуру [GUID](guid.md) , определяющую определенный набор свойств; Этот элемент не может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="7f604-110">Pointer to a [GUID](guid.md) structure defining a particular property set; this member cannot be NULL.</span></span> <span data-ttu-id="7f604-111">Допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7f604-111">Valid values are as follows:</span></span> 
    
<span data-ttu-id="7f604-112">ПС_ПУБЛИК_СТРИНГС</span><span class="sxs-lookup"><span data-stu-id="7f604-112">PS_PUBLIC_STRINGS</span></span>
  
> 
    
<span data-ttu-id="7f604-113">ПС_МАПИ</span><span class="sxs-lookup"><span data-stu-id="7f604-113">PS_MAPI</span></span>
  
> 
    
<span data-ttu-id="7f604-114">Значение, определяемое клиентом</span><span class="sxs-lookup"><span data-stu-id="7f604-114">A client-defined value</span></span>
  
> 
    
 <span data-ttu-id="7f604-115">**Улкинд**</span><span class="sxs-lookup"><span data-stu-id="7f604-115">**ulKind**</span></span>
  
> <span data-ttu-id="7f604-116">Значение, описывающее тип значения в члене **типа** .</span><span class="sxs-lookup"><span data-stu-id="7f604-116">Value describing the type of value in the **Kind** member.</span></span> <span data-ttu-id="7f604-117">Допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7f604-117">Valid values are as follows:</span></span> 
    
<span data-ttu-id="7f604-118">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="7f604-118">MNID_ID</span></span> 
  
> <span data-ttu-id="7f604-119">Элемент **Kind** содержит целое значение, представляющее имя свойства.</span><span class="sxs-lookup"><span data-stu-id="7f604-119">The **Kind** member contains an integer value that represents the property name.</span></span> 
    
<span data-ttu-id="7f604-120">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="7f604-120">MNID_STRING</span></span> 
  
> <span data-ttu-id="7f604-121">Элемент **Kind** содержит строку символов Юникода, представляющую имя свойства.</span><span class="sxs-lookup"><span data-stu-id="7f604-121">The **Kind** member contains a Unicode character string representing the property name.</span></span> 
    
 <span data-ttu-id="7f604-122">**Kind**</span><span class="sxs-lookup"><span data-stu-id="7f604-122">**Kind**</span></span>
  
> <span data-ttu-id="7f604-123">Union, описывающий имя именованного свойства.</span><span class="sxs-lookup"><span data-stu-id="7f604-123">Union describing the name of the named property.</span></span> <span data-ttu-id="7f604-124">Имя может быть целым числом, хранящимся в **крышки**, или строкой символов Юникода, хранящимся в **лпвстрнаме**.</span><span class="sxs-lookup"><span data-stu-id="7f604-124">The name can be either an integer value, stored in **lID**, or a Unicode character string, stored in **lpwstrName**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7f604-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="7f604-125">Remarks</span></span>

<span data-ttu-id="7f604-126">Структура **мапинамеид** используется для описания свойств именованных свойств, идентификаторы которых превыше 0x8000.</span><span class="sxs-lookup"><span data-stu-id="7f604-126">The **MAPINAMEID** structure is used to describe named properties properties that have identifiers over 0x8000.</span></span> <span data-ttu-id="7f604-127">Набор свойств является важной частью именованного свойства.</span><span class="sxs-lookup"><span data-stu-id="7f604-127">A property set is an important part a named property.</span></span> <span data-ttu-id="7f604-128">Например, ПС_ПУБЛИК_СТРИНГС или ПС_РАУТИНГ_АДДРТИПЕ — это наборы свойств, определенные MAPI.</span><span class="sxs-lookup"><span data-stu-id="7f604-128">For example PS_PUBLIC_STRINGS or PS_ROUTING_ADDRTYPE are property sets defined by MAPI.</span></span> 
  
<span data-ttu-id="7f604-129">Именованные свойства позволяют клиентам определять настраиваемые свойства в пространстве имен, превышающем доступное в диапазоне идентификаторов свойств, заданных MAPI.</span><span class="sxs-lookup"><span data-stu-id="7f604-129">Named properties enable clients to define custom properties in a larger namespace than is available in the MAPI-defined property identifier range.</span></span> <span data-ttu-id="7f604-130">Имена свойств нельзя использовать для непосредственного получения значений свойств; Сначала они должны быть сопоставлены с идентификаторами свойств с помощью метода [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="7f604-130">Property names cannot be used to obtain property values directly; they must first be mapped to property identifiers through the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> <span data-ttu-id="7f604-131">Для определенных объектов, например сообщений, в MAPI резервируется диапазон идентификаторов свойств для настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="7f604-131">For particular objects such as messages, MAPI reserves a range of property identifiers for custom properties.</span></span> <span data-ttu-id="7f604-132">Таким образом, для этих объектов клиентам не нужно использовать именованные свойства и могут сохранять связанные издержки.</span><span class="sxs-lookup"><span data-stu-id="7f604-132">Therefore, for these objects, clients do not have to use named properties and can save the associated overhead.</span></span> 
  
<span data-ttu-id="7f604-133">Более подробную информацию об именованных свойствах можно узнать в статье [именованНые свойства](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="7f604-133">For more information about named properties, see [Named Properties](mapi-named-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7f604-134">См. также</span><span class="sxs-lookup"><span data-stu-id="7f604-134">See also</span></span>



[<span data-ttu-id="7f604-135">GUID</span><span class="sxs-lookup"><span data-stu-id="7f604-135">GUID</span></span>](guid.md)
  
[<span data-ttu-id="7f604-136">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="7f604-136">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)


[<span data-ttu-id="7f604-137">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="7f604-137">MAPI Structures</span></span>](mapi-structures.md)

