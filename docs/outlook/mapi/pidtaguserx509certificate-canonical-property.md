---
title: Каноническое свойство PidTagUserX509Certificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserX509Certificate
api_type:
- COM
ms.assetid: 278bb9e4-3ff6-4bef-b208-7924f7a5e9b1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4e6446283116c39080271e5c2fb3ec128b25d32e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385538"
---
# <a name="pidtaguserx509certificate-canonical-property"></a><span data-ttu-id="826e8-103">Каноническое свойство PidTagUserX509Certificate</span><span class="sxs-lookup"><span data-stu-id="826e8-103">PidTagUserX509Certificate Canonical Property</span></span>

  
  
<span data-ttu-id="826e8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="826e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="826e8-105">Содержит сертификаты безопасности X.509 версии 3 для обмена сообщениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="826e8-105">Contains X.509 version 3 security certificates for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="826e8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="826e8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="826e8-107">PR_USER_X509_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="826e8-107">PR_USER_X509_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="826e8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="826e8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="826e8-109">0x3A70</span><span class="sxs-lookup"><span data-stu-id="826e8-109">0x3A70</span></span>  <br/> |
|<span data-ttu-id="826e8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="826e8-110">Data type:</span></span>  <br/> |<span data-ttu-id="826e8-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="826e8-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="826e8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="826e8-112">Area:</span></span>  <br/> |<span data-ttu-id="826e8-113">Пользователь почты MAPI</span><span class="sxs-lookup"><span data-stu-id="826e8-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="826e8-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="826e8-114">Remarks</span></span>

<span data-ttu-id="826e8-115">Это свойство используется приложений, использующих безопасности открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="826e8-115">This property is used by applications that utilize public-key security.</span></span> <span data-ttu-id="826e8-116">Он содержит двоичное представление одного или нескольких X.509 версии 3 безопасности сертификатов.</span><span class="sxs-lookup"><span data-stu-id="826e8-116">It holds a binary representation of one or more X.509 version 3 security certificates.</span></span> 
  
<span data-ttu-id="826e8-117">Это свойство можно использовать различные приложения и клиентов для свои собственные сертификаты безопасности.</span><span class="sxs-lookup"><span data-stu-id="826e8-117">Various applications and clients can use this property for their own security certificates.</span></span> <span data-ttu-id="826e8-118">Двоичный формат данных X.509 может зависеть от поставщиков.</span><span class="sxs-lookup"><span data-stu-id="826e8-118">The binary format of the X.509 data can vary among vendors.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="826e8-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="826e8-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="826e8-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="826e8-120">Protocol specifications</span></span>

<span data-ttu-id="826e8-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="826e8-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="826e8-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="826e8-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="826e8-123">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="826e8-123">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="826e8-124">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="826e8-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="826e8-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="826e8-125">Header files</span></span>

<span data-ttu-id="826e8-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="826e8-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="826e8-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="826e8-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="826e8-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="826e8-128">Mapitags.h</span></span>
  
> <span data-ttu-id="826e8-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="826e8-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="826e8-130">См. также</span><span class="sxs-lookup"><span data-stu-id="826e8-130">See also</span></span>



[<span data-ttu-id="826e8-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="826e8-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="826e8-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="826e8-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="826e8-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="826e8-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="826e8-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="826e8-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

