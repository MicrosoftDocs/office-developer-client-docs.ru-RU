---
title: Каноническое свойство PidLidEmail3OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail3OriginalDisplayName
api_type:
- COM
ms.assetid: f3fa392a-c3b1-46dd-bf9b-5ce310719542
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0c85656c7e618a2329470f8326f434031726d1a2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590934"
---
# <a name="pidlidemail3originaldisplayname-canonical-property"></a><span data-ttu-id="1a81c-103">Каноническое свойство PidLidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="1a81c-103">PidLidEmail3OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="1a81c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a81c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a81c-105">Указывает, третий отображаемое имя, соответствующий адрес электронной почты, указанный для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="1a81c-105">Specifies the third display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a81c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1a81c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a81c-107">dispidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="1a81c-107">dispidEmail3OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="1a81c-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="1a81c-108">Property set:</span></span>  <br/> |<span data-ttu-id="1a81c-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="1a81c-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="1a81c-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="1a81c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1a81c-111">0x000080A4</span><span class="sxs-lookup"><span data-stu-id="1a81c-111">0x000080A4</span></span>  <br/> |
|<span data-ttu-id="1a81c-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1a81c-112">Data type:</span></span>  <br/> |<span data-ttu-id="1a81c-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1a81c-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1a81c-114">Область:</span><span class="sxs-lookup"><span data-stu-id="1a81c-114">Area:</span></span>  <br/> |<span data-ttu-id="1a81c-115">Contact</span><span class="sxs-lookup"><span data-stu-id="1a81c-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a81c-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="1a81c-116">Remarks</span></span>

<span data-ttu-id="1a81c-117">Если значение свойства **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) «SMTP», значение свойства соответствующих **dispidEmail3OriginalDisplayName** должно быть равно значение соответствующих ** dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1a81c-117">If the value of the **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail3OriginalDisplayName** property should equal the value of the respective **dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)).</span></span> <span data-ttu-id="1a81c-118">Это свойство предназначено для отображения альтернативный понятное адрес, который соответствует тому в **dispidEmail3EmailAddress**.</span><span class="sxs-lookup"><span data-stu-id="1a81c-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail3EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1a81c-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1a81c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1a81c-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1a81c-120">Protocol specifications</span></span>

<span data-ttu-id="1a81c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a81c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a81c-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1a81c-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1a81c-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a81c-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a81c-124">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="1a81c-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1a81c-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1a81c-125">Header files</span></span>

<span data-ttu-id="1a81c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a81c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a81c-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1a81c-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a81c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="1a81c-128">See also</span></span>



[<span data-ttu-id="1a81c-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1a81c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a81c-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1a81c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a81c-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1a81c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a81c-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1a81c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

