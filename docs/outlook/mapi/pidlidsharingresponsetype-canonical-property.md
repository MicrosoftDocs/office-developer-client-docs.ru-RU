---
title: Каноническое свойство PidLidSharingResponseType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingResponseType
api_type:
- COM
ms.assetid: c27b1239-3612-4bb3-9f22-4b89ee9900cd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: beb2c46b43ae77de08900aeb987d875e85575aba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563186"
---
# <a name="pidlidsharingresponsetype-canonical-property"></a><span data-ttu-id="8332c-103">Каноническое свойство PidLidSharingResponseType</span><span class="sxs-lookup"><span data-stu-id="8332c-103">PidLidSharingResponseType Canonical Property</span></span>

  
  
<span data-ttu-id="8332c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8332c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8332c-105">Указывает тип ответа, с которого ответили получателя запрос общий доступ.</span><span class="sxs-lookup"><span data-stu-id="8332c-105">Specifies the type of response with which the recipient of the sharing request responded.</span></span> <span data-ttu-id="8332c-106">Это свойство общего доступа сообщения.</span><span class="sxs-lookup"><span data-stu-id="8332c-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8332c-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8332c-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="8332c-108">dispidSharingResponseType</span><span class="sxs-lookup"><span data-stu-id="8332c-108">dispidSharingResponseType</span></span>  <br/> |
|<span data-ttu-id="8332c-109">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="8332c-109">Property set:</span></span>  <br/> |<span data-ttu-id="8332c-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="8332c-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="8332c-111">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="8332c-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8332c-112">0x00008A27</span><span class="sxs-lookup"><span data-stu-id="8332c-112">0x00008A27</span></span>  <br/> |
|<span data-ttu-id="8332c-113">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8332c-113">Data type:</span></span>  <br/> |<span data-ttu-id="8332c-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8332c-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8332c-115">Область:</span><span class="sxs-lookup"><span data-stu-id="8332c-115">Area:</span></span>  <br/> |<span data-ttu-id="8332c-116">Sharing</span><span class="sxs-lookup"><span data-stu-id="8332c-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8332c-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="8332c-117">Remarks</span></span>

<span data-ttu-id="8332c-118">Значение этого свойства необходимо задать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="8332c-118">The value of this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="8332c-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8332c-119">**Value**</span></span>|<span data-ttu-id="8332c-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8332c-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8332c-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8332c-121">0x00000000</span></span>  <br/> |<span data-ttu-id="8332c-122">Нет ответа</span><span class="sxs-lookup"><span data-stu-id="8332c-122">No response</span></span>  <br/> |
|<span data-ttu-id="8332c-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8332c-123">0x00000001</span></span>  <br/> |<span data-ttu-id="8332c-124">Принято</span><span class="sxs-lookup"><span data-stu-id="8332c-124">Accepted</span></span>  <br/> |
|<span data-ttu-id="8332c-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8332c-125">0x00000002</span></span>  <br/> |<span data-ttu-id="8332c-126">Запрещен</span><span class="sxs-lookup"><span data-stu-id="8332c-126">Denied</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8332c-127">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8332c-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8332c-128">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8332c-128">Protocol specifications</span></span>

<span data-ttu-id="8332c-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8332c-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8332c-130">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8332c-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8332c-131">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8332c-131">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8332c-132">Открывает общий доступ папки почтовых ящиков между клиентами.</span><span class="sxs-lookup"><span data-stu-id="8332c-132">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8332c-133">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8332c-133">Header files</span></span>

<span data-ttu-id="8332c-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8332c-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="8332c-135">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8332c-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8332c-136">См. также</span><span class="sxs-lookup"><span data-stu-id="8332c-136">See also</span></span>



[<span data-ttu-id="8332c-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8332c-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8332c-138">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8332c-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8332c-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8332c-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8332c-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8332c-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

