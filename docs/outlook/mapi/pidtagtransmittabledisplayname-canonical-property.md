---
title: Каноническое свойство PidTagTransmittableDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTransmittableDisplayName
api_type:
- COM
ms.assetid: aadd9086-b936-4067-bf7d-f54fc50e3c83
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e66fe8d3621c122ccc19bdde169f20f7d47a148d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331859"
---
# <a name="pidtagtransmittabledisplayname-canonical-property"></a><span data-ttu-id="93f10-103">Каноническое свойство PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="93f10-103">PidTagTransmittableDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="93f10-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93f10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93f10-105">Содержит отображаемую имя получателя в безопасной форме, которую нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="93f10-105">Contains a recipient's display name in a secure form that cannot be changed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93f10-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="93f10-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="93f10-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="93f10-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="93f10-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="93f10-108">Identifier:</span></span>  <br/> |<span data-ttu-id="93f10-109">0x3A20</span><span class="sxs-lookup"><span data-stu-id="93f10-109">0x3A20</span></span>  <br/> |
|<span data-ttu-id="93f10-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="93f10-110">Data type:</span></span>  <br/> |<span data-ttu-id="93f10-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="93f10-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="93f10-112">Область:</span><span class="sxs-lookup"><span data-stu-id="93f10-112">Area:</span></span>  <br/> |<span data-ttu-id="93f10-113">Address</span><span class="sxs-lookup"><span data-stu-id="93f10-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93f10-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="93f10-114">Remarks</span></span>

<span data-ttu-id="93f10-115">Эти свойства должны быть реализованы всеми поставщиками адресных книг.</span><span class="sxs-lookup"><span data-stu-id="93f10-115">These properties should be implemented by all address book providers.</span></span> <span data-ttu-id="93f10-116">Они содержат версию отображаемого имени получателя, передаваемого вместе с сообщением.</span><span class="sxs-lookup"><span data-stu-id="93f10-116">They contain the version of the recipient's display name that is transmitted with the message.</span></span> <span data-ttu-id="93f10-117">Для большинства поставщиков адресных книг эти свойства имеют то же значение, что и **PR_DISPLAY_NAME** ([PidTagDisplayName).](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="93f10-117">For most address book providers these properties have the same value as the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="93f10-118">Поставщики, не защищенные отображаемой именем, PT_ERROR MAPI изменяет отображаемую именем путем добавления кавычка вокруг имени.</span><span class="sxs-lookup"><span data-stu-id="93f10-118">Providers that do not have a secure display name return PT_ERROR and MAPI changes the display name by adding quotation marks around the name.</span></span>
  
<span data-ttu-id="93f10-119">Клиентские приложения могут использовать это свойство для предотвращения изменения или "спуфинга" записей.</span><span class="sxs-lookup"><span data-stu-id="93f10-119">A client application can use this property to prevent alteration or "spoofing" of entries.</span></span> <span data-ttu-id="93f10-120">Примером спуфинга является передача John Doe as John (What a Guy) Doe.</span><span class="sxs-lookup"><span data-stu-id="93f10-120">An example of spoofing is transmitting John Doe as John (What a Guy) Doe.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="93f10-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="93f10-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="93f10-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="93f10-122">Protocol specifications</span></span>

<span data-ttu-id="93f10-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93f10-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93f10-124">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="93f10-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="93f10-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93f10-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93f10-126">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93f10-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="93f10-127">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93f10-127">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93f10-128">Обрабатывает взаимодействие клиента с сервером интерфейса поставщика службы имен (NSPI).</span><span class="sxs-lookup"><span data-stu-id="93f10-128">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="93f10-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93f10-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93f10-130">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="93f10-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="93f10-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93f10-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93f10-132">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="93f10-132">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="93f10-133">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="93f10-133">Header files</span></span>

<span data-ttu-id="93f10-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="93f10-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="93f10-135">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="93f10-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="93f10-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="93f10-136">Mapitags.h</span></span>
  
> <span data-ttu-id="93f10-137">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="93f10-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93f10-138">См. также</span><span class="sxs-lookup"><span data-stu-id="93f10-138">See also</span></span>



[<span data-ttu-id="93f10-139">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="93f10-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93f10-140">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="93f10-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93f10-141">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="93f10-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93f10-142">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="93f10-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

