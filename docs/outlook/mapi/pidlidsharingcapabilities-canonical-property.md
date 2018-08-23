---
title: Каноническое свойство PidLidSharingCapabilities
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingCapabilities
api_type:
- COM
ms.assetid: 86b3eab2-2594-4204-aedf-8ce2ee3b81ce
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b6bf95a68c868bfca247ea21d56dd872092c3e02
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578369"
---
# <a name="pidlidsharingcapabilities-canonical-property"></a><span data-ttu-id="00493-103">Каноническое свойство PidLidSharingCapabilities</span><span class="sxs-lookup"><span data-stu-id="00493-103">PidLidSharingCapabilities Canonical Property</span></span>

  
  
<span data-ttu-id="00493-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00493-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00493-105">Определяет, как свойство общего доступа сообщения.</span><span class="sxs-lookup"><span data-stu-id="00493-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00493-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="00493-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00493-107">dispidSharingCaps</span><span class="sxs-lookup"><span data-stu-id="00493-107">dispidSharingCaps</span></span>  <br/> |
|<span data-ttu-id="00493-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="00493-108">Property set:</span></span>  <br/> |<span data-ttu-id="00493-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="00493-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="00493-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="00493-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="00493-111">0x00008A17</span><span class="sxs-lookup"><span data-stu-id="00493-111">0x00008A17</span></span>  <br/> |
|<span data-ttu-id="00493-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="00493-112">Data type:</span></span>  <br/> |<span data-ttu-id="00493-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="00493-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="00493-114">Область:</span><span class="sxs-lookup"><span data-stu-id="00493-114">Area:</span></span>  <br/> |<span data-ttu-id="00493-115">Sharing</span><span class="sxs-lookup"><span data-stu-id="00493-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00493-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="00493-116">Remarks</span></span>

<span data-ttu-id="00493-117">Это свойство должно быть задано одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="00493-117">This property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="00493-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="00493-118">**Value**</span></span>|<span data-ttu-id="00493-119">**Сценарий**</span><span class="sxs-lookup"><span data-stu-id="00493-119">**Scenario**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00493-120">0x00040290</span><span class="sxs-lookup"><span data-stu-id="00493-120">0x00040290</span></span>  <br/> |<span data-ttu-id="00493-121">Этот объект общего доступа к Message связана с особой папкой.</span><span class="sxs-lookup"><span data-stu-id="00493-121">This Sharing Message object relates to a special folder.</span></span>  <br/> |
|<span data-ttu-id="00493-122">0x000402B0</span><span class="sxs-lookup"><span data-stu-id="00493-122">0x000402B0</span></span>  <br/> |<span data-ttu-id="00493-123">Этот объект общего доступа к сообщения не связан специальную папку.</span><span class="sxs-lookup"><span data-stu-id="00493-123">This Sharing Message object does not relate to a special folder.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="00493-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="00493-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00493-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="00493-125">Protocol specifications</span></span>

<span data-ttu-id="00493-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00493-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00493-127">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="00493-127">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="00493-128">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00493-128">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00493-129">Открывает общий доступ папки почтовых ящиков между клиентами.</span><span class="sxs-lookup"><span data-stu-id="00493-129">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="00493-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="00493-130">Header files</span></span>

<span data-ttu-id="00493-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00493-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="00493-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="00493-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00493-133">См. также</span><span class="sxs-lookup"><span data-stu-id="00493-133">See also</span></span>



[<span data-ttu-id="00493-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="00493-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00493-135">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="00493-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00493-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="00493-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00493-137">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="00493-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

