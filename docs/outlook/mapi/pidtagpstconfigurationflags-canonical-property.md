---
title: Каноническое свойство PidTagPstConfigurationFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e4234ddf-d9dc-4dc9-8eda-dbbee151b5d7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b5a3978741f7ecb871e3c3de28e52dffdcf3a74f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811598"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a><span data-ttu-id="b1d74-103">Каноническое свойство PidTagPstConfigurationFlags</span><span class="sxs-lookup"><span data-stu-id="b1d74-103">PidTagPstConfigurationFlags Canonical Property</span></span>
  
<span data-ttu-id="b1d74-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b1d74-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b1d74-105">Задает флаги конфигурации для таблицы личных папок (PST-файл).</span><span class="sxs-lookup"><span data-stu-id="b1d74-105">Specfies configuration flags for a personal storage table (.pst file).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b1d74-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b1d74-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b1d74-107">PR_PST_CONFIG_FLAGS</span><span class="sxs-lookup"><span data-stu-id="b1d74-107">PR_PST_CONFIG_FLAGS</span></span>  <br/> |
|<span data-ttu-id="b1d74-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b1d74-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b1d74-109">0x6770</span><span class="sxs-lookup"><span data-stu-id="b1d74-109">0x6770</span></span>  <br/> |
|<span data-ttu-id="b1d74-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b1d74-110">Data type:</span></span>  <br/> |<span data-ttu-id="b1d74-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b1d74-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b1d74-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b1d74-112">Area:</span></span>  <br/> |<span data-ttu-id="b1d74-113">Таблица личных папок (.pst) внутренний</span><span class="sxs-lookup"><span data-stu-id="b1d74-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1d74-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b1d74-114">Remarks</span></span>

<span data-ttu-id="b1d74-115">Ниже приведены допустимые значения для этого свойства:</span><span class="sxs-lookup"><span data-stu-id="b1d74-115">The following are valid values for this property:</span></span>
  
<span data-ttu-id="b1d74-116">PST_CONFIG_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b1d74-116">PST_CONFIG_UNICODE</span></span>
  
> <span data-ttu-id="b1d74-117">Указывает в Unicode PST-файл.</span><span class="sxs-lookup"><span data-stu-id="b1d74-117">Indicates a Unicode .pst file.</span></span> 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
<span data-ttu-id="b1d74-118">PST_CONFIG_CREATE_NOWARN</span><span class="sxs-lookup"><span data-stu-id="b1d74-118">PST_CONFIG_CREATE_NOWARN</span></span>
  
> <span data-ttu-id="b1d74-119">При набор из клиента помечает в метод [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) , обрабатывает **ConfigureMsgService** как звонок [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) и пропускает «эта служба сведения не было настроено» Предупреждение.</span><span class="sxs-lookup"><span data-stu-id="b1d74-119">When set from the client flags to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method, treats **ConfigureMsgService** like a [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) call and skips the "This information service has not been configured" warning.</span></span> 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
<span data-ttu-id="b1d74-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="b1d74-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span></span>
  
> <span data-ttu-id="b1d74-121">Указывает **ConfigureMsgService** не изменение значение свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), несмотря на то, что он был предоставлен.</span><span class="sxs-lookup"><span data-stu-id="b1d74-121">Tells **ConfigureMsgService** to not change the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, even though it was supplied.</span></span> <span data-ttu-id="b1d74-122">В этом случае он был предоставлен только для новых PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="b1d74-122">In that case, it was supplied only for new .pst files.</span></span>
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
<span data-ttu-id="b1d74-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span><span class="sxs-lookup"><span data-stu-id="b1d74-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span></span>
  
> <span data-ttu-id="b1d74-124">Указывает конфигурацию на первый экран диалоговое окно для подтверждения, была ли файл автономной папки (OST) найти и, в зависимости от ответа пользователя, либо использовать обнаруженного автономных папок или пользователь может выбрать другую папку автономный режим.</span><span class="sxs-lookup"><span data-stu-id="b1d74-124">Tells the configuration code to first display a dialog box to confirm whether an Offline Folder (.ost) file was found and, depending on the user's response, either use the found Offline Folder or enable the user to browse for another Offline Folder.</span></span>
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
<span data-ttu-id="b1d74-125">OST_CONFIG_CREATE_NEW_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="b1d74-125">OST_CONFIG_CREATE_NEW_DEFAULT</span></span>
  
> <span data-ttu-id="b1d74-126">Копирует OST-файла с новым уникальным именем и отменяет текущее имя.</span><span class="sxs-lookup"><span data-stu-id="b1d74-126">Copies the .ost file with a new unique name and discards the current name.</span></span> <span data-ttu-id="b1d74-127">Существующие OST-файла остается на компьютере, но больше не используется в этот профиль.</span><span class="sxs-lookup"><span data-stu-id="b1d74-127">The existing .ost file remains on the computer but is no longer used in this profile.</span></span> <span data-ttu-id="b1d74-128">Обычно это происходит, когда Microsoft Outlook больше не разрешает определенного OST-файла и политики реестра не разрешает пользователю переименуйте файл.</span><span class="sxs-lookup"><span data-stu-id="b1d74-128">This typically occurs when Microsoft Outlook no longer permits a particular .ost file, and registry policies do not allow the user to rename the file.</span></span> 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a><span data-ttu-id="b1d74-129">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b1d74-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b1d74-130">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b1d74-130">Protocol specifications</span></span>

<span data-ttu-id="b1d74-131">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="b1d74-131">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="b1d74-132">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b1d74-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b1d74-133">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b1d74-133">Header files</span></span>

<span data-ttu-id="b1d74-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1d74-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="b1d74-135">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b1d74-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="b1d74-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b1d74-136">Mapitags.h</span></span>
  
> <span data-ttu-id="b1d74-137">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="b1d74-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1d74-138">См. также</span><span class="sxs-lookup"><span data-stu-id="b1d74-138">See also</span></span>



[<span data-ttu-id="b1d74-139">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b1d74-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b1d74-140">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b1d74-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b1d74-141">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b1d74-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b1d74-142">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b1d74-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

