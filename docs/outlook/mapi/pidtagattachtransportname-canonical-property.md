---
title: Каноническое свойство PidTagAttachTransportName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTransportName
api_type:
- HeaderDef
ms.assetid: 701fca52-0f96-4019-80cd-c0ccd059ff9b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bd3a22bf55d03f3a9f06bf5c19650407bcc5627d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400518"
---
# <a name="pidtagattachtransportname-canonical-property"></a><span data-ttu-id="a409f-103">Каноническое свойство PidTagAttachTransportName</span><span class="sxs-lookup"><span data-stu-id="a409f-103">PidTagAttachTransportName Canonical Property</span></span>

  
  
<span data-ttu-id="a409f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a409f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a409f-105">Содержит имя файла вложения, изменена, поэтому его можно связать с сообщениями TNEF.</span><span class="sxs-lookup"><span data-stu-id="a409f-105">Contains the name of an attachment file modified so that it can be associated with TNEF messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a409f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a409f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a409f-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="a409f-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="a409f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a409f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a409f-109">0x370C</span><span class="sxs-lookup"><span data-stu-id="a409f-109">0x370C</span></span>  <br/> |
|<span data-ttu-id="a409f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a409f-110">Data type:</span></span>  <br/> |<span data-ttu-id="a409f-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a409f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a409f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a409f-112">Area:</span></span>  <br/> |<span data-ttu-id="a409f-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="a409f-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a409f-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a409f-114">Remarks</span></span>

<span data-ttu-id="a409f-115">Поставщик транспорта и TNEF использовать эти свойства.</span><span class="sxs-lookup"><span data-stu-id="a409f-115">TNEF and the transport provider use these properties.</span></span> <span data-ttu-id="a409f-116">Обычно не отображаются на клиентские приложения.</span><span class="sxs-lookup"><span data-stu-id="a409f-116">They are usually not available to client applications.</span></span> 
  
<span data-ttu-id="a409f-117">Эти свойства часто используемые TNEF при системы обмена сообщениями не поддерживает заданный имена файлов.</span><span class="sxs-lookup"><span data-stu-id="a409f-117">These properties are commonly used by TNEF when the underlying messaging system does not support the supplied filenames.</span></span> <span data-ttu-id="a409f-118">Например они используются при присоединении пользователя несколько файлов с тем же именем, например пять файлы с именем конфигурации. SYS.</span><span class="sxs-lookup"><span data-stu-id="a409f-118">For example, they are used when the user attaches multiple files with the same name, such as five files named CONFIG.SYS.</span></span> <span data-ttu-id="a409f-119">Поставщика транспорта необходимо изменить имена, чтобы убедиться в том, что они являются уникальными.</span><span class="sxs-lookup"><span data-stu-id="a409f-119">The transport provider must modify the names to make sure they are unique.</span></span> <span data-ttu-id="a409f-120">Имя каждого изменения отображается в **PR_ATTACH_TRANSPORT_NAME** его вложение и связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="a409f-120">Each modified name appears in its attachment's **PR_ATTACH_TRANSPORT_NAME** and associated properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a409f-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a409f-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a409f-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a409f-122">Protocol specifications</span></span>

<span data-ttu-id="a409f-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a409f-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a409f-124">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="a409f-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a409f-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a409f-125">Header files</span></span>

<span data-ttu-id="a409f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a409f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a409f-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a409f-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="a409f-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a409f-128">Mapitags.h</span></span>
  
> <span data-ttu-id="a409f-129">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="a409f-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a409f-130">См. также</span><span class="sxs-lookup"><span data-stu-id="a409f-130">See also</span></span>



[<span data-ttu-id="a409f-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a409f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a409f-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a409f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a409f-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a409f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a409f-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a409f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

