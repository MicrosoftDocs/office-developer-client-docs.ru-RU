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
# <a name="pidlidsharingremoteuid-canonical-property"></a><span data-ttu-id="93b76-103">Каноническое свойство PidLidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="93b76-103">PidLidSharingRemoteUid Canonical Property</span></span>

  
  
<span data-ttu-id="93b76-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93b76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93b76-105">Указывает ИД записи удаленной папки, к которая совместному доступу.</span><span class="sxs-lookup"><span data-stu-id="93b76-105">Specifies the entry ID of the remote folder being shared.</span></span> <span data-ttu-id="93b76-106">Это свойство общего сообщения.</span><span class="sxs-lookup"><span data-stu-id="93b76-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93b76-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="93b76-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="93b76-108">dispidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="93b76-108">dispidSharingRemoteUid</span></span>  <br/> |
|<span data-ttu-id="93b76-109">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="93b76-109">Property set:</span></span>  <br/> |<span data-ttu-id="93b76-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="93b76-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="93b76-111">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="93b76-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="93b76-112">0x00008A06</span><span class="sxs-lookup"><span data-stu-id="93b76-112">0x00008A06</span></span>  <br/> |
|<span data-ttu-id="93b76-113">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="93b76-113">Data type:</span></span>  <br/> |<span data-ttu-id="93b76-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="93b76-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="93b76-115">Область:</span><span class="sxs-lookup"><span data-stu-id="93b76-115">Area:</span></span>  <br/> |<span data-ttu-id="93b76-116">Общий доступ</span><span class="sxs-lookup"><span data-stu-id="93b76-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93b76-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="93b76-117">Remarks</span></span>

<span data-ttu-id="93b76-118">Этому свойству должно быть задано представление строки значения свойства PR_ENTRYID ([PidTagEntryId)](pidtagentryid-canonical-property.md)в общей папке.</span><span class="sxs-lookup"><span data-stu-id="93b76-118">This property must be set to the hexadecimal string representation of the value of the PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) property on the folder being shared.</span></span> <span data-ttu-id="93b76-119">Это свойство сообщения общего доступа.</span><span class="sxs-lookup"><span data-stu-id="93b76-119">This is a property of a sharing message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="93b76-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="93b76-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="93b76-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="93b76-121">Protocol specifications</span></span>

<span data-ttu-id="93b76-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93b76-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93b76-123">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="93b76-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="93b76-124">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93b76-124">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93b76-125">Папки почтовых ящиков разделяются между клиентами.</span><span class="sxs-lookup"><span data-stu-id="93b76-125">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="93b76-126">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="93b76-126">Header files</span></span>

<span data-ttu-id="93b76-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="93b76-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="93b76-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="93b76-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93b76-129">См. также</span><span class="sxs-lookup"><span data-stu-id="93b76-129">See also</span></span>



[<span data-ttu-id="93b76-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="93b76-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93b76-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="93b76-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93b76-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="93b76-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93b76-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="93b76-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

