---
title: Каноническое свойство PidTagMessageEditorFormat
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageEditorFormat
api_type:
- HeaderDef
ms.assetid: 197b21ed-9f2f-425f-a6ed-cae1208fa2ca
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 029df4397f4d24c7c111d2017d34e6403df367d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325636"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a><span data-ttu-id="2f885-103">Каноническое свойство PidTagMessageEditorFormat</span><span class="sxs-lookup"><span data-stu-id="2f885-103">PidTagMessageEditorFormat Canonical Property</span></span>

  
  
<span data-ttu-id="2f885-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f885-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f885-105">Задает формат, используемый редактором для отображения сообщения.</span><span class="sxs-lookup"><span data-stu-id="2f885-105">Specifies the format for an editor to use to display a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2f885-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2f885-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2f885-107">ПР_МСГ_ЕДИТОР_ФОРМАТ</span><span class="sxs-lookup"><span data-stu-id="2f885-107">PR_MSG_EDITOR_FORMAT</span></span>  <br/> |
|<span data-ttu-id="2f885-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2f885-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2f885-109">0x5909</span><span class="sxs-lookup"><span data-stu-id="2f885-109">0x5909</span></span>  <br/> |
|<span data-ttu-id="2f885-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2f885-110">Data type:</span></span>  <br/> |<span data-ttu-id="2f885-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2f885-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2f885-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2f885-112">Area:</span></span>  <br/> |<span data-ttu-id="2f885-113">Разное</span><span class="sxs-lookup"><span data-stu-id="2f885-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f885-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2f885-114">Remarks</span></span>

<span data-ttu-id="2f885-115">Возможные значения для параметра **пр_мсг_едитор_формат** могут быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="2f885-115">The possible values for **PR_MSG_EDITOR_FORMAT** can be one of the following:</span></span> 
  
|<span data-ttu-id="2f885-116">**Value**</span><span class="sxs-lookup"><span data-stu-id="2f885-116">**Value**</span></span>|<span data-ttu-id="2f885-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2f885-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2f885-118">**ЕДИТОР_ФОРМАТ_ДОНТКНОВ**</span><span class="sxs-lookup"><span data-stu-id="2f885-118">**EDITOR_FORMAT_DONTKNOW**</span></span> <br/> |<span data-ttu-id="2f885-119">Неизвестный формат используемого редактора.</span><span class="sxs-lookup"><span data-stu-id="2f885-119">The format for the editor to use is unknown.</span></span>  <br/> |
|<span data-ttu-id="2f885-120">**ЕДИТОР_ФОРМАТ_ПЛАИНТЕКСТ**</span><span class="sxs-lookup"><span data-stu-id="2f885-120">**EDITOR_FORMAT_PLAINTEXT**</span></span> <br/> |<span data-ttu-id="2f885-121">Редактор должен отображать сообщение в формате обычного текста.</span><span class="sxs-lookup"><span data-stu-id="2f885-121">The editor should display the message in plain text format.</span></span>  <br/> |
|<span data-ttu-id="2f885-122">**ЕДИТОР_ФОРМАТ_ХТМЛ**</span><span class="sxs-lookup"><span data-stu-id="2f885-122">**EDITOR_FORMAT_HTML**</span></span> <br/> |<span data-ttu-id="2f885-123">Редактор должен отображать сообщение в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="2f885-123">The editor should display the message in HTML format.</span></span>  <br/> |
|<span data-ttu-id="2f885-124">**ЕДИТОР_ФОРМАТ_РТФ**</span><span class="sxs-lookup"><span data-stu-id="2f885-124">**EDITOR_FORMAT_RTF**</span></span> <br/> |<span data-ttu-id="2f885-125">Редактор должен отображать сообщение в формате RTF.</span><span class="sxs-lookup"><span data-stu-id="2f885-125">The editor should display the message in Rich Text Format.</span></span>  <br/> |
   
