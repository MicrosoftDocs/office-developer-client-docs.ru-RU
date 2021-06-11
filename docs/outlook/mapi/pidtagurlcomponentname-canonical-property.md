---
title: Каноническое свойство PidTagUrlComponentName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUrlComponentName
api_type:
- COM
ms.assetid: a21906f9-5408-41ba-a89b-273ab60eeef3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 26a9d432d98c546aefa8f511ba2c4c9bb26cfd80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320428"
---
# <a name="pidtagurlcomponentname-canonical-property"></a><span data-ttu-id="18c93-103">Каноническое свойство PidTagUrlComponentName</span><span class="sxs-lookup"><span data-stu-id="18c93-103">PidTagUrlComponentName Canonical Property</span></span>

  
  
<span data-ttu-id="18c93-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18c93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18c93-105">Имя компонента URL-адреса для сообщения.</span><span class="sxs-lookup"><span data-stu-id="18c93-105">The URL component name for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18c93-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="18c93-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18c93-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span><span class="sxs-lookup"><span data-stu-id="18c93-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span></span>  <br/> |
|<span data-ttu-id="18c93-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="18c93-108">Identifier:</span></span>  <br/> |<span data-ttu-id="18c93-109">0x10F3</span><span class="sxs-lookup"><span data-stu-id="18c93-109">0x10F3</span></span>  <br/> |
|<span data-ttu-id="18c93-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="18c93-110">Data type:</span></span>  <br/> |<span data-ttu-id="18c93-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="18c93-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="18c93-112">Область:</span><span class="sxs-lookup"><span data-stu-id="18c93-112">Area:</span></span>  <br/> |<span data-ttu-id="18c93-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="18c93-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18c93-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="18c93-114">Remarks</span></span>

<span data-ttu-id="18c93-115">Эти свойства должны быть уникальными в папке.</span><span class="sxs-lookup"><span data-stu-id="18c93-115">These properties should be unique within a folder.</span></span> <span data-ttu-id="18c93-116">Если не установлено, когда сообщение создано, хранилище сообщений должно устанавливать эти свойства на основе различных свойств сообщений в зависимости от класса сообщения.</span><span class="sxs-lookup"><span data-stu-id="18c93-116">If not set when the message is created, the message store should set these properties based on various message properties, depending on the message class.</span></span> <span data-ttu-id="18c93-117">Например, **IPM. Примечание** и **IPM. Сообщения** о встрече должны иметь этот набор свойств на основе **свойства PR_SUBJECT** [(PidTagSubject)](pidtagsubject-canonical-property.md)и **IPM. В** контактных сообщениях должен быть этот набор свойств, основанный на свойстве **dispidFileUnder** [(PidLidFileUnder).](pidlidfileunder-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="18c93-117">For example, the **IPM.Note** and **IPM.Appointment** messages should have this property set based on the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property and the **IPM.Contact** messages should have this property set based on the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property.</span></span> <span data-ttu-id="18c93-118">Для большинства других классов сообщений это свойство должно основываться на **свойстве PR_DISPLAY_NAME** [(PidTagDisplayName).](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="18c93-118">For most other message classes, this property should be based on the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="18c93-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="18c93-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18c93-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="18c93-120">Protocol specifications</span></span>

<span data-ttu-id="18c93-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18c93-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18c93-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="18c93-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="18c93-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18c93-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18c93-124">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="18c93-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="18c93-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18c93-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18c93-126">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="18c93-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18c93-127">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="18c93-127">Header files</span></span>

<span data-ttu-id="18c93-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18c93-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="18c93-129">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="18c93-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="18c93-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="18c93-130">Mapitags.h</span></span>
  
> <span data-ttu-id="18c93-131">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="18c93-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18c93-132">См. также</span><span class="sxs-lookup"><span data-stu-id="18c93-132">See also</span></span>



[<span data-ttu-id="18c93-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="18c93-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18c93-134">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="18c93-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18c93-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="18c93-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18c93-136">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="18c93-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

