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
ms.openlocfilehash: bb51e9a602bd5c2e59bb56fdbf44fddc39651de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811663"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a><span data-ttu-id="dc363-103">Каноническое свойство PidTagRecipientCertificate</span><span class="sxs-lookup"><span data-stu-id="dc363-103">PidTagRecipientCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="dc363-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dc363-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dc363-105">Содержит сертификат ASN.1 получателя сообщения для использования в отчете.</span><span class="sxs-lookup"><span data-stu-id="dc363-105">Contains a message recipient's ASN.1 certificate for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dc363-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="dc363-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dc363-107">PR_RECIPIENT_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="dc363-107">PR_RECIPIENT_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="dc363-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="dc363-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dc363-109">0x0C13</span><span class="sxs-lookup"><span data-stu-id="dc363-109">0x0C13</span></span>  <br/> |
|<span data-ttu-id="dc363-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="dc363-110">Data type:</span></span>  <br/> |<span data-ttu-id="dc363-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="dc363-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="dc363-112">Область:</span><span class="sxs-lookup"><span data-stu-id="dc363-112">Area:</span></span>  <br/> |<span data-ttu-id="dc363-113">Получатель MAPI</span><span class="sxs-lookup"><span data-stu-id="dc363-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc363-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="dc363-114">Remarks</span></span>

<span data-ttu-id="dc363-115">Это свойство соответствует копию получателя свойство **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) для использования в отчете.</span><span class="sxs-lookup"><span data-stu-id="dc363-115">This property is a copy of the recipient's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property for use in a report.</span></span> <span data-ttu-id="dc363-116">Используется для подтверждения инициатором, в том, что получатель фактически получено сообщение, которое не обязательно отчетов о доставке.</span><span class="sxs-lookup"><span data-stu-id="dc363-116">It can be used to prove to the originator that the recipient actually received the message, which a delivery report does not necessarily indicate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dc363-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dc363-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="dc363-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="dc363-118">Header files</span></span>

<span data-ttu-id="dc363-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc363-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="dc363-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="dc363-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="dc363-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dc363-121">Mapitags.h</span></span>
  
> <span data-ttu-id="dc363-122">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="dc363-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc363-123">См. также</span><span class="sxs-lookup"><span data-stu-id="dc363-123">See also</span></span>



[<span data-ttu-id="dc363-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dc363-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dc363-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dc363-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dc363-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="dc363-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dc363-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="dc363-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

