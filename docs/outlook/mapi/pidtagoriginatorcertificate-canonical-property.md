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
ms.openlocfilehash: d367073de2134ff766cbae3d4f6bcfa30b862122
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351109"
---
# <a name="pidtagoriginatorcertificate-canonical-property"></a><span data-ttu-id="03fa6-103">Каноническое свойство PidTagOriginatorCertificate</span><span class="sxs-lookup"><span data-stu-id="03fa6-103">PidTagOriginatorCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="03fa6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03fa6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03fa6-105">Содержит сертификат ASN. 1 для инициатора сообщения.</span><span class="sxs-lookup"><span data-stu-id="03fa6-105">Contains an ASN.1 certificate for the message originator.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03fa6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="03fa6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03fa6-107">ПР_ОРИГИНАТОР_ЦЕРТИФИКАТЕ</span><span class="sxs-lookup"><span data-stu-id="03fa6-107">PR_ORIGINATOR_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="03fa6-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="03fa6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="03fa6-109">0x0022</span><span class="sxs-lookup"><span data-stu-id="03fa6-109">0x0022</span></span>  <br/> |
|<span data-ttu-id="03fa6-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="03fa6-110">Data type:</span></span>  <br/> |<span data-ttu-id="03fa6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="03fa6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="03fa6-112">Область:</span><span class="sxs-lookup"><span data-stu-id="03fa6-112">Area:</span></span>  <br/> |<span data-ttu-id="03fa6-113">MIME</span><span class="sxs-lookup"><span data-stu-id="03fa6-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03fa6-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="03fa6-114">Remarks</span></span>

<span data-ttu-id="03fa6-115">Это свойство является копией свойства **пр_усер_цертификате** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) создателя.</span><span class="sxs-lookup"><span data-stu-id="03fa6-115">This property is a copy of the originator's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="03fa6-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="03fa6-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="03fa6-117">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="03fa6-117">Header files</span></span>

<span data-ttu-id="03fa6-118">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="03fa6-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="03fa6-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="03fa6-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="03fa6-120">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="03fa6-120">Mapitags.h</span></span>
  
> <span data-ttu-id="03fa6-121">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="03fa6-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03fa6-122">См. также</span><span class="sxs-lookup"><span data-stu-id="03fa6-122">See also</span></span>



[<span data-ttu-id="03fa6-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="03fa6-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03fa6-124">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="03fa6-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03fa6-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="03fa6-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03fa6-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="03fa6-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

