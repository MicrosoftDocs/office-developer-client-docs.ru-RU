---
title: Каноническое свойство PidTagAttachPayloadProviderGuidString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadProviderGuidString
api_type:
- HeaderDef
ms.assetid: c9d4b561-53b3-492b-9324-9376dd7abddf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1313ac62bd2ee6c1db27bd1c583f56dadc1bff1e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574302"
---
# <a name="pidtagattachpayloadproviderguidstring-canonical-property"></a><span data-ttu-id="452ce-103">Каноническое свойство PidTagAttachPayloadProviderGuidString</span><span class="sxs-lookup"><span data-stu-id="452ce-103">PidTagAttachPayloadProviderGuidString Canonical Property</span></span>

  
  
<span data-ttu-id="452ce-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="452ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="452ce-105">Содержит значение поля заголовка X MIME-полезной нагрузки-поставщика-Guid.</span><span class="sxs-lookup"><span data-stu-id="452ce-105">Contains the value of a MIME X-Payload-Provider-Guid header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="452ce-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="452ce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="452ce-107">PR_ATTACH_PAYLOAD_PROV_GUID_STR, PR_ATTACH_PAYLOAD_PROV_GUID_STR_A, PR_ATTACH_PAYLOAD_PROV_GUID_STR_W</span><span class="sxs-lookup"><span data-stu-id="452ce-107">PR_ATTACH_PAYLOAD_PROV_GUID_STR, PR_ATTACH_PAYLOAD_PROV_GUID_STR_A, PR_ATTACH_PAYLOAD_PROV_GUID_STR_W</span></span>  <br/> |
|<span data-ttu-id="452ce-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="452ce-108">Identifier:</span></span>  <br/> |<span data-ttu-id="452ce-109">0x3719</span><span class="sxs-lookup"><span data-stu-id="452ce-109">0x3719</span></span>  <br/> |
|<span data-ttu-id="452ce-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="452ce-110">Data type:</span></span>  <br/> |<span data-ttu-id="452ce-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="452ce-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="452ce-112">Область:</span><span class="sxs-lookup"><span data-stu-id="452ce-112">Area:</span></span>  <br/> |<span data-ttu-id="452ce-113">Приложения Outlook</span><span class="sxs-lookup"><span data-stu-id="452ce-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="452ce-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="452ce-114">Remarks</span></span>

<span data-ttu-id="452ce-115">Чтобы задать значения этих свойств, клиенты MIME указывайте поле заголовка X--поставщика — код Guid полезных данных MIME лицо, которое будет анализироваться как вложение.</span><span class="sxs-lookup"><span data-stu-id="452ce-115">To set the value of these properties, MIME clients should write an X-Payload-Provider-Guid header field to a MIME entity that will be analyzed as an attachment.</span></span>
  
<span data-ttu-id="452ce-116">Читатели MIME, должен скопировать это значение поля заголовка на значение соответствующего свойства.</span><span class="sxs-lookup"><span data-stu-id="452ce-116">MIME readers must copy this header field value to the value of the corresponding property.</span></span> <span data-ttu-id="452ce-117">Читатели MIME следует игнорировать это поле заголовка при его отображении в сущности MIME, анализируется как сообщение или текст сообщения, а не как вложение.</span><span class="sxs-lookup"><span data-stu-id="452ce-117">MIME readers should ignore this header field when it appears on a MIME entity that is analyzed as a message or message body, rather than as an attachment.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="452ce-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="452ce-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="452ce-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="452ce-119">Protocol specifications</span></span>

<span data-ttu-id="452ce-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="452ce-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="452ce-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="452ce-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="452ce-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="452ce-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="452ce-123">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="452ce-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="452ce-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="452ce-124">Header files</span></span>

<span data-ttu-id="452ce-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="452ce-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="452ce-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="452ce-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="452ce-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="452ce-127">Mapitags.h</span></span>
  
> <span data-ttu-id="452ce-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="452ce-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="452ce-129">См. также</span><span class="sxs-lookup"><span data-stu-id="452ce-129">See also</span></span>



[<span data-ttu-id="452ce-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="452ce-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="452ce-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="452ce-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="452ce-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="452ce-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="452ce-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="452ce-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