<span data-ttu-id="2f885-126">По умолчанию сообщения электронной почты (с классом сообщения **IPM. Примечание** или с настраиваемым классом сообщений, производным от **IPM. Note**), отправленные с учетной записи почты POP3/SMTP, отправляются в формате TNEF.</span><span class="sxs-lookup"><span data-stu-id="2f885-126">By default, mail messages (with the message class **IPM.Note** or with a custom message class derived from **IPM.Note**) sent from a POP3/SMTP mail account are sent in the Transport Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="2f885-127">Свойство **пр_мсг_едитор_формат** можно использовать для принудительного применения только обычного текста, а не TNEF при отправке сообщения.</span><span class="sxs-lookup"><span data-stu-id="2f885-127">The **PR_MSG_EDITOR_FORMAT** property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="2f885-128">Если для **пр_мсг_едитор_формат** задано значение **едитор_формат_плаинтекст**, сообщение отправляется в виде обычного текста без формата TNEF.</span><span class="sxs-lookup"><span data-stu-id="2f885-128">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_PLAINTEXT**, the message is sent as plain text without TNEF.</span></span> <span data-ttu-id="2f885-129">Если для **пр_мсг_едитор_формат** задано значение **едитор_формат_ртф**, кодировка TNEF неявно включена, а сообщение отправляется с использованием формата Интернета по умолчанию, указанного в клиенте Outlook.</span><span class="sxs-lookup"><span data-stu-id="2f885-129">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_RTF**, TNEF encoding is implicitly enabled, and the message is sent by using the default Internet format that is specified in the Outlook client.</span></span>
  
<span data-ttu-id="2f885-130">Существует два других способа применения формата TNEF при отправке сообщения.</span><span class="sxs-lookup"><span data-stu-id="2f885-130">There are two other ways to enforce the use of TNEF when sending a message.</span></span>
  
- <span data-ttu-id="2f885-131">Если задать для свойства с именем **диспидусетнеф** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) значение true в сообщении, то при преобразовании сообщения из MAPI в MIME/SMTP необходимо включить формат TNEF.</span><span class="sxs-lookup"><span data-stu-id="2f885-131">Setting the **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) named property to True on a message indicates TNEF should be included when converting the message from MAPI to MIME/SMTP.</span></span> <span data-ttu-id="2f885-132">Обратите внимание, что **диспидусетнеф** применяется только в том случае, если сообщение отправлено с учетной записи электронной почты POP3/SMTP и не применяется, когда сообщение отправляется другими поставщиками, например Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2f885-132">Note that **dispidUseTNEF** only applies when the message is sent from a POP3/SMTP mail account, and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="2f885-133">**диспидусетнеф** переопределяет параметр в **пр_мсг_едитор_формат**.</span><span class="sxs-lookup"><span data-stu-id="2f885-133">**dispidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**.</span></span>
    
- <span data-ttu-id="2f885-134">Использование флага **кксф_усе_тнеф** при вызове [Иконвертерсессион:: мапитомиместм](iconvertersession-mapitomimestm.md) для преобразования исходящего сообщения MAPI в MIME поток также может применять TNEF.</span><span class="sxs-lookup"><span data-stu-id="2f885-134">Using the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="2f885-135">Это свойство применяется, даже если **диспидусетнеф** не задано.</span><span class="sxs-lookup"><span data-stu-id="2f885-135">This applies even if **dispidUseTNEF** is not set.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="2f885-136">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2f885-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2f885-137">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2f885-137">Protocol specifications</span></span>

<span data-ttu-id="2f885-138">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f885-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f885-139">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2f885-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2f885-140">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f885-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f885-141">Определяет основные структуры данных, используемые в удаленных операциях.</span><span class="sxs-lookup"><span data-stu-id="2f885-141">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="2f885-142">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f885-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f885-143">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2f885-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2f885-144">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="2f885-144">Header files</span></span>

<span data-ttu-id="2f885-145">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="2f885-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="2f885-146">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2f885-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="2f885-147">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="2f885-147">Mapitags.h</span></span>
  
> <span data-ttu-id="2f885-148">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="2f885-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2f885-149">См. также</span><span class="sxs-lookup"><span data-stu-id="2f885-149">See also</span></span>



[<span data-ttu-id="2f885-150">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2f885-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2f885-151">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="2f885-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2f885-152">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2f885-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2f885-153">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2f885-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

