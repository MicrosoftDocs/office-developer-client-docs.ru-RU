---
title: Каноническое свойство PidTagOriginatorCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorCertificate
api_type:
- COM
ms.assetid: 65f890d8-9d25-408e-ab29-89991278b92d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 966af9b3b3cbe52031402450be324ab6821d53ac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586580"
---
# <a name="pidtagoriginatorcertificate-canonical-property"></a><span data-ttu-id="b9cc9-103">Каноническое свойство PidTagOriginatorCertificate</span><span class="sxs-lookup"><span data-stu-id="b9cc9-103">PidTagOriginatorCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="b9cc9-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9cc9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9cc9-105">Содержит сертификат ASN.1 для этого отправитель сообщения.</span><span class="sxs-lookup"><span data-stu-id="b9cc9-105">Contains an ASN.1 certificate for the message originator.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b9cc9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b9cc9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b9cc9-107">PR_ORIGINATOR_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="b9cc9-107">PR_ORIGINATOR_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="b9cc9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b9cc9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b9cc9-109">0x0022</span><span class="sxs-lookup"><span data-stu-id="b9cc9-109">0x0022</span></span>  <br/> |
|<span data-ttu-id="b9cc9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b9cc9-110">Data type:</span></span>  <br/> |<span data-ttu-id="b9cc9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b9cc9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b9cc9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b9cc9-112">Area:</span></span>  <br/> |<span data-ttu-id="b9cc9-113">MIME</span><span class="sxs-lookup"><span data-stu-id="b9cc9-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9cc9-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b9cc9-114">Remarks</span></span>

<span data-ttu-id="b9cc9-115">Это свойство соответствует копию этого отправитель свойство **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b9cc9-115">This property is a copy of the originator's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b9cc9-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b9cc9-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b9cc9-117">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b9cc9-117">Header files</span></span>

<span data-ttu-id="b9cc9-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b9cc9-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="b9cc9-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b9cc9-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="b9cc9-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b9cc9-120">Mapitags.h</span></span>
  
> <span data-ttu-id="b9cc9-121">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="b9cc9-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b9cc9-122">См. также</span><span class="sxs-lookup"><span data-stu-id="b9cc9-122">See also</span></span>



[<span data-ttu-id="b9cc9-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b9cc9-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b9cc9-124">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b9cc9-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b9cc9-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b9cc9-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b9cc9-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b9cc9-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

