---
title: Каноническое свойство PidTagRecipientCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientCertificate
api_type:
- COM
ms.assetid: 7c5c749e-5463-4935-85b5-32219d06f782
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 464db3d360f6e872ac28f8d7cbec842d8b521f7e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585117"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a><span data-ttu-id="ff25f-103">Каноническое свойство PidTagRecipientCertificate</span><span class="sxs-lookup"><span data-stu-id="ff25f-103">PidTagRecipientCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="ff25f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff25f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff25f-105">Содержит сертификат ASN.1 получателя сообщения для использования в отчете.</span><span class="sxs-lookup"><span data-stu-id="ff25f-105">Contains a message recipient's ASN.1 certificate for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ff25f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ff25f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ff25f-107">PR_RECIPIENT_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="ff25f-107">PR_RECIPIENT_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="ff25f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ff25f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ff25f-109">0x0C13</span><span class="sxs-lookup"><span data-stu-id="ff25f-109">0x0C13</span></span>  <br/> |
|<span data-ttu-id="ff25f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ff25f-110">Data type:</span></span>  <br/> |<span data-ttu-id="ff25f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ff25f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ff25f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ff25f-112">Area:</span></span>  <br/> |<span data-ttu-id="ff25f-113">Получатель MAPI</span><span class="sxs-lookup"><span data-stu-id="ff25f-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff25f-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ff25f-114">Remarks</span></span>

<span data-ttu-id="ff25f-115">Это свойство соответствует копию получателя свойство **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) для использования в отчете.</span><span class="sxs-lookup"><span data-stu-id="ff25f-115">This property is a copy of the recipient's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property for use in a report.</span></span> <span data-ttu-id="ff25f-116">Используется для подтверждения инициатором, в том, что получатель фактически получено сообщение, которое не обязательно отчетов о доставке.</span><span class="sxs-lookup"><span data-stu-id="ff25f-116">It can be used to prove to the originator that the recipient actually received the message, which a delivery report does not necessarily indicate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ff25f-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ff25f-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ff25f-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ff25f-118">Header files</span></span>

<span data-ttu-id="ff25f-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ff25f-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="ff25f-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ff25f-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="ff25f-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ff25f-121">Mapitags.h</span></span>
  
> <span data-ttu-id="ff25f-122">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="ff25f-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff25f-123">См. также</span><span class="sxs-lookup"><span data-stu-id="ff25f-123">See also</span></span>



[<span data-ttu-id="ff25f-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ff25f-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ff25f-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ff25f-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ff25f-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ff25f-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ff25f-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ff25f-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

