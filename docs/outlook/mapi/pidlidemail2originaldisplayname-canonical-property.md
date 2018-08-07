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
ms.openlocfilehash: 2b3f59633fcea0b895cd024dbbbc106c8d492bf0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810258"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a><span data-ttu-id="5dabb-103">Каноническое свойство PidLidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="5dabb-103">PidLidEmail2OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="5dabb-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5dabb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5dabb-105">Задает второй отображаемое имя, соответствующий адрес электронной почты, указанный для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="5dabb-105">Specifies the second display name that corresponds to the email address specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5dabb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5dabb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5dabb-107">dispidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="5dabb-107">dispidEmail2OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="5dabb-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="5dabb-108">Property set:</span></span>  <br/> |<span data-ttu-id="5dabb-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="5dabb-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="5dabb-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="5dabb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5dabb-111">0x00008094</span><span class="sxs-lookup"><span data-stu-id="5dabb-111">0x00008094</span></span>  <br/> |
|<span data-ttu-id="5dabb-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5dabb-112">Data type:</span></span>  <br/> |<span data-ttu-id="5dabb-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5dabb-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5dabb-114">Область:</span><span class="sxs-lookup"><span data-stu-id="5dabb-114">Area:</span></span>  <br/> |<span data-ttu-id="5dabb-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="5dabb-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5dabb-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="5dabb-116">Remarks</span></span>

<span data-ttu-id="5dabb-117">Если значение свойства **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) «SMTP», значение соответствующего свойства **PidLidEmail2OriginalDisplayName** должно быть равно значение соответствующих ** dispidEmail2EmailAddress** свойство ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5dabb-117">If the value of the **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) property is "SMTP", the value of the respective **PidLidEmail2OriginalDisplayName** property should equal the value of the respective **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="5dabb-118">Это свойство предназначено для отображения альтернативный понятное адрес, который соответствует тому в **dispidEmail2EmailAddress**.</span><span class="sxs-lookup"><span data-stu-id="5dabb-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail2EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5dabb-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5dabb-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5dabb-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5dabb-120">Protocol specifications</span></span>

<span data-ttu-id="5dabb-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5dabb-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5dabb-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5dabb-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5dabb-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5dabb-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5dabb-124">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="5dabb-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5dabb-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5dabb-125">Header files</span></span>

<span data-ttu-id="5dabb-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5dabb-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5dabb-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5dabb-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5dabb-128">См. также</span><span class="sxs-lookup"><span data-stu-id="5dabb-128">See also</span></span>



[<span data-ttu-id="5dabb-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5dabb-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5dabb-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5dabb-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5dabb-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5dabb-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5dabb-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5dabb-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

