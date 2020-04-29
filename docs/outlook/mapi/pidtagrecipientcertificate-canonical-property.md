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
ms.openlocfilehash: c659b77767fddc4c783732082c2eb65c68af8dbf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431668"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a><span data-ttu-id="0b233-103">Каноническое свойство PidTagRecipientCertificate</span><span class="sxs-lookup"><span data-stu-id="0b233-103">PidTagRecipientCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="0b233-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b233-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b233-105">Содержит сертификат получателя сообщения ASN. 1 получателя, который будет использоваться в отчете.</span><span class="sxs-lookup"><span data-stu-id="0b233-105">Contains a message recipient's ASN.1 certificate for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0b233-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0b233-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b233-107">PR_RECIPIENT_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="0b233-107">PR_RECIPIENT_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="0b233-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0b233-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0b233-109">0x0C13</span><span class="sxs-lookup"><span data-stu-id="0b233-109">0x0C13</span></span>  <br/> |
|<span data-ttu-id="0b233-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0b233-110">Data type:</span></span>  <br/> |<span data-ttu-id="0b233-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0b233-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0b233-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0b233-112">Area:</span></span>  <br/> |<span data-ttu-id="0b233-113">Получатель MAPI</span><span class="sxs-lookup"><span data-stu-id="0b233-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b233-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0b233-114">Remarks</span></span>

<span data-ttu-id="0b233-115">Это свойство является копией свойства **PR_USER_CERTIFICATE** получателя ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) для использования в отчете.</span><span class="sxs-lookup"><span data-stu-id="0b233-115">This property is a copy of the recipient's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property for use in a report.</span></span> <span data-ttu-id="0b233-116">Его можно использовать, чтобы доказать инициатор, который фактически получал сообщение, что отчет о доставке не обязательно указывает.</span><span class="sxs-lookup"><span data-stu-id="0b233-116">It can be used to prove to the originator that the recipient actually received the message, which a delivery report does not necessarily indicate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0b233-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0b233-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0b233-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0b233-118">Header files</span></span>

<span data-ttu-id="0b233-119">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="0b233-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b233-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0b233-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="0b233-121">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="0b233-121">Mapitags.h</span></span>
  
> <span data-ttu-id="0b233-122">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="0b233-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b233-123">См. также</span><span class="sxs-lookup"><span data-stu-id="0b233-123">See also</span></span>



[<span data-ttu-id="0b233-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0b233-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b233-125">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="0b233-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b233-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0b233-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b233-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0b233-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

