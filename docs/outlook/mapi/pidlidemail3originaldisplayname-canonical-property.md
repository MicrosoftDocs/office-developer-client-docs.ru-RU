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
ms.openlocfilehash: e69bcde35bcfec7746893ee18423aca3a24a6c4a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338075"
---
# <a name="pidlidemail3originaldisplayname-canonical-property"></a><span data-ttu-id="25707-103">Каноническое свойство PidLidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="25707-103">PidLidEmail3OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="25707-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25707-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25707-105">Задает третье отображаемое имя, которое соответствует адресу электронной почты, указанному для контакта.</span><span class="sxs-lookup"><span data-stu-id="25707-105">Specifies the third display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25707-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="25707-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25707-107">dispidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="25707-107">dispidEmail3OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="25707-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="25707-108">Property set:</span></span>  <br/> |<span data-ttu-id="25707-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="25707-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="25707-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="25707-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="25707-111">0x000080A4</span><span class="sxs-lookup"><span data-stu-id="25707-111">0x000080A4</span></span>  <br/> |
|<span data-ttu-id="25707-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="25707-112">Data type:</span></span>  <br/> |<span data-ttu-id="25707-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="25707-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="25707-114">Область:</span><span class="sxs-lookup"><span data-stu-id="25707-114">Area:</span></span>  <br/> |<span data-ttu-id="25707-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="25707-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25707-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="25707-116">Remarks</span></span>

<span data-ttu-id="25707-117">Если свойство **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) имеет значение "SMTP", значение соответствующего свойства **dispidEmail3OriginalDisplayName** должно равняться значению соответствующего **dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="25707-117">If the value of the **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail3OriginalDisplayName** property should equal the value of the respective **dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)).</span></span> <span data-ttu-id="25707-118">Это свойство предназначено для отображения альтернативного пользовательского адреса, эквивалентного параметру в **dispidEmail3EmailAddress**.</span><span class="sxs-lookup"><span data-stu-id="25707-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail3EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="25707-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="25707-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="25707-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="25707-120">Protocol specifications</span></span>

<span data-ttu-id="25707-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25707-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25707-122">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="25707-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="25707-123">[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25707-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25707-124">Задает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="25707-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="25707-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="25707-125">Header files</span></span>

<span data-ttu-id="25707-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="25707-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="25707-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="25707-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25707-128">См. также</span><span class="sxs-lookup"><span data-stu-id="25707-128">See also</span></span>



[<span data-ttu-id="25707-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="25707-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25707-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="25707-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25707-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="25707-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25707-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="25707-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

