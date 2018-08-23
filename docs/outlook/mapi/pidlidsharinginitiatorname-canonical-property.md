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
ms.openlocfilehash: 66ec6ecb33336c51ce76dd080a80af4c26e098f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563039"
---
# <a name="pidlidsharinginitiatorname-canonical-property"></a><span data-ttu-id="2a06f-103">Каноническое свойство PidLidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="2a06f-103">PidLidSharingInitiatorName Canonical Property</span></span>

  
  
<span data-ttu-id="2a06f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a06f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a06f-105">Определяет, как свойство общего доступа сообщения.</span><span class="sxs-lookup"><span data-stu-id="2a06f-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2a06f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2a06f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2a06f-107">dispidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="2a06f-107">dispidSharingInitiatorName</span></span>  <br/> |
|<span data-ttu-id="2a06f-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="2a06f-108">Property set:</span></span>  <br/> |<span data-ttu-id="2a06f-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="2a06f-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="2a06f-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="2a06f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2a06f-111">0x00008A07</span><span class="sxs-lookup"><span data-stu-id="2a06f-111">0x00008A07</span></span>  <br/> |
|<span data-ttu-id="2a06f-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2a06f-112">Data type:</span></span>  <br/> |<span data-ttu-id="2a06f-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2a06f-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2a06f-114">Область:</span><span class="sxs-lookup"><span data-stu-id="2a06f-114">Area:</span></span>  <br/> |<span data-ttu-id="2a06f-115">Sharing</span><span class="sxs-lookup"><span data-stu-id="2a06f-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a06f-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="2a06f-116">Remarks</span></span>

<span data-ttu-id="2a06f-117">Это свойство должно быть присвоено значение **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) из адресной книги, определяемую средством **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) и можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="2a06f-117">This property must be set to the value of **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from the Address Book identified by **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) and should be ignored.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2a06f-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2a06f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2a06f-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2a06f-119">Protocol specifications</span></span>

<span data-ttu-id="2a06f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a06f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a06f-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2a06f-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2a06f-122">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a06f-122">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a06f-123">Открывает общий доступ папки почтовых ящиков между клиентами.</span><span class="sxs-lookup"><span data-stu-id="2a06f-123">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2a06f-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2a06f-124">Header files</span></span>

<span data-ttu-id="2a06f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2a06f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2a06f-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2a06f-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2a06f-127">См. также</span><span class="sxs-lookup"><span data-stu-id="2a06f-127">See also</span></span>



[<span data-ttu-id="2a06f-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2a06f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2a06f-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2a06f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2a06f-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2a06f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2a06f-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2a06f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

