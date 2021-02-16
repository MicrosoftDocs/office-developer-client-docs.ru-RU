---
title: Каноническое свойство PidTagUserCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserCertificate
api_type:
- COM
ms.assetid: 2ac14c43-36c1-4f2f-97b0-2462f2360575
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 53ee4019752cf717840199d4a51cbc90133b8636
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320393"
---
# <a name="pidtagusercertificate-canonical-property"></a><span data-ttu-id="6e851-103">Каноническое свойство PidTagUserCertificate</span><span class="sxs-lookup"><span data-stu-id="6e851-103">PidTagUserCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="6e851-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e851-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e851-105">Содержит сертификат проверки подлинности ASN.1 для пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="6e851-105">Contains an ASN.1 authentication certificate for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e851-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6e851-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e851-107">PR_USER_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="6e851-107">PR_USER_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="6e851-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6e851-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6e851-109">0x3A22</span><span class="sxs-lookup"><span data-stu-id="6e851-109">0x3A22</span></span>  <br/> |
|<span data-ttu-id="6e851-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6e851-110">Data type:</span></span>  <br/> |<span data-ttu-id="6e851-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6e851-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6e851-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6e851-112">Area:</span></span>  <br/> |<span data-ttu-id="6e851-113">Пользователь почты MAPI</span><span class="sxs-lookup"><span data-stu-id="6e851-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e851-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6e851-114">Remarks</span></span>

<span data-ttu-id="6e851-115">Сертификат проверки подлинности похож на цифровую подпись.</span><span class="sxs-lookup"><span data-stu-id="6e851-115">An authentication certificate is similar to a digital signature.</span></span> <span data-ttu-id="6e851-116">Некоторые свойства MAPI имеют сертификаты ASN.1.</span><span class="sxs-lookup"><span data-stu-id="6e851-116">Several MAPI properties supply ASN.1 certificates.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6e851-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6e851-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e851-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6e851-118">Protocol specifications</span></span>

<span data-ttu-id="6e851-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e851-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e851-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="6e851-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6e851-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e851-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e851-122">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6e851-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e851-123">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="6e851-123">Header files</span></span>

<span data-ttu-id="6e851-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e851-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e851-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6e851-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="6e851-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6e851-126">Mapitags.h</span></span>
  
> <span data-ttu-id="6e851-127">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="6e851-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e851-128">См. также</span><span class="sxs-lookup"><span data-stu-id="6e851-128">See also</span></span>



[<span data-ttu-id="6e851-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6e851-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e851-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6e851-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e851-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6e851-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e851-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6e851-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

