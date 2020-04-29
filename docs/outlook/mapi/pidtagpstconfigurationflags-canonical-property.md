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
# <a name="pidtagpstconfigurationflags-canonical-property"></a><span data-ttu-id="7c5e0-103">Каноническое свойство PidTagPstConfigurationFlags</span><span class="sxs-lookup"><span data-stu-id="7c5e0-103">PidTagPstConfigurationFlags Canonical Property</span></span>
  
<span data-ttu-id="7c5e0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c5e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c5e0-105">Флаги конфигурации спекфиес для таблицы личных запоминающих устройств (PST-файла).</span><span class="sxs-lookup"><span data-stu-id="7c5e0-105">Specfies configuration flags for a personal storage table (.pst file).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7c5e0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7c5e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c5e0-107">PR_PST_CONFIG_FLAGS</span><span class="sxs-lookup"><span data-stu-id="7c5e0-107">PR_PST_CONFIG_FLAGS</span></span>  <br/> |
|<span data-ttu-id="7c5e0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7c5e0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7c5e0-109">0x6770</span><span class="sxs-lookup"><span data-stu-id="7c5e0-109">0x6770</span></span>  <br/> |
|<span data-ttu-id="7c5e0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7c5e0-110">Data type:</span></span>  <br/> |<span data-ttu-id="7c5e0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7c5e0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7c5e0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7c5e0-112">Area:</span></span>  <br/> |<span data-ttu-id="7c5e0-113">Внутренняя таблица хранения личных данных (PST)</span><span class="sxs-lookup"><span data-stu-id="7c5e0-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c5e0-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="7c5e0-114">Remarks</span></span>

<span data-ttu-id="7c5e0-115">Ниже приведены допустимые значения для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="7c5e0-115">The following are valid values for this property:</span></span>
  
<span data-ttu-id="7c5e0-116">PST_CONFIG_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7c5e0-116">PST_CONFIG_UNICODE</span></span>
  
> <span data-ttu-id="7c5e0-117">Указывает PST-файл в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="7c5e0-117">Indicates a Unicode .pst file.</span></span> 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
<span data-ttu-id="7c5e0-118">PST_CONFIG_CREATE_NOWARN</span><span class="sxs-lookup"><span data-stu-id="7c5e0-118">PST_CONFIG_CREATE_NOWARN</span></span>
  
> <span data-ttu-id="7c5e0-119">При задании из флагов клиента в метод [имсгсервицеадмин:: конфигуремсгсервице](imsgserviceadmin-configuremsgservice.md) обрабатывает **Конфигуремсгсервице** , как [имсгсервицеадмин:: креатемсгсервице](imsgserviceadmin-createmsgservice.md) Call и пропускает предупреждение "Эта информационная служба не настроена".</span><span class="sxs-lookup"><span data-stu-id="7c5e0-119">When set from the client flags to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method, treats **ConfigureMsgService** like a [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) call and skips the "This information service has not been configured" warning.</span></span> 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
<span data-ttu-id="7c5e0-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="7c5e0-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span></span>
  
> <span data-ttu-id="7c5e0-121">Указывает **конфигуремсгсервице** не изменять значение свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), даже если оно было предоставлено.</span><span class="sxs-lookup"><span data-stu-id="7c5e0-121">Tells **ConfigureMsgService** to not change the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, even though it was supplied.</span></span> <span data-ttu-id="7c5e0-122">В этом случае он был предоставлен только для новых PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="7c5e0-122">In that case, it was supplied only for new .pst files.</span></span>
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
<span data-ttu-id="7c5e0-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span><span class="sxs-lookup"><span data-stu-id="7c5e0-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span></span>
  
> <span data-ttu-id="7c5e0-124">Указывает коду конфигурации сначала отобразить диалоговое окно, чтобы убедиться, что файл автономных папок (OST) найден, и в зависимости от ответа пользователя либо использовать найденную автономную папку, либо разрешить пользователю просматривать другую автономную папку.</span><span class="sxs-lookup"><span data-stu-id="7c5e0-124">Tells the configuration code to first display a dialog box to confirm whether an Offline Folder (.ost) file was found and, depending on the user's response, either use the found Offline Folder or enable the user to browse for another Offline Folder.</span></span>
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
<span data-ttu-id="7c5e0-125">OST_CONFIG_CREATE_NEW_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7c5e0-125">OST_CONFIG_CREATE_NEW_DEFAULT</span></span>
  
> <span data-ttu-id="7c5e0-126">Копирует OST-файл с новым уникальным именем и отменяет текущее имя.</span><span class="sxs-lookup"><span data-stu-id="7c5e0-126">Copies the .ost file with a new unique name and discards the current name.</span></span> <span data-ttu-id="7c5e0-127">Существующий OST-файл остается на компьютере, но больше не используется в этом профиле.</span><span class="sxs-lookup"><span data-stu-id="7c5e0-127">The existing .ost file remains on the computer but is no longer used in this profile.</span></span> <span data-ttu-id="7c5e0-128">Обычно это происходит в том случае, если Microsoft Outlook больше не разрешает определенный OST-файл, а политики реестра запрещают пользователю переименовывать файл.</span><span class="sxs-lookup"><span data-stu-id="7c5e0-128">This typically occurs when Microsoft Outlook no longer permits a particular .ost file, and registry policies do not allow the user to rename the file.</span></span> 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a><span data-ttu-id="7c5e0-129">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7c5e0-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7c5e0-130">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7c5e0-130">Protocol specifications</span></span>

<span data-ttu-id="7c5e0-131">[[MS — ОКСПРОПС]]</span><span class="sxs-lookup"><span data-stu-id="7c5e0-131">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="7c5e0-132">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7c5e0-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7c5e0-133">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7c5e0-133">Header files</span></span>

<span data-ttu-id="7c5e0-134">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="7c5e0-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c5e0-135">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7c5e0-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="7c5e0-136">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="7c5e0-136">Mapitags.h</span></span>
  
> <span data-ttu-id="7c5e0-137">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="7c5e0-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c5e0-138">См. также</span><span class="sxs-lookup"><span data-stu-id="7c5e0-138">See also</span></span>



[<span data-ttu-id="7c5e0-139">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7c5e0-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c5e0-140">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="7c5e0-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c5e0-141">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7c5e0-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c5e0-142">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7c5e0-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

