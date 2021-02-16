---
title: Каноническое свойство PidTagAttachExtension
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachExtension
api_type:
- HeaderDef
ms.assetid: 667da30b-e11c-4040-aecf-bb35eed23722
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 26efa868de29bc8a6a180b717230951b76da26a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319763"
---
# <a name="pidtagattachextension-canonical-property"></a><span data-ttu-id="4cdfa-103">Каноническое свойство PidTagAttachExtension</span><span class="sxs-lookup"><span data-stu-id="4cdfa-103">PidTagAttachExtension Canonical Property</span></span>

  
  
<span data-ttu-id="4cdfa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cdfa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cdfa-105">Содержит расширение имени файла, которое указывает тип документа вложения.</span><span class="sxs-lookup"><span data-stu-id="4cdfa-105">Contains a file name extension that indicates the document type of an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4cdfa-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4cdfa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4cdfa-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span><span class="sxs-lookup"><span data-stu-id="4cdfa-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span></span>  <br/> |
|<span data-ttu-id="4cdfa-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4cdfa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4cdfa-109">0x3703</span><span class="sxs-lookup"><span data-stu-id="4cdfa-109">0x3703</span></span>  <br/> |
|<span data-ttu-id="4cdfa-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4cdfa-110">Data type:</span></span>  <br/> |<span data-ttu-id="4cdfa-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4cdfa-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4cdfa-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4cdfa-112">Area:</span></span>  <br/> |<span data-ttu-id="4cdfa-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="4cdfa-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cdfa-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="4cdfa-114">Remarks</span></span>

<span data-ttu-id="4cdfa-115">Эти свойства устанавливаются клиентской приложением во время отправки.</span><span class="sxs-lookup"><span data-stu-id="4cdfa-115">These properties are set by the client application at submission time.</span></span> 
  
<span data-ttu-id="4cdfa-116">Система обмена сообщениями  использует PR_ATTACH_EXTENSION при преобразовании вложений сообщений (преобразование в маршруте) или запуске приложений на основе вложений в полученных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="4cdfa-116">The messaging system uses **PR_ATTACH_EXTENSION** when converting message attachments (in-route conversion) or launching applications based on attachments in received messages.</span></span> <span data-ttu-id="4cdfa-117">Если отправляющий клиент не предоставляет значение для этих свойств, хранилище сообщений, которое занимается вложением, не обязано его создавать.</span><span class="sxs-lookup"><span data-stu-id="4cdfa-117">If the sending client does not provide a value for these properties, the message store handling the attachment is not obligated to generate it.</span></span> <span data-ttu-id="4cdfa-118">Принимающий клиент должен сначала проверить PR_ATTACH_EXTENSION , и если он не предоставлен, следует синтацировать расширение имени файла из свойства **PR_ATTACH_FILENAME** [(PidTagAttachFilename)](pidtagattachfilename-canonical-property.md)или **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename).](pidtagattachlongfilename-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="4cdfa-118">The receiving client should first check for **PR_ATTACH_EXTENSION**, and if it is not provided, should parse the file name extension from the attachment's **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) or **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4cdfa-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4cdfa-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4cdfa-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4cdfa-120">Protocol specifications</span></span>

<span data-ttu-id="4cdfa-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4cdfa-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4cdfa-122">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="4cdfa-122">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4cdfa-123">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="4cdfa-123">Header files</span></span>

<span data-ttu-id="4cdfa-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4cdfa-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="4cdfa-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4cdfa-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="4cdfa-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4cdfa-126">Mapitags.h</span></span>
  
> <span data-ttu-id="4cdfa-127">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="4cdfa-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4cdfa-128">См. также</span><span class="sxs-lookup"><span data-stu-id="4cdfa-128">See also</span></span>



[<span data-ttu-id="4cdfa-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4cdfa-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4cdfa-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4cdfa-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4cdfa-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4cdfa-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4cdfa-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4cdfa-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

