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
ms.openlocfilehash: e881c8eeffa29706591e07113d70a3670606f2be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408945"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a><span data-ttu-id="e0b08-103">Каноническое свойство PidTagPstConfigurationFlags</span><span class="sxs-lookup"><span data-stu-id="e0b08-103">PidTagPstConfigurationFlags Canonical Property</span></span>
  
<span data-ttu-id="e0b08-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0b08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0b08-105">Флажки конфигурации для личной таблицы хранения (PST-файла).</span><span class="sxs-lookup"><span data-stu-id="e0b08-105">Specfies configuration flags for a personal storage table (.pst file).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e0b08-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e0b08-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e0b08-107">PR_PST_CONFIG_FLAGS</span><span class="sxs-lookup"><span data-stu-id="e0b08-107">PR_PST_CONFIG_FLAGS</span></span>  <br/> |
|<span data-ttu-id="e0b08-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e0b08-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e0b08-109">0x6770</span><span class="sxs-lookup"><span data-stu-id="e0b08-109">0x6770</span></span>  <br/> |
|<span data-ttu-id="e0b08-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e0b08-110">Data type:</span></span>  <br/> |<span data-ttu-id="e0b08-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e0b08-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e0b08-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e0b08-112">Area:</span></span>  <br/> |<span data-ttu-id="e0b08-113">Внутренняя таблица личных хранилищ (PST)</span><span class="sxs-lookup"><span data-stu-id="e0b08-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0b08-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e0b08-114">Remarks</span></span>

<span data-ttu-id="e0b08-115">Для этого свойства допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e0b08-115">The following are valid values for this property:</span></span>
  
<span data-ttu-id="e0b08-116">PST_CONFIG_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e0b08-116">PST_CONFIG_UNICODE</span></span>
  
> <span data-ttu-id="e0b08-117">Указывает PST-файл Юникода.</span><span class="sxs-lookup"><span data-stu-id="e0b08-117">Indicates a Unicode .pst file.</span></span> 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
<span data-ttu-id="e0b08-118">PST_CONFIG_CREATE_NOWARN</span><span class="sxs-lookup"><span data-stu-id="e0b08-118">PST_CONFIG_CREATE_NOWARN</span></span>
  
> <span data-ttu-id="e0b08-119">Если для метода [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) заданная от флагов клиента, **configureMsgService** обрабатывается как вызов [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) и пропускает предупреждение "Эта служба сведений не настроена".</span><span class="sxs-lookup"><span data-stu-id="e0b08-119">When set from the client flags to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method, treats **ConfigureMsgService** like a [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) call and skips the "This information service has not been configured" warning.</span></span> 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
<span data-ttu-id="e0b08-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="e0b08-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span></span>
  
> <span data-ttu-id="e0b08-121">Сообщает **ConfigureMsgService,** чтобы не изменять значение свойства **PR_DISPLAY_NAME** ([PidTagDisplayName),](pidtagdisplayname-canonical-property.md)даже если оно было предоставлено.</span><span class="sxs-lookup"><span data-stu-id="e0b08-121">Tells **ConfigureMsgService** to not change the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, even though it was supplied.</span></span> <span data-ttu-id="e0b08-122">В этом случае она была предоставлена только для новых PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="e0b08-122">In that case, it was supplied only for new .pst files.</span></span>
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
<span data-ttu-id="e0b08-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span><span class="sxs-lookup"><span data-stu-id="e0b08-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span></span>
  
> <span data-ttu-id="e0b08-124">Сообщает коду конфигурации, чтобы сначала отобразить диалоговое окно, чтобы подтвердить, что файл автономной папки (OST) найден, и, в зависимости от ответа пользователя, использовать найденную папку в автономном режиме или позволить пользователю найти другую папку в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="e0b08-124">Tells the configuration code to first display a dialog box to confirm whether an Offline Folder (.ost) file was found and, depending on the user's response, either use the found Offline Folder or enable the user to browse for another Offline Folder.</span></span>
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
<span data-ttu-id="e0b08-125">OST_CONFIG_CREATE_NEW_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="e0b08-125">OST_CONFIG_CREATE_NEW_DEFAULT</span></span>
  
> <span data-ttu-id="e0b08-126">Копирует OST-файл с новым уникальным именем и удаляет текущее имя.</span><span class="sxs-lookup"><span data-stu-id="e0b08-126">Copies the .ost file with a new unique name and discards the current name.</span></span> <span data-ttu-id="e0b08-127">Существующий OST-файл остается на компьютере, но больше не используется в этом профиле.</span><span class="sxs-lookup"><span data-stu-id="e0b08-127">The existing .ost file remains on the computer but is no longer used in this profile.</span></span> <span data-ttu-id="e0b08-128">Обычно это происходит, когда Microsoft Outlook больше не разрешает определенный OST-файл, а политики реестра не позволяют пользователю переименовывать файл.</span><span class="sxs-lookup"><span data-stu-id="e0b08-128">This typically occurs when Microsoft Outlook no longer permits a particular .ost file, and registry policies do not allow the user to rename the file.</span></span> 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a><span data-ttu-id="e0b08-129">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e0b08-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e0b08-130">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e0b08-130">Protocol specifications</span></span>

<span data-ttu-id="e0b08-131">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="e0b08-131">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="e0b08-132">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="e0b08-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e0b08-133">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="e0b08-133">Header files</span></span>

<span data-ttu-id="e0b08-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e0b08-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="e0b08-135">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e0b08-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="e0b08-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e0b08-136">Mapitags.h</span></span>
  
> <span data-ttu-id="e0b08-137">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="e0b08-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0b08-138">См. также</span><span class="sxs-lookup"><span data-stu-id="e0b08-138">See also</span></span>



[<span data-ttu-id="e0b08-139">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e0b08-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e0b08-140">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e0b08-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e0b08-141">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e0b08-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e0b08-142">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e0b08-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

