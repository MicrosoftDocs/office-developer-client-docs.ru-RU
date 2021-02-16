---
title: Каноническое свойство PidTagResolveMethod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResolveMethod
api_type:
- COM
ms.assetid: 30d23c19-e0da-4511-9361-761153259216
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 14bb31ae9aebbb6441948b5756b426508107c9f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331404"
---
# <a name="pidtagresolvemethod-canonical-property"></a><span data-ttu-id="d0038-103">Каноническое свойство PidTagResolveMethod</span><span class="sxs-lookup"><span data-stu-id="d0038-103">PidTagResolveMethod Canonical Property</span></span>

  
  
<span data-ttu-id="d0038-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0038-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0038-105">Содержит значение разрешения конфликтов папки.</span><span class="sxs-lookup"><span data-stu-id="d0038-105">Contains a folder's conflict resolution value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d0038-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d0038-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d0038-107">PR_RESOLVE_METHOD</span><span class="sxs-lookup"><span data-stu-id="d0038-107">PR_RESOLVE_METHOD</span></span>  <br/> |
|<span data-ttu-id="d0038-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d0038-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d0038-109">0x3FE7</span><span class="sxs-lookup"><span data-stu-id="d0038-109">0x3FE7</span></span>  <br/> |
|<span data-ttu-id="d0038-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d0038-110">Data type:</span></span>  <br/> |<span data-ttu-id="d0038-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d0038-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d0038-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d0038-112">Area:</span></span>  <br/> |<span data-ttu-id="d0038-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="d0038-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0038-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d0038-114">Remarks</span></span>

<span data-ttu-id="d0038-115">Это свойство в папке, содержащей сообщение о разрешении конфликтов, указывает, как устранить конфликт.</span><span class="sxs-lookup"><span data-stu-id="d0038-115">This property on the folder containing the conflict resolution message will indicate how to resolve the conflict.</span></span> <span data-ttu-id="d0038-116">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="d0038-116">This property is not required.</span></span> <span data-ttu-id="d0038-117">Однако если этот флажок установлен, флаги, кроме следующих, не должны присутствовать:</span><span class="sxs-lookup"><span data-stu-id="d0038-117">However, if it is set, flags other than the following must not be present:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d0038-118">RESOLVE_METHOD_DEFAULT (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="d0038-118">RESOLVE_METHOD_DEFAULT (0x00000000)</span></span>  <br/> |<span data-ttu-id="d0038-119">Должно быть сгенерировано сообщение об устранении конфликтов.</span><span class="sxs-lookup"><span data-stu-id="d0038-119">Conflict resolve message should be generated.</span></span>  <br/> |
|<span data-ttu-id="d0038-120">RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="d0038-120">RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)</span></span>  <br/> |<span data-ttu-id="d0038-121">Переописывание целевого сообщения с примененными текущими изменениями.</span><span class="sxs-lookup"><span data-stu-id="d0038-121">Overwrite target message with current changes being applied.</span></span>  <br/> |
|<span data-ttu-id="d0038-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="d0038-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)</span></span>  <br/> |<span data-ttu-id="d0038-123">Не отправляйте сообщение с уведомлением о конфликте при создании сообщения о конфликте, разрешаемом в общедоступных папках.</span><span class="sxs-lookup"><span data-stu-id="d0038-123">Do not send conflict notification message when generating conflict resolve message in public folder.</span></span>  <br/> |
   
<span data-ttu-id="d0038-124">Клиент или сервер не должны создавать сообщения с разрешением конфликтов для связанных сообщений.</span><span class="sxs-lookup"><span data-stu-id="d0038-124">A client or server must not generate a conflict resolve message for associated messages.</span></span> <span data-ttu-id="d0038-125">Эти сообщения должны быть разрешены с **помощью** RESOLVE_METHOD_LAST_WRITER_WINS семантики.</span><span class="sxs-lookup"><span data-stu-id="d0038-125">These messages must be resolved by using **RESOLVE_METHOD_LAST_WRITER_WINS** semantics.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d0038-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d0038-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d0038-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d0038-127">Protocol specifications</span></span>

<span data-ttu-id="d0038-128">[[MS-OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0038-128">[[MS-OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0038-129">Обрабатывает синхронизацию данных объектов обмена сообщениями между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="d0038-129">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="d0038-130">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0038-130">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0038-131">Определяет основные структуры данных, используемые в удаленных операциях.</span><span class="sxs-lookup"><span data-stu-id="d0038-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d0038-132">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="d0038-132">Header files</span></span>

<span data-ttu-id="d0038-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d0038-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="d0038-134">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d0038-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="d0038-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d0038-135">Mapitags.h</span></span>
  
> <span data-ttu-id="d0038-136">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="d0038-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0038-137">См. также</span><span class="sxs-lookup"><span data-stu-id="d0038-137">See also</span></span>



[<span data-ttu-id="d0038-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d0038-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d0038-139">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d0038-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d0038-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d0038-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d0038-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d0038-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

