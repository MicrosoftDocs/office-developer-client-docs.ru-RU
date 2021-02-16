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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335044"
---
# <a name="pidlidemail1originaldisplayname-canonical-property"></a><span data-ttu-id="7e9b2-103">Каноническое свойство PidLidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="7e9b2-103">PidLidEmail1OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="7e9b2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e9b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e9b2-105">Указывает первое отображаемого имени, соответствующее адресу электронной почты, указанному для контакта.</span><span class="sxs-lookup"><span data-stu-id="7e9b2-105">Specifies the first display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7e9b2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7e9b2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7e9b2-107">dispidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="7e9b2-107">dispidEmail1OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="7e9b2-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="7e9b2-108">Property set:</span></span>  <br/> |<span data-ttu-id="7e9b2-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="7e9b2-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="7e9b2-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="7e9b2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7e9b2-111">0x00008084</span><span class="sxs-lookup"><span data-stu-id="7e9b2-111">0x00008084</span></span>  <br/> |
|<span data-ttu-id="7e9b2-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7e9b2-112">Data type:</span></span>  <br/> |<span data-ttu-id="7e9b2-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7e9b2-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7e9b2-114">Область:</span><span class="sxs-lookup"><span data-stu-id="7e9b2-114">Area:</span></span>  <br/> |<span data-ttu-id="7e9b2-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="7e9b2-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e9b2-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="7e9b2-116">Remarks</span></span>

<span data-ttu-id="7e9b2-117">Если свойство **dispidEmail1AddrType** ([PidLidEmail1AddressType)](pidlidemail1addresstype-canonical-property.md)имеет значение "SMTP", значение соответствующего свойства **dispidEmail1OriginalDisplayName** должно быть равно значению соответствующего свойства **dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress).](pidlidemail1emailaddress-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="7e9b2-117">If the value of the **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail1OriginalDisplayName** property should equal the value of the respective **dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="7e9b2-118">Это свойство отображает альтернативный пользовательский адрес, эквивалентный адресу в свойстве **dispidEmail1EmailAddress.**</span><span class="sxs-lookup"><span data-stu-id="7e9b2-118">This property displays an alternative user-friendly address that is equivalent to the one in the **dispidEmail1EmailAddress** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7e9b2-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7e9b2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7e9b2-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7e9b2-120">Protocol specifications</span></span>

<span data-ttu-id="7e9b2-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e9b2-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e9b2-122">Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="7e9b2-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7e9b2-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e9b2-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e9b2-124">Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="7e9b2-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7e9b2-125">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="7e9b2-125">Header files</span></span>

<span data-ttu-id="7e9b2-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7e9b2-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7e9b2-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7e9b2-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7e9b2-128">См. также</span><span class="sxs-lookup"><span data-stu-id="7e9b2-128">See also</span></span>



[<span data-ttu-id="7e9b2-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7e9b2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7e9b2-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7e9b2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7e9b2-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7e9b2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7e9b2-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7e9b2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

