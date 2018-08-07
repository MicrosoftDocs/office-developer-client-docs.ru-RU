---
title: Каноническое свойство PidLidSharingInitiatorSmtp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorSmtp
api_type:
- COM
ms.assetid: 4fb7d91d-4c51-41c1-9cb6-7b837dd12f11
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 188424fc67534ea5df6ed5eb209909731e12c73c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810540"
---
# <a name="pidlidsharinginitiatorsmtp-canonical-property"></a><span data-ttu-id="2bb01-103">Каноническое свойство PidLidSharingInitiatorSmtp</span><span class="sxs-lookup"><span data-stu-id="2bb01-103">PidLidSharingInitiatorSmtp Canonical Property</span></span>

  
  
<span data-ttu-id="2bb01-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2bb01-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2bb01-105">Указывает SMTP-адрес пользователя, инициировавшего сообщение о совместном доступе.</span><span class="sxs-lookup"><span data-stu-id="2bb01-105">Specifies the SMTP address of the user who initiated the sharing message.</span></span> <span data-ttu-id="2bb01-106">Это свойство общего доступа сообщения.</span><span class="sxs-lookup"><span data-stu-id="2bb01-106">This is a property of a sharing message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2bb01-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2bb01-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="2bb01-108">dispidSharingInitiatorSmtp</span><span class="sxs-lookup"><span data-stu-id="2bb01-108">dispidSharingInitiatorSmtp</span></span>  <br/> |
|<span data-ttu-id="2bb01-109">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="2bb01-109">Property set:</span></span>  <br/> |<span data-ttu-id="2bb01-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="2bb01-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="2bb01-111">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="2bb01-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2bb01-112">0x00008A08</span><span class="sxs-lookup"><span data-stu-id="2bb01-112">0x00008A08</span></span>  <br/> |
|<span data-ttu-id="2bb01-113">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2bb01-113">Data type:</span></span>  <br/> |<span data-ttu-id="2bb01-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2bb01-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2bb01-115">Область:</span><span class="sxs-lookup"><span data-stu-id="2bb01-115">Area:</span></span>  <br/> |<span data-ttu-id="2bb01-116">Sharing</span><span class="sxs-lookup"><span data-stu-id="2bb01-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2bb01-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="2bb01-117">Remarks</span></span>

<span data-ttu-id="2bb01-118">Это свойство должно быть задано значение свойства **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) из адресной книги, заданной свойством **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) и должен быть игнорируются.</span><span class="sxs-lookup"><span data-stu-id="2bb01-118">This property must be set to the value of the **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) property from the Address Book identified by the **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2bb01-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2bb01-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2bb01-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2bb01-120">Protocol specifications</span></span>

<span data-ttu-id="2bb01-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2bb01-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2bb01-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2bb01-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2bb01-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2bb01-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2bb01-124">Открывает общий доступ папки почтовых ящиков между клиентами.</span><span class="sxs-lookup"><span data-stu-id="2bb01-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2bb01-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2bb01-125">Header files</span></span>

<span data-ttu-id="2bb01-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2bb01-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2bb01-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2bb01-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2bb01-128">См. также</span><span class="sxs-lookup"><span data-stu-id="2bb01-128">See also</span></span>



[<span data-ttu-id="2bb01-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2bb01-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2bb01-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2bb01-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2bb01-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2bb01-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2bb01-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2bb01-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

