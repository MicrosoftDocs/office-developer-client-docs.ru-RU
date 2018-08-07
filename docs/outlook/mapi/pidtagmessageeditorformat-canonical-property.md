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
ms.openlocfilehash: a6a3eb88377777a3d27687179bfdcb82057be3a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811365"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a><span data-ttu-id="96a35-103">Каноническое свойство PidTagMessageEditorFormat</span><span class="sxs-lookup"><span data-stu-id="96a35-103">PidTagMessageEditorFormat Canonical Property</span></span>

  
  
<span data-ttu-id="96a35-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="96a35-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="96a35-105">Задает формат для редактор, используемый для отображения сообщения.</span><span class="sxs-lookup"><span data-stu-id="96a35-105">Specifies the format for an editor to use to display a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="96a35-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="96a35-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="96a35-107">PR_MSG_EDITOR_FORMAT</span><span class="sxs-lookup"><span data-stu-id="96a35-107">PR_MSG_EDITOR_FORMAT</span></span>  <br/> |
|<span data-ttu-id="96a35-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="96a35-108">Identifier:</span></span>  <br/> |<span data-ttu-id="96a35-109">0x5909</span><span class="sxs-lookup"><span data-stu-id="96a35-109">0x5909</span></span>  <br/> |
|<span data-ttu-id="96a35-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="96a35-110">Data type:</span></span>  <br/> |<span data-ttu-id="96a35-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="96a35-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="96a35-112">Область:</span><span class="sxs-lookup"><span data-stu-id="96a35-112">Area:</span></span>  <br/> |<span data-ttu-id="96a35-113">Разное</span><span class="sxs-lookup"><span data-stu-id="96a35-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96a35-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="96a35-114">Remarks</span></span>

<span data-ttu-id="96a35-115">Возможные значения для **PR_MSG_EDITOR_FORMAT** может иметь одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="96a35-115">The possible values for **PR_MSG_EDITOR_FORMAT** can be one of the following:</span></span> 
  
|<span data-ttu-id="96a35-116">**Значение**</span><span class="sxs-lookup"><span data-stu-id="96a35-116">**Value**</span></span>|<span data-ttu-id="96a35-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="96a35-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="96a35-118">**EDITOR_FORMAT_DONTKNOW**</span><span class="sxs-lookup"><span data-stu-id="96a35-118">**EDITOR_FORMAT_DONTKNOW**</span></span> <br/> |<span data-ttu-id="96a35-119">Формат редактора использовать неизвестен.</span><span class="sxs-lookup"><span data-stu-id="96a35-119">The format for the editor to use is unknown.</span></span>  <br/> |
|<span data-ttu-id="96a35-120">**EDITOR_FORMAT_PLAINTEXT**</span><span class="sxs-lookup"><span data-stu-id="96a35-120">**EDITOR_FORMAT_PLAINTEXT**</span></span> <br/> |<span data-ttu-id="96a35-121">Редактор должны отображать сообщения в формате обычного текста.</span><span class="sxs-lookup"><span data-stu-id="96a35-121">The editor should display the message in plain text format.</span></span>  <br/> |
|<span data-ttu-id="96a35-122">**EDITOR_FORMAT_HTML**</span><span class="sxs-lookup"><span data-stu-id="96a35-122">**EDITOR_FORMAT_HTML**</span></span> <br/> |<span data-ttu-id="96a35-123">Редактор должны отображать сообщения в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="96a35-123">The editor should display the message in HTML format.</span></span>  <br/> |
|<span data-ttu-id="96a35-124">**EDITOR_FORMAT_RTF**</span><span class="sxs-lookup"><span data-stu-id="96a35-124">**EDITOR_FORMAT_RTF**</span></span> <br/> |<span data-ttu-id="96a35-125">Редактор должны отображать сообщения в формате RTF.</span><span class="sxs-lookup"><span data-stu-id="96a35-125">The editor should display the message in Rich Text Format.</span></span>  <br/> |
   
