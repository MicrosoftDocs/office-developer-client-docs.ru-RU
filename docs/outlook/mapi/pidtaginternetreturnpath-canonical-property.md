---
title: Каноническое свойство PidTagInternetReturnPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReturnPath
api_type:
- HeaderDef
ms.assetid: 4530dbcf-9436-4f29-b79e-1bb0f791f60b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: aa8a683c0033682aa46944c5cc78503dc1a7d729
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811256"
---
# <a name="pidtaginternetreturnpath-canonical-property"></a><span data-ttu-id="8e1d2-103">Каноническое свойство PidTagInternetReturnPath</span><span class="sxs-lookup"><span data-stu-id="8e1d2-103">PidTagInternetReturnPath Canonical Property</span></span>

  
  
<span data-ttu-id="8e1d2-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e1d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e1d2-105">Содержит значение поля заголовка сообщения Multipurpose Internet Mail Extensions (MIME) возврата пути.</span><span class="sxs-lookup"><span data-stu-id="8e1d2-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's Return-Path header field.</span></span> <span data-ttu-id="8e1d2-106">Адрес электронной почты отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="8e1d2-106">The email address of the message's sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e1d2-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8e1d2-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e1d2-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span><span class="sxs-lookup"><span data-stu-id="8e1d2-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span></span>  <br/> |
|<span data-ttu-id="8e1d2-109">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8e1d2-109">Identifier:</span></span>  <br/> |<span data-ttu-id="8e1d2-110">0x1046</span><span class="sxs-lookup"><span data-stu-id="8e1d2-110">0x1046</span></span>  <br/> |
|<span data-ttu-id="8e1d2-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8e1d2-111">Data type:</span></span>  <br/> |<span data-ttu-id="8e1d2-112">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8e1d2-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8e1d2-113">Область:</span><span class="sxs-lookup"><span data-stu-id="8e1d2-113">Area:</span></span>  <br/> |<span data-ttu-id="8e1d2-114">MIME</span><span class="sxs-lookup"><span data-stu-id="8e1d2-114">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e1d2-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="8e1d2-115">Remarks</span></span>

<span data-ttu-id="8e1d2-116">Чтобы получить значение этого свойства, сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства и укажите этот тег свойства в [IMAPIProp::GetProps](imapiprop-getprops.md) для получения значения.</span><span class="sxs-lookup"><span data-stu-id="8e1d2-116">To retrieve the value of this property, first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="8e1d2-117">При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), укажите следующие значения для структуры [MAPINAMEID](mapinameid.md) , на которую указывает входного параметра _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="8e1d2-117">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e1d2-118">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="8e1d2-118">lpGuid:</span></span>  <br/> |<span data-ttu-id="8e1d2-119">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="8e1d2-119">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="8e1d2-120">ulKind:</span><span class="sxs-lookup"><span data-stu-id="8e1d2-120">ulKind:</span></span>  <br/> |<span data-ttu-id="8e1d2-121">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="8e1d2-121">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="8e1d2-122">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="8e1d2-122">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="8e1d2-123">L «возврат пути»</span><span class="sxs-lookup"><span data-stu-id="8e1d2-123">L"return-path"</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8e1d2-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8e1d2-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8e1d2-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8e1d2-125">Protocol specifications</span></span>

<span data-ttu-id="8e1d2-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e1d2-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e1d2-127">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8e1d2-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8e1d2-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e1d2-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e1d2-129">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="8e1d2-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8e1d2-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8e1d2-130">Header files</span></span>

<span data-ttu-id="8e1d2-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e1d2-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e1d2-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8e1d2-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="8e1d2-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8e1d2-133">Mapitags.h</span></span>
  
> <span data-ttu-id="8e1d2-134">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="8e1d2-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e1d2-135">См. также</span><span class="sxs-lookup"><span data-stu-id="8e1d2-135">See also</span></span>



[<span data-ttu-id="8e1d2-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8e1d2-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e1d2-137">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="8e1d2-137">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="8e1d2-138">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8e1d2-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e1d2-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8e1d2-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e1d2-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8e1d2-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

