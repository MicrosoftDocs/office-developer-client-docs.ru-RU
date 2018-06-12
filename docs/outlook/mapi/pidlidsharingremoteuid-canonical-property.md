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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: cb8b4a7c71f3ad81949f3eac6cab230f40c6d487
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810547"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a><span data-ttu-id="c799b-103">Каноническое свойство PidLidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="c799b-103">PidLidSharingRemoteUid Canonical Property</span></span>

  
  
<span data-ttu-id="c799b-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c799b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c799b-105">Указывает идентификатор записи удаленной общей папке.</span><span class="sxs-lookup"><span data-stu-id="c799b-105">Specifies the entry ID of the remote folder being shared.</span></span> <span data-ttu-id="c799b-106">Это свойство общего доступа сообщения.</span><span class="sxs-lookup"><span data-stu-id="c799b-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c799b-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c799b-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="c799b-108">dispidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="c799b-108">dispidSharingRemoteUid</span></span>  <br/> |
|<span data-ttu-id="c799b-109">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="c799b-109">Property set:</span></span>  <br/> |<span data-ttu-id="c799b-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="c799b-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="c799b-111">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="c799b-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c799b-112">0x00008A06</span><span class="sxs-lookup"><span data-stu-id="c799b-112">0x00008A06</span></span>  <br/> |
|<span data-ttu-id="c799b-113">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c799b-113">Data type:</span></span>  <br/> |<span data-ttu-id="c799b-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c799b-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c799b-115">Области:</span><span class="sxs-lookup"><span data-stu-id="c799b-115">Area:</span></span>  <br/> |<span data-ttu-id="c799b-116">Sharing</span><span class="sxs-lookup"><span data-stu-id="c799b-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c799b-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="c799b-117">Remarks</span></span>

<span data-ttu-id="c799b-118">Это свойство должно иметь значение шестнадцатеричную строку, представляющую значение свойства PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) в общей папке.</span><span class="sxs-lookup"><span data-stu-id="c799b-118">This property must be set to the hexadecimal string representation of the value of the PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) property on the folder being shared.</span></span> <span data-ttu-id="c799b-119">Это свойство общего доступа сообщения.</span><span class="sxs-lookup"><span data-stu-id="c799b-119">This is a property of a sharing message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c799b-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c799b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c799b-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c799b-121">Protocol specifications</span></span>

<span data-ttu-id="c799b-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c799b-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c799b-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c799b-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c799b-124">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c799b-124">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c799b-125">Открывает общий доступ папки почтовых ящиков между клиентами.</span><span class="sxs-lookup"><span data-stu-id="c799b-125">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c799b-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c799b-126">Header files</span></span>

<span data-ttu-id="c799b-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c799b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c799b-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c799b-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c799b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="c799b-129">See also</span></span>



[<span data-ttu-id="c799b-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c799b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c799b-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c799b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c799b-132">Каноническое свойство имена сопоставляемых именам MAPI</span><span class="sxs-lookup"><span data-stu-id="c799b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c799b-133">Сопоставление имен MAPI имена каноническое свойств</span><span class="sxs-lookup"><span data-stu-id="c799b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

