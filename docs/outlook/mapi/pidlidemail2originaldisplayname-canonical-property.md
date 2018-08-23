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
ms.openlocfilehash: 3461b265e9cae3609cc595401907c506e24aaf91
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584179"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a><span data-ttu-id="63e70-103">Каноническое свойство PidLidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="63e70-103">PidLidEmail2OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="63e70-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63e70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63e70-105">Задает второй отображаемое имя, соответствующий адрес электронной почты, указанный для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="63e70-105">Specifies the second display name that corresponds to the email address specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="63e70-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="63e70-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="63e70-107">dispidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="63e70-107">dispidEmail2OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="63e70-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="63e70-108">Property set:</span></span>  <br/> |<span data-ttu-id="63e70-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="63e70-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="63e70-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="63e70-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="63e70-111">0x00008094</span><span class="sxs-lookup"><span data-stu-id="63e70-111">0x00008094</span></span>  <br/> |
|<span data-ttu-id="63e70-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="63e70-112">Data type:</span></span>  <br/> |<span data-ttu-id="63e70-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="63e70-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="63e70-114">Область:</span><span class="sxs-lookup"><span data-stu-id="63e70-114">Area:</span></span>  <br/> |<span data-ttu-id="63e70-115">Contact</span><span class="sxs-lookup"><span data-stu-id="63e70-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63e70-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="63e70-116">Remarks</span></span>

<span data-ttu-id="63e70-117">Если значение свойства **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) «SMTP», значение соответствующего свойства **PidLidEmail2OriginalDisplayName** должно быть равно значение соответствующих ** dispidEmail2EmailAddress** свойство ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="63e70-117">If the value of the **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) property is "SMTP", the value of the respective **PidLidEmail2OriginalDisplayName** property should equal the value of the respective **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="63e70-118">Это свойство предназначено для отображения альтернативный понятное адрес, который соответствует тому в **dispidEmail2EmailAddress**.</span><span class="sxs-lookup"><span data-stu-id="63e70-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail2EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="63e70-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="63e70-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="63e70-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="63e70-120">Protocol specifications</span></span>

<span data-ttu-id="63e70-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63e70-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63e70-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="63e70-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="63e70-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63e70-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63e70-124">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="63e70-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="63e70-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="63e70-125">Header files</span></span>

<span data-ttu-id="63e70-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="63e70-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="63e70-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="63e70-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63e70-128">См. также</span><span class="sxs-lookup"><span data-stu-id="63e70-128">See also</span></span>



[<span data-ttu-id="63e70-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="63e70-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63e70-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="63e70-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63e70-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="63e70-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63e70-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="63e70-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

