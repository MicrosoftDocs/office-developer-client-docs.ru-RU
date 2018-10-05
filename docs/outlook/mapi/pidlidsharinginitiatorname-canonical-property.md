---
title: Каноническое свойство PidLidSharingInitiatorName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorName
api_type:
- COM
ms.assetid: f2b126fc-41fa-4dc4-9f13-07bc4f621d0b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b9e3236affa9612356e68044d2943ea7b9276384
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394384"
---
# <a name="pidlidsharinginitiatorname-canonical-property"></a><span data-ttu-id="53b9b-103">Каноническое свойство PidLidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="53b9b-103">PidLidSharingInitiatorName Canonical Property</span></span>

  
  
<span data-ttu-id="53b9b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53b9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53b9b-105">Определяет, как свойство общего доступа сообщения.</span><span class="sxs-lookup"><span data-stu-id="53b9b-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="53b9b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="53b9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53b9b-107">dispidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="53b9b-107">dispidSharingInitiatorName</span></span>  <br/> |
|<span data-ttu-id="53b9b-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="53b9b-108">Property set:</span></span>  <br/> |<span data-ttu-id="53b9b-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="53b9b-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="53b9b-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="53b9b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="53b9b-111">0x00008A07</span><span class="sxs-lookup"><span data-stu-id="53b9b-111">0x00008A07</span></span>  <br/> |
|<span data-ttu-id="53b9b-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="53b9b-112">Data type:</span></span>  <br/> |<span data-ttu-id="53b9b-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="53b9b-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="53b9b-114">Область:</span><span class="sxs-lookup"><span data-stu-id="53b9b-114">Area:</span></span>  <br/> |<span data-ttu-id="53b9b-115">Sharing</span><span class="sxs-lookup"><span data-stu-id="53b9b-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53b9b-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="53b9b-116">Remarks</span></span>

<span data-ttu-id="53b9b-117">Это свойство должно быть присвоено значение **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) из адресной книги, определяемую средством **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) и можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="53b9b-117">This property must be set to the value of **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from the Address Book identified by **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) and should be ignored.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="53b9b-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="53b9b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="53b9b-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="53b9b-119">Protocol specifications</span></span>

<span data-ttu-id="53b9b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53b9b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53b9b-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="53b9b-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="53b9b-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53b9b-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53b9b-123">Открывает общий доступ папки почтовых ящиков между клиентами.</span><span class="sxs-lookup"><span data-stu-id="53b9b-123">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="53b9b-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="53b9b-124">Header files</span></span>

<span data-ttu-id="53b9b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53b9b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="53b9b-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="53b9b-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53b9b-127">См. также</span><span class="sxs-lookup"><span data-stu-id="53b9b-127">See also</span></span>



[<span data-ttu-id="53b9b-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="53b9b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="53b9b-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="53b9b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="53b9b-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="53b9b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="53b9b-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="53b9b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

