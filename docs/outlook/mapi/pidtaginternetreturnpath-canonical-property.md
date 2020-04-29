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
ms.openlocfilehash: c2d8eaf627f789c3e862a83d71e4ca2e3e55e1e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327960"
---
# <a name="pidtaginternetreturnpath-canonical-property"></a><span data-ttu-id="5f484-103">Каноническое свойство PidTagInternetReturnPath</span><span class="sxs-lookup"><span data-stu-id="5f484-103">PidTagInternetReturnPath Canonical Property</span></span>

  
  
<span data-ttu-id="5f484-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f484-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f484-105">Содержит значение поля заголовка Return-Path для многоцелевого почтового расширения Интернета (MIME).</span><span class="sxs-lookup"><span data-stu-id="5f484-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's Return-Path header field.</span></span> <span data-ttu-id="5f484-106">Адрес электронной почты отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="5f484-106">The email address of the message's sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f484-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5f484-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f484-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A PR_INTERNET_RETURN_PATH_W</span><span class="sxs-lookup"><span data-stu-id="5f484-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span></span>  <br/> |
|<span data-ttu-id="5f484-109">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5f484-109">Identifier:</span></span>  <br/> |<span data-ttu-id="5f484-110">0x1046</span><span class="sxs-lookup"><span data-stu-id="5f484-110">0x1046</span></span>  <br/> |
|<span data-ttu-id="5f484-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5f484-111">Data type:</span></span>  <br/> |<span data-ttu-id="5f484-112">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5f484-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5f484-113">Область:</span><span class="sxs-lookup"><span data-stu-id="5f484-113">Area:</span></span>  <br/> |<span data-ttu-id="5f484-114">MIME</span><span class="sxs-lookup"><span data-stu-id="5f484-114">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f484-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="5f484-115">Remarks</span></span>

<span data-ttu-id="5f484-116">Чтобы получить значение этого свойства, сначала используйте [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) , чтобы получить тег свойства, а затем укажите этот тег свойства в [IMAPIProp:: Prop](imapiprop-getprops.md) , чтобы получить значение.</span><span class="sxs-lookup"><span data-stu-id="5f484-116">To retrieve the value of this property, first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="5f484-117">При вызове [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [мапинамеид](mapinameid.md) , на которую указывает входный параметр _лпппропнамес_:</span><span class="sxs-lookup"><span data-stu-id="5f484-117">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f484-118">Лпгуид:</span><span class="sxs-lookup"><span data-stu-id="5f484-118">lpGuid:</span></span>  <br/> |<span data-ttu-id="5f484-119">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="5f484-119">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="5f484-120">Улкинд:</span><span class="sxs-lookup"><span data-stu-id="5f484-120">ulKind:</span></span>  <br/> |<span data-ttu-id="5f484-121">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="5f484-121">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="5f484-122">Тип. Лпвстрнаме:</span><span class="sxs-lookup"><span data-stu-id="5f484-122">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="5f484-123">L "Return. path"</span><span class="sxs-lookup"><span data-stu-id="5f484-123">L"return-path"</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5f484-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5f484-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5f484-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5f484-125">Protocol specifications</span></span>

<span data-ttu-id="5f484-126">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f484-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f484-127">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5f484-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5f484-128">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f484-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f484-129">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="5f484-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5f484-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5f484-130">Header files</span></span>

<span data-ttu-id="5f484-131">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="5f484-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f484-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5f484-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="5f484-133">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="5f484-133">Mapitags.h</span></span>
  
> <span data-ttu-id="5f484-134">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="5f484-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f484-135">См. также</span><span class="sxs-lookup"><span data-stu-id="5f484-135">See also</span></span>



[<span data-ttu-id="5f484-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5f484-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f484-137">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="5f484-137">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="5f484-138">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="5f484-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f484-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5f484-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f484-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5f484-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

