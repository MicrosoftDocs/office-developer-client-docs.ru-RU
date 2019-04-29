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
# <a name="pidtagpstconfigurationflags-canonical-property"></a><span data-ttu-id="b4868-103">Каноническое свойство PidTagPstConfigurationFlags</span><span class="sxs-lookup"><span data-stu-id="b4868-103">PidTagPstConfigurationFlags Canonical Property</span></span>
  
<span data-ttu-id="b4868-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4868-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4868-105">Флаги конфигурации Спекфиес для таблицы личных запоминающих устройств (PST-файла).</span><span class="sxs-lookup"><span data-stu-id="b4868-105">Specfies configuration flags for a personal storage table (.pst file).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b4868-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b4868-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4868-107">ПР_ПСТ_КОНФИГ_ФЛАГС</span><span class="sxs-lookup"><span data-stu-id="b4868-107">PR_PST_CONFIG_FLAGS</span></span>  <br/> |
|<span data-ttu-id="b4868-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b4868-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b4868-109">0x6770</span><span class="sxs-lookup"><span data-stu-id="b4868-109">0x6770</span></span>  <br/> |
|<span data-ttu-id="b4868-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b4868-110">Data type:</span></span>  <br/> |<span data-ttu-id="b4868-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b4868-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b4868-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b4868-112">Area:</span></span>  <br/> |<span data-ttu-id="b4868-113">Внутренняя таблица хранения личных данных (PST)</span><span class="sxs-lookup"><span data-stu-id="b4868-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4868-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b4868-114">Remarks</span></span>

<span data-ttu-id="b4868-115">Ниже приведены допустимые значения для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="b4868-115">The following are valid values for this property:</span></span>
  
<span data-ttu-id="b4868-116">ПСТ_КОНФИГ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="b4868-116">PST_CONFIG_UNICODE</span></span>
  
> <span data-ttu-id="b4868-117">Указывает PST-файл в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="b4868-117">Indicates a Unicode .pst file.</span></span> 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
<span data-ttu-id="b4868-118">ПСТ_КОНФИГ_КРЕАТЕ_НОВАРН</span><span class="sxs-lookup"><span data-stu-id="b4868-118">PST_CONFIG_CREATE_NOWARN</span></span>
  
> <span data-ttu-id="b4868-119">При задании из флагов клиента в метод [имсгсервицеадмин:: конфигуремсгсервице](imsgserviceadmin-configuremsgservice.md) обрабатывает **Конфигуремсгсервице** , как [имсгсервицеадмин:: креатемсгсервице](imsgserviceadmin-createmsgservice.md) Call и пропускает "Эта информационная служба не настроена". предупреждение.</span><span class="sxs-lookup"><span data-stu-id="b4868-119">When set from the client flags to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method, treats **ConfigureMsgService** like a [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) call and skips the "This information service has not been configured" warning.</span></span> 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
<span data-ttu-id="b4868-120">ПСТ_КОНФИГ_ПРЕСЕРВЕ_ДИСПЛАЙ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="b4868-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span></span>
  
> <span data-ttu-id="b4868-121">Указывает **конфигуремсгсервице** не изменять значение свойства **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), несмотря на то, что оно было предоставлено.</span><span class="sxs-lookup"><span data-stu-id="b4868-121">Tells **ConfigureMsgService** to not change the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, even though it was supplied.</span></span> <span data-ttu-id="b4868-122">В этом случае он был предоставлен только для новых PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="b4868-122">In that case, it was supplied only for new .pst files.</span></span>
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
<span data-ttu-id="b4868-123">ОСТ_КОНФИГ_ПОЛИЦИ_ДЕЛАЙ_ИГНОРЕ_ОСТ</span><span class="sxs-lookup"><span data-stu-id="b4868-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span></span>
  
> <span data-ttu-id="b4868-124">Указывает коду конфигурации сначала отобразить диалоговое окно, чтобы убедиться, что файл автономных папок (OST) найден, и в зависимости от ответа пользователя либо использовать найденную автономную папку, либо разрешить пользователю просматривать другую автономную папку.</span><span class="sxs-lookup"><span data-stu-id="b4868-124">Tells the configuration code to first display a dialog box to confirm whether an Offline Folder (.ost) file was found and, depending on the user's response, either use the found Offline Folder or enable the user to browse for another Offline Folder.</span></span>
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
<span data-ttu-id="b4868-125">ОСТ_КОНФИГ_КРЕАТЕ_НЕВ_ДЕФАУЛТ</span><span class="sxs-lookup"><span data-stu-id="b4868-125">OST_CONFIG_CREATE_NEW_DEFAULT</span></span>
  
> <span data-ttu-id="b4868-126">Копирует OST-файл с новым уникальным именем и отменяет текущее имя.</span><span class="sxs-lookup"><span data-stu-id="b4868-126">Copies the .ost file with a new unique name and discards the current name.</span></span> <span data-ttu-id="b4868-127">Существующий OST-файл остается на компьютере, но больше не используется в этом профиле.</span><span class="sxs-lookup"><span data-stu-id="b4868-127">The existing .ost file remains on the computer but is no longer used in this profile.</span></span> <span data-ttu-id="b4868-128">Обычно это происходит в том случае, если Microsoft Outlook больше не разрешает определенный OST-файл, а политики реестра запрещают пользователю переименовывать файл.</span><span class="sxs-lookup"><span data-stu-id="b4868-128">This typically occurs when Microsoft Outlook no longer permits a particular .ost file, and registry policies do not allow the user to rename the file.</span></span> 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a><span data-ttu-id="b4868-129">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b4868-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b4868-130">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b4868-130">Protocol specifications</span></span>

<span data-ttu-id="b4868-131">[[MS — ОКСПРОПС]]</span><span class="sxs-lookup"><span data-stu-id="b4868-131">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="b4868-132">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b4868-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b4868-133">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="b4868-133">Header files</span></span>

<span data-ttu-id="b4868-134">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b4868-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4868-135">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b4868-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="b4868-136">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="b4868-136">Mapitags.h</span></span>
  
> <span data-ttu-id="b4868-137">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="b4868-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4868-138">См. также</span><span class="sxs-lookup"><span data-stu-id="b4868-138">See also</span></span>



[<span data-ttu-id="b4868-139">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b4868-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4868-140">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="b4868-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4868-141">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b4868-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4868-142">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b4868-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

