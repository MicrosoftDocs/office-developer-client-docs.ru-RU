---
title: Каноническое свойство PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNextSendAcct
api_type:
- HeaderDef
ms.assetid: b7429c2e-0d9d-4921-9f56-9ecad817f8cb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 76584e248f03deac62af94e4638fcead15594b3e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581134"
---
# <a name="pidtagnextsendacct-canonical-property"></a><span data-ttu-id="45423-103">Каноническое свойство PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="45423-103">PidTagNextSendAcct Canonical Property</span></span>

  
  
<span data-ttu-id="45423-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45423-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45423-105">Указывает сервер, клиент пытается использовать для отправки электронной почты.</span><span class="sxs-lookup"><span data-stu-id="45423-105">Specifies the server that a client is currently attempting to use to send email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45423-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="45423-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45423-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="45423-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="45423-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="45423-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45423-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="45423-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="45423-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="45423-110">Data type:</span></span>  <br/> |<span data-ttu-id="45423-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="45423-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="45423-112">Область:</span><span class="sxs-lookup"><span data-stu-id="45423-112">Area:</span></span>  <br/> |<span data-ttu-id="45423-113">Приложения Outlook</span><span class="sxs-lookup"><span data-stu-id="45423-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45423-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="45423-114">Remarks</span></span>

<span data-ttu-id="45423-115">Формат этого свойства — это зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="45423-115">The format of this property is implementation dependent.</span></span> <span data-ttu-id="45423-116">Это свойство можно использовать клиента, чтобы определить, какой сервер, чтобы направить сообщение электронной почты для, но является необязательным, и значение не имеет значения для сервера.</span><span class="sxs-lookup"><span data-stu-id="45423-116">This property can be used by the client to determine which server to direct the email to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="45423-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="45423-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45423-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="45423-118">Protocol specifications</span></span>

<span data-ttu-id="45423-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45423-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45423-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="45423-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45423-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45423-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45423-122">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="45423-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="45423-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45423-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45423-124">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="45423-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45423-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="45423-125">Header files</span></span>

<span data-ttu-id="45423-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45423-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="45423-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="45423-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="45423-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="45423-128">Mapitags.h</span></span>
  
> <span data-ttu-id="45423-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="45423-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45423-130">См. также</span><span class="sxs-lookup"><span data-stu-id="45423-130">See also</span></span>



[<span data-ttu-id="45423-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="45423-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45423-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="45423-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45423-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="45423-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45423-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="45423-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

