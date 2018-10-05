---
title: Каноническое свойство PidLidSharingRemoteType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteType
api_type:
- COM
ms.assetid: e9bc7c7c-86df-45d8-922b-76e3b076144a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3297ca951097c9f3601086809c6e294854c88656
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394610"
---
# <a name="pidlidsharingremotetype-canonical-property"></a><span data-ttu-id="7cb63-103">Каноническое свойство PidLidSharingRemoteType</span><span class="sxs-lookup"><span data-stu-id="7cb63-103">PidLidSharingRemoteType Canonical Property</span></span>

  
  
<span data-ttu-id="7cb63-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7cb63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7cb63-105">Указывает тип удаленной общей папке.</span><span class="sxs-lookup"><span data-stu-id="7cb63-105">Specifies the type of the remote shared folder.</span></span> <span data-ttu-id="7cb63-106">Это свойство общего доступа сообщения.</span><span class="sxs-lookup"><span data-stu-id="7cb63-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7cb63-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7cb63-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="7cb63-108">dispidSharingRemoteType</span><span class="sxs-lookup"><span data-stu-id="7cb63-108">dispidSharingRemoteType</span></span>  <br/> |
|<span data-ttu-id="7cb63-109">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="7cb63-109">Property set:</span></span>  <br/> |<span data-ttu-id="7cb63-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="7cb63-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="7cb63-111">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="7cb63-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7cb63-112">0x00008A1D</span><span class="sxs-lookup"><span data-stu-id="7cb63-112">0x00008A1D</span></span>  <br/> |
|<span data-ttu-id="7cb63-113">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7cb63-113">Data type:</span></span>  <br/> |<span data-ttu-id="7cb63-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7cb63-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7cb63-115">Область:</span><span class="sxs-lookup"><span data-stu-id="7cb63-115">Area:</span></span>  <br/> |<span data-ttu-id="7cb63-116">Sharing</span><span class="sxs-lookup"><span data-stu-id="7cb63-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7cb63-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="7cb63-117">Remarks</span></span>

<span data-ttu-id="7cb63-118">Это свойство должно иметь значение совпадает со значением свойства **dispidSharingLocalType** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) и можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="7cb63-118">This property must be set to the same value as the **dispidSharingLocalType** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7cb63-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7cb63-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7cb63-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7cb63-120">Protocol specifications</span></span>

<span data-ttu-id="7cb63-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7cb63-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7cb63-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7cb63-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7cb63-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7cb63-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7cb63-124">Открывает общий доступ папки почтовых ящиков между клиентами.</span><span class="sxs-lookup"><span data-stu-id="7cb63-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7cb63-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7cb63-125">Header files</span></span>

<span data-ttu-id="7cb63-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7cb63-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7cb63-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7cb63-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7cb63-128">См. также</span><span class="sxs-lookup"><span data-stu-id="7cb63-128">See also</span></span>



[<span data-ttu-id="7cb63-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7cb63-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7cb63-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7cb63-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7cb63-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7cb63-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7cb63-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7cb63-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

