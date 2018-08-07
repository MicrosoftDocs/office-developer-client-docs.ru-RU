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
ms.openlocfilehash: 3a2b0939bbfa5143e4bd99e74b0f84e3ca7efb12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812036"
---
# <a name="pidtagurlcomponentname-canonical-property"></a><span data-ttu-id="87e21-103">Каноническое свойство PidTagUrlComponentName</span><span class="sxs-lookup"><span data-stu-id="87e21-103">PidTagUrlComponentName Canonical Property</span></span>

  
  
<span data-ttu-id="87e21-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="87e21-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="87e21-105">Имя компонента URL-адрес для сообщения.</span><span class="sxs-lookup"><span data-stu-id="87e21-105">The URL component name for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87e21-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="87e21-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87e21-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span><span class="sxs-lookup"><span data-stu-id="87e21-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span></span>  <br/> |
|<span data-ttu-id="87e21-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="87e21-108">Identifier:</span></span>  <br/> |<span data-ttu-id="87e21-109">0x10F3</span><span class="sxs-lookup"><span data-stu-id="87e21-109">0x10F3</span></span>  <br/> |
|<span data-ttu-id="87e21-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="87e21-110">Data type:</span></span>  <br/> |<span data-ttu-id="87e21-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="87e21-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="87e21-112">Область:</span><span class="sxs-lookup"><span data-stu-id="87e21-112">Area:</span></span>  <br/> |<span data-ttu-id="87e21-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="87e21-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87e21-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="87e21-114">Remarks</span></span>

<span data-ttu-id="87e21-115">Эти свойства должны быть уникальными в рамках папку.</span><span class="sxs-lookup"><span data-stu-id="87e21-115">These properties should be unique within a folder.</span></span> <span data-ttu-id="87e21-116">Если не задан при создании сообщения, хранилища сообщений следует задать эти свойства, на основе различных свойств сообщения, в зависимости от класса сообщения.</span><span class="sxs-lookup"><span data-stu-id="87e21-116">If not set when the message is created, the message store should set these properties based on various message properties, depending on the message class.</span></span> <span data-ttu-id="87e21-117">Например **IPM. Примечание** и **IPM. Встреча** сообщения должны иметь данное свойство установлено на основе свойства **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) и **IPM. Контакт** сообщений должен иметь это свойство заданы на основании свойство **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="87e21-117">For example, the **IPM.Note** and **IPM.Appointment** messages should have this property set based on the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property and the **IPM.Contact** messages should have this property set based on the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property.</span></span> <span data-ttu-id="87e21-118">Для большинства классов сообщений этого свойства необходимо основываться на свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="87e21-118">For most other message classes, this property should be based on the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="87e21-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="87e21-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="87e21-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="87e21-120">Protocol specifications</span></span>

<span data-ttu-id="87e21-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87e21-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87e21-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="87e21-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="87e21-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87e21-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87e21-124">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="87e21-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="87e21-125">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87e21-125">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87e21-126">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="87e21-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="87e21-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="87e21-127">Header files</span></span>

<span data-ttu-id="87e21-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="87e21-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="87e21-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="87e21-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="87e21-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="87e21-130">Mapitags.h</span></span>
  
> <span data-ttu-id="87e21-131">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="87e21-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87e21-132">См. также</span><span class="sxs-lookup"><span data-stu-id="87e21-132">See also</span></span>



[<span data-ttu-id="87e21-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="87e21-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87e21-134">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="87e21-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87e21-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="87e21-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87e21-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="87e21-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

