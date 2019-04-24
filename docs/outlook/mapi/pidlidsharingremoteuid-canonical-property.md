---
title: Каноническое свойство PidLidSharingRemoteUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteUid
api_type:
- COM
ms.assetid: cfe3b728-317b-4871-adea-e2fdf8441da7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c3e783934367ad7c5c1a9a760aa8a24525901832
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331264"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a><span data-ttu-id="0ede7-103">Каноническое свойство PidLidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="0ede7-103">PidLidSharingRemoteUid Canonical Property</span></span>

  
  
<span data-ttu-id="0ede7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ede7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ede7-105">Указывает идентификатор удаленной папки, к которой предоставлен общий доступ.</span><span class="sxs-lookup"><span data-stu-id="0ede7-105">Specifies the entry ID of the remote folder being shared.</span></span> <span data-ttu-id="0ede7-106">Это свойство сообщения о совместном доступе.</span><span class="sxs-lookup"><span data-stu-id="0ede7-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0ede7-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0ede7-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="0ede7-108">Диспидшарингремотеуид</span><span class="sxs-lookup"><span data-stu-id="0ede7-108">dispidSharingRemoteUid</span></span>  <br/> |
|<span data-ttu-id="0ede7-109">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="0ede7-109">Property set:</span></span>  <br/> |<span data-ttu-id="0ede7-110">Псетид_шаринг</span><span class="sxs-lookup"><span data-stu-id="0ede7-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="0ede7-111">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="0ede7-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0ede7-112">0x00008A06</span><span class="sxs-lookup"><span data-stu-id="0ede7-112">0x00008A06</span></span>  <br/> |
|<span data-ttu-id="0ede7-113">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0ede7-113">Data type:</span></span>  <br/> |<span data-ttu-id="0ede7-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0ede7-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0ede7-115">Область:</span><span class="sxs-lookup"><span data-stu-id="0ede7-115">Area:</span></span>  <br/> |<span data-ttu-id="0ede7-116">Общий доступ</span><span class="sxs-lookup"><span data-stu-id="0ede7-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ede7-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ede7-117">Remarks</span></span>

<span data-ttu-id="0ede7-118">Для этого свойства должно быть задано шестнадцатеричное строковое представление значения свойства ПР_ЕНТРИД ([PidTagEntryId](pidtagentryid-canonical-property.md)) для общей папки.</span><span class="sxs-lookup"><span data-stu-id="0ede7-118">This property must be set to the hexadecimal string representation of the value of the PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) property on the folder being shared.</span></span> <span data-ttu-id="0ede7-119">Это свойство сообщения о совместном доступе.</span><span class="sxs-lookup"><span data-stu-id="0ede7-119">This is a property of a sharing message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0ede7-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0ede7-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0ede7-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0ede7-121">Protocol specifications</span></span>

<span data-ttu-id="0ede7-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ede7-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ede7-123">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0ede7-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0ede7-124">[[MS — ОКСШАРЕ]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ede7-124">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ede7-125">Предоставляет общий доступ к папкам почтового ящика между клиентами.</span><span class="sxs-lookup"><span data-stu-id="0ede7-125">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0ede7-126">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="0ede7-126">Header files</span></span>

<span data-ttu-id="0ede7-127">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="0ede7-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0ede7-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0ede7-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ede7-129">См. также</span><span class="sxs-lookup"><span data-stu-id="0ede7-129">See also</span></span>



[<span data-ttu-id="0ede7-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0ede7-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0ede7-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="0ede7-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0ede7-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0ede7-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0ede7-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0ede7-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

