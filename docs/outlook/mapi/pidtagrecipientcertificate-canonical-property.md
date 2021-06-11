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
# <a name="pidtagrecipientcertificate-canonical-property"></a><span data-ttu-id="a737b-103">Каноническое свойство PidTagRecipientCertificate</span><span class="sxs-lookup"><span data-stu-id="a737b-103">PidTagRecipientCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="a737b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a737b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a737b-105">Содержит сертификат ASN.1 получателя сообщения для использования в отчете.</span><span class="sxs-lookup"><span data-stu-id="a737b-105">Contains a message recipient's ASN.1 certificate for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a737b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a737b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a737b-107">PR_RECIPIENT_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="a737b-107">PR_RECIPIENT_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="a737b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a737b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a737b-109">0x0C13</span><span class="sxs-lookup"><span data-stu-id="a737b-109">0x0C13</span></span>  <br/> |
|<span data-ttu-id="a737b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a737b-110">Data type:</span></span>  <br/> |<span data-ttu-id="a737b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a737b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a737b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a737b-112">Area:</span></span>  <br/> |<span data-ttu-id="a737b-113">Получатель MAPI</span><span class="sxs-lookup"><span data-stu-id="a737b-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a737b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a737b-114">Remarks</span></span>

<span data-ttu-id="a737b-115">Это свойство является копией свойства  PR_USER_CERTIFICATE[(PidTagUserCertificate)](pidtagusercertificate-canonical-property.md)для использования в отчете.</span><span class="sxs-lookup"><span data-stu-id="a737b-115">This property is a copy of the recipient's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property for use in a report.</span></span> <span data-ttu-id="a737b-116">Его можно использовать для того, чтобы доказать, что получатель действительно получил сообщение, которое в отчете о доставке не обязательно указывается.</span><span class="sxs-lookup"><span data-stu-id="a737b-116">It can be used to prove to the originator that the recipient actually received the message, which a delivery report does not necessarily indicate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a737b-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a737b-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a737b-118">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="a737b-118">Header files</span></span>

<span data-ttu-id="a737b-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a737b-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="a737b-120">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a737b-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="a737b-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a737b-121">Mapitags.h</span></span>
  
> <span data-ttu-id="a737b-122">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="a737b-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a737b-123">См. также</span><span class="sxs-lookup"><span data-stu-id="a737b-123">See also</span></span>



[<span data-ttu-id="a737b-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a737b-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a737b-125">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a737b-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a737b-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a737b-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a737b-127">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="a737b-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

