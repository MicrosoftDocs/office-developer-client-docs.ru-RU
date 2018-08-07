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
ms.openlocfilehash: 0dd477a055562f692c8869bc436c4238c77fd02a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812038"
---
# <a name="pidtagusercertificate-canonical-property"></a><span data-ttu-id="a1ca3-103">Каноническое свойство PidTagUserCertificate</span><span class="sxs-lookup"><span data-stu-id="a1ca3-103">PidTagUserCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="a1ca3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a1ca3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a1ca3-105">Содержит сертификат подлинности ASN.1 для обмена сообщениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="a1ca3-105">Contains an ASN.1 authentication certificate for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1ca3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a1ca3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1ca3-107">PR_USER_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="a1ca3-107">PR_USER_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="a1ca3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a1ca3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a1ca3-109">0x3A22</span><span class="sxs-lookup"><span data-stu-id="a1ca3-109">0x3A22</span></span>  <br/> |
|<span data-ttu-id="a1ca3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a1ca3-110">Data type:</span></span>  <br/> |<span data-ttu-id="a1ca3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a1ca3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a1ca3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a1ca3-112">Area:</span></span>  <br/> |<span data-ttu-id="a1ca3-113">Пользователь почты MAPI</span><span class="sxs-lookup"><span data-stu-id="a1ca3-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1ca3-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a1ca3-114">Remarks</span></span>

<span data-ttu-id="a1ca3-115">Сертификат подлинности аналогична цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="a1ca3-115">An authentication certificate is similar to a digital signature.</span></span> <span data-ttu-id="a1ca3-116">Несколько свойств MAPI предоставить ASN.1 сертификаты.</span><span class="sxs-lookup"><span data-stu-id="a1ca3-116">Several MAPI properties supply ASN.1 certificates.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a1ca3-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a1ca3-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a1ca3-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a1ca3-118">Protocol specifications</span></span>

<span data-ttu-id="a1ca3-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1ca3-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1ca3-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a1ca3-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a1ca3-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1ca3-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1ca3-122">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1ca3-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a1ca3-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a1ca3-123">Header files</span></span>

<span data-ttu-id="a1ca3-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1ca3-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1ca3-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a1ca3-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="a1ca3-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a1ca3-126">Mapitags.h</span></span>
  
> <span data-ttu-id="a1ca3-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a1ca3-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1ca3-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a1ca3-128">See also</span></span>



[<span data-ttu-id="a1ca3-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a1ca3-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1ca3-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a1ca3-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1ca3-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a1ca3-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1ca3-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a1ca3-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

