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
ms.openlocfilehash: eb699b2312064f8ed330238962dd86992c046139
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337123"
---
# <a name="pidlidsharinginitiatorsmtp-canonical-property"></a><span data-ttu-id="d4de6-103">Каноническое свойство PidLidSharingInitiatorSmtp</span><span class="sxs-lookup"><span data-stu-id="d4de6-103">PidLidSharingInitiatorSmtp Canonical Property</span></span>

  
  
<span data-ttu-id="d4de6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4de6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4de6-105">Указывает SMTP-адрес пользователя, инициировавшего сообщение о предоставлении общего доступа.</span><span class="sxs-lookup"><span data-stu-id="d4de6-105">Specifies the SMTP address of the user who initiated the sharing message.</span></span> <span data-ttu-id="d4de6-106">Это свойство сообщения о совместном доступе.</span><span class="sxs-lookup"><span data-stu-id="d4de6-106">This is a property of a sharing message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4de6-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d4de6-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="d4de6-108">Диспидшарингинитиаторсмтп</span><span class="sxs-lookup"><span data-stu-id="d4de6-108">dispidSharingInitiatorSmtp</span></span>  <br/> |
|<span data-ttu-id="d4de6-109">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="d4de6-109">Property set:</span></span>  <br/> |<span data-ttu-id="d4de6-110">Псетид_шаринг</span><span class="sxs-lookup"><span data-stu-id="d4de6-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="d4de6-111">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="d4de6-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d4de6-112">0x00008A08</span><span class="sxs-lookup"><span data-stu-id="d4de6-112">0x00008A08</span></span>  <br/> |
|<span data-ttu-id="d4de6-113">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d4de6-113">Data type:</span></span>  <br/> |<span data-ttu-id="d4de6-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d4de6-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d4de6-115">Область:</span><span class="sxs-lookup"><span data-stu-id="d4de6-115">Area:</span></span>  <br/> |<span data-ttu-id="d4de6-116">Общий доступ</span><span class="sxs-lookup"><span data-stu-id="d4de6-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4de6-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4de6-117">Remarks</span></span>

<span data-ttu-id="d4de6-118">Для этого свойства должно быть задано значение свойства **пр_смтп_аддресс** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) из адресной книги, определенной свойством **диспидшарингинитиатореид** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)), и должно быть обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="d4de6-118">This property must be set to the value of the **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) property from the Address Book identified by the **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d4de6-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d4de6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d4de6-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d4de6-120">Protocol specifications</span></span>

<span data-ttu-id="d4de6-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4de6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4de6-122">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d4de6-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d4de6-123">[[MS — ОКСШАРЕ]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4de6-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4de6-124">Предоставляет общий доступ к папкам почтового ящика между клиентами.</span><span class="sxs-lookup"><span data-stu-id="d4de6-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d4de6-125">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="d4de6-125">Header files</span></span>

<span data-ttu-id="d4de6-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="d4de6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d4de6-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d4de6-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d4de6-128">См. также</span><span class="sxs-lookup"><span data-stu-id="d4de6-128">See also</span></span>



[<span data-ttu-id="d4de6-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d4de6-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d4de6-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="d4de6-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d4de6-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d4de6-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d4de6-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d4de6-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