<span data-ttu-id="96a35-126">По умолчанию почтовые сообщения (с классом сообщения **IPM. Примечание** или с помощью настраиваемого сообщения класс, производный от **IPM. Обратите внимание на то**) отправляются из почты POP3/SMTP учетной записи, передаются в транспорта Neutral Encapsulation формата TNEF.</span><span class="sxs-lookup"><span data-stu-id="96a35-126">By default, mail messages (with the message class **IPM.Note** or with a custom message class derived from **IPM.Note**) sent from a POP3/SMTP mail account are sent in the Transport Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="96a35-127">Свойство **PR_MSG_EDITOR_FORMAT** можно использовать для применения параметров только обычный текст и не TNEF при отправке сообщения.</span><span class="sxs-lookup"><span data-stu-id="96a35-127">The **PR_MSG_EDITOR_FORMAT** property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="96a35-128">Если **PR_MSG_EDITOR_FORMAT** **EDITOR_FORMAT_PLAINTEXT**, сообщение отправляется в виде обычного текста без TNEF.</span><span class="sxs-lookup"><span data-stu-id="96a35-128">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_PLAINTEXT**, the message is sent as plain text without TNEF.</span></span> <span data-ttu-id="96a35-129">Если **PR_MSG_EDITOR_FORMAT** **EDITOR_FORMAT_RTF**, кодировка TNEF неявно включен, а сообщение отправляется в формате Интернета по умолчанию, который указан в клиенте Outlook.</span><span class="sxs-lookup"><span data-stu-id="96a35-129">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_RTF**, TNEF encoding is implicitly enabled, and the message is sent by using the default Internet format that is specified in the Outlook client.</span></span>
  
<span data-ttu-id="96a35-130">Существует два способа внедрить использование TNEF при отправке сообщения.</span><span class="sxs-lookup"><span data-stu-id="96a35-130">There are two other ways to enforce the use of TNEF when sending a message.</span></span>
  
- <span data-ttu-id="96a35-131">Параметр **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) с именем значение True для сообщения указывает, что TNEF должны быть включены при преобразовании сообщения из MAPI MIME/SMTP.</span><span class="sxs-lookup"><span data-stu-id="96a35-131">Setting the **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) named property to True on a message indicates TNEF should be included when converting the message from MAPI to MIME/SMTP.</span></span> <span data-ttu-id="96a35-132">Обратите внимание, что этот **dispidUseTNEF** применяется только в том случае, когда сообщение отправляется с учетной записью электронной почты POP3/SMTP и не применяется, если сообщение отправляется с другими поставщиками, такими как Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="96a35-132">Note that **dispidUseTNEF** only applies when the message is sent from a POP3/SMTP mail account, and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="96a35-133">**dispidUseTNEF** переопределяет параметр **PR_MSG_EDITOR_FORMAT**.</span><span class="sxs-lookup"><span data-stu-id="96a35-133">**dispidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**.</span></span>
    
- <span data-ttu-id="96a35-134">С помощью флага **CCSF_USE_TNEF** при вызове [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) для преобразования исходящих сообщений MAPI в MIME-поток также обеспечивают TNEF.</span><span class="sxs-lookup"><span data-stu-id="96a35-134">Using the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="96a35-135">Это относится даже в том случае, если не указано **dispidUseTNEF** .</span><span class="sxs-lookup"><span data-stu-id="96a35-135">This applies even if **dispidUseTNEF** is not set.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="96a35-136">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="96a35-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="96a35-137">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="96a35-137">Protocol specifications</span></span>

<span data-ttu-id="96a35-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96a35-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96a35-139">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="96a35-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="96a35-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96a35-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96a35-141">Определяет структуры основных данных, которые используются для удаленных операций.</span><span class="sxs-lookup"><span data-stu-id="96a35-141">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="96a35-142">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96a35-142">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96a35-143">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="96a35-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="96a35-144">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="96a35-144">Header files</span></span>

<span data-ttu-id="96a35-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96a35-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="96a35-146">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="96a35-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="96a35-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="96a35-147">Mapitags.h</span></span>
  
> <span data-ttu-id="96a35-148">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="96a35-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96a35-149">См. также</span><span class="sxs-lookup"><span data-stu-id="96a35-149">See also</span></span>



[<span data-ttu-id="96a35-150">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="96a35-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="96a35-151">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="96a35-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="96a35-152">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="96a35-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="96a35-153">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="96a35-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

