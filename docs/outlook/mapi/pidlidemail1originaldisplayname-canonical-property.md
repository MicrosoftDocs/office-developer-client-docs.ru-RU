---
title: Каноническое свойство PidLidEmail1OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail1OriginalDisplayName
api_type:
- COM
ms.assetid: 991c2969-0180-4c7d-95ee-e62fd24d67ef
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a20ae8e3f19073bfb88d58db516a0e5f93d91445
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399867"
---
# <a name="pidlidemail1originaldisplayname-canonical-property"></a><span data-ttu-id="494ad-103">Каноническое свойство PidLidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="494ad-103">PidLidEmail1OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="494ad-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="494ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="494ad-105">Задает первый отображаемое имя, соответствующий адрес электронной почты, указанный для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="494ad-105">Specifies the first display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="494ad-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="494ad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="494ad-107">dispidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="494ad-107">dispidEmail1OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="494ad-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="494ad-108">Property set:</span></span>  <br/> |<span data-ttu-id="494ad-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="494ad-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="494ad-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="494ad-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="494ad-111">0x00008084</span><span class="sxs-lookup"><span data-stu-id="494ad-111">0x00008084</span></span>  <br/> |
|<span data-ttu-id="494ad-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="494ad-112">Data type:</span></span>  <br/> |<span data-ttu-id="494ad-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="494ad-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="494ad-114">Область:</span><span class="sxs-lookup"><span data-stu-id="494ad-114">Area:</span></span>  <br/> |<span data-ttu-id="494ad-115">Contact</span><span class="sxs-lookup"><span data-stu-id="494ad-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="494ad-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="494ad-116">Remarks</span></span>

<span data-ttu-id="494ad-117">Если значение свойства **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) «SMTP», значение свойства соответствующих **dispidEmail1OriginalDisplayName** должно быть равно значение соответствующих \*\* dispidEmail1EmailAddress\*\* свойство ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="494ad-117">If the value of the **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail1OriginalDisplayName** property should equal the value of the respective **dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="494ad-118">Это свойство отображает понятное альтернативный адрес, который соответствует тому в свойстве **dispidEmail1EmailAddress** .</span><span class="sxs-lookup"><span data-stu-id="494ad-118">This property displays an alternative user-friendly address that is equivalent to the one in the **dispidEmail1EmailAddress** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="494ad-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="494ad-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="494ad-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="494ad-120">Protocol specifications</span></span>

<span data-ttu-id="494ad-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="494ad-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="494ad-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="494ad-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="494ad-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="494ad-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="494ad-124">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="494ad-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="494ad-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="494ad-125">Header files</span></span>

<span data-ttu-id="494ad-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="494ad-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="494ad-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="494ad-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="494ad-128">См. также</span><span class="sxs-lookup"><span data-stu-id="494ad-128">See also</span></span>



[<span data-ttu-id="494ad-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="494ad-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="494ad-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="494ad-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="494ad-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="494ad-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="494ad-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="494ad-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

