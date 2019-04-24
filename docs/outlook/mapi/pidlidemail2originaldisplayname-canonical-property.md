---
title: Каноническое свойство PidLidEmail2OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail2OriginalDisplayName
api_type:
- COM
ms.assetid: 0b648ef6-86ed-40ee-b068-8fcde7e0fe75
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7fb7e5afa6a1c050a5d91274bc4f82439fb98640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337963"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a><span data-ttu-id="de70f-103">Каноническое свойство PidLidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="de70f-103">PidLidEmail2OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="de70f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de70f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de70f-105">Задает второе отображаемое имя, которое соответствует адресу электронной почты, указанному для контакта.</span><span class="sxs-lookup"><span data-stu-id="de70f-105">Specifies the second display name that corresponds to the email address specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="de70f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="de70f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de70f-107">dispidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="de70f-107">dispidEmail2OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="de70f-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="de70f-108">Property set:</span></span>  <br/> |<span data-ttu-id="de70f-109">Псетид_аддресс</span><span class="sxs-lookup"><span data-stu-id="de70f-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="de70f-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="de70f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="de70f-111">0x00008094</span><span class="sxs-lookup"><span data-stu-id="de70f-111">0x00008094</span></span>  <br/> |
|<span data-ttu-id="de70f-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="de70f-112">Data type:</span></span>  <br/> |<span data-ttu-id="de70f-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="de70f-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="de70f-114">Область:</span><span class="sxs-lookup"><span data-stu-id="de70f-114">Area:</span></span>  <br/> |<span data-ttu-id="de70f-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="de70f-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de70f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de70f-116">Remarks</span></span>

<span data-ttu-id="de70f-117">Если свойство **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) имеет значение "SMTP", значение соответствующего свойства **PidLidEmail2OriginalDisplayName** должно равняться значению соответствующего \*\* Свойство dispidEmail2EmailAddress\*\* ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="de70f-117">If the value of the **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) property is "SMTP", the value of the respective **PidLidEmail2OriginalDisplayName** property should equal the value of the respective **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="de70f-118">Это свойство предназначено для отображения альтернативного пользовательского адреса, эквивалентного параметру в **dispidEmail2EmailAddress**.</span><span class="sxs-lookup"><span data-stu-id="de70f-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail2EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="de70f-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="de70f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="de70f-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="de70f-120">Protocol specifications</span></span>

<span data-ttu-id="de70f-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de70f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de70f-122">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="de70f-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="de70f-123">[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de70f-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de70f-124">Задает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="de70f-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="de70f-125">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="de70f-125">Header files</span></span>

<span data-ttu-id="de70f-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="de70f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="de70f-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="de70f-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de70f-128">См. также</span><span class="sxs-lookup"><span data-stu-id="de70f-128">See also</span></span>



[<span data-ttu-id="de70f-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="de70f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de70f-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="de70f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de70f-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="de70f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de70f-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="de70f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

