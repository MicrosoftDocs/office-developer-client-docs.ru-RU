---
title: Каноническое свойство PidTagStoreUnicodeMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreUnicodeMask
api_type:
- COM
ms.assetid: a6082162-2a74-4850-a0df-4bdbc67b41d8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e15c259003ed2cb425eb181f4383f3054967b993
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437940"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a><span data-ttu-id="75332-103">Каноническое свойство PidTagStoreUnicodeMask</span><span class="sxs-lookup"><span data-stu-id="75332-103">PidTagStoreUnicodeMask Canonical Property</span></span>

  
  
<span data-ttu-id="75332-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75332-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75332-105">Содержит битовуюmass флагов, которые клиентские приложения должны запросить, чтобы определить характеристики хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="75332-105">Contains a bitmask of flags that client applications should query to determine the characteristics of a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="75332-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="75332-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75332-107">PR_STORE_UNICODE_MASK</span><span class="sxs-lookup"><span data-stu-id="75332-107">PR_STORE_UNICODE_MASK</span></span>  <br/> |
|<span data-ttu-id="75332-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="75332-108">Identifier:</span></span>  <br/> |<span data-ttu-id="75332-109">0x340F</span><span class="sxs-lookup"><span data-stu-id="75332-109">0x340F</span></span>  <br/> |
|<span data-ttu-id="75332-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="75332-110">Data type:</span></span>  <br/> |<span data-ttu-id="75332-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="75332-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="75332-112">Область:</span><span class="sxs-lookup"><span data-stu-id="75332-112">Area:</span></span>  <br/> |<span data-ttu-id="75332-113">Хранилище сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="75332-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75332-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="75332-114">Remarks</span></span>

<span data-ttu-id="75332-115">Это свойство раскрывает возможности хранения сообщений для клиентских приложений, планируя отправку сообщения.</span><span class="sxs-lookup"><span data-stu-id="75332-115">This property discloses the capabilities of a message store to client applications planning to send it a message.</span></span> <span data-ttu-id="75332-116">Флаги могут упростить принятие решений клиентом или другим хранилищем, например, нужно ли отправлять PR_BODY **(** [PidTagBody)](pidtagbody-canonical-property.md)или только PR_RTF_COMPRESSED **(** [PidTagRtfCompressed).](pidtagrtfcompressed-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="75332-116">The flags can facilitate decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="75332-117">Клиент никогда не должен устанавливать это свойство.</span><span class="sxs-lookup"><span data-stu-id="75332-117">A client should never set this property.</span></span> <span data-ttu-id="75332-118">Попытка возвращает **MAPI_E_COMPUTED**.</span><span class="sxs-lookup"><span data-stu-id="75332-118">An attempt returns **MAPI_E_COMPUTED**.</span></span> 
  
<span data-ttu-id="75332-119">Для этого свойства можно установить один или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="75332-119">One or more of the following flags can be set for this property:</span></span> 
  
<span data-ttu-id="75332-120">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="75332-120">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="75332-121">(131072, 0x00020000) Хранилище сообщений поддерживает свойства, содержащие символы Американского национального института стандартов (ANSI) (8-битные).</span><span class="sxs-lookup"><span data-stu-id="75332-121">(131072, 0x00020000) The message store supports properties that contain American National Standards Institute (ANSI) (8-bit) characters.</span></span>
    
<span data-ttu-id="75332-122">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="75332-122">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="75332-123">(32, 0x00000020) Хранилище сообщений поддерживает привязку и вложения объектов (OLE) или вложения, не вложенные в OLE, в сообщения.</span><span class="sxs-lookup"><span data-stu-id="75332-123">(32, 0x00000020) The message store supports Object Linking and Embedding (OLE) or non-OLE attachments to messages.</span></span> 
    
<span data-ttu-id="75332-124">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="75332-124">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="75332-125">(1024, 0x00000400) Хранилище сообщений поддерживает классификацию представлений таблиц.</span><span class="sxs-lookup"><span data-stu-id="75332-125">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="75332-126">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="75332-126">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="75332-127">(16, 0x00000010) Хранилище сообщений поддерживает создание новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="75332-127">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="75332-128">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="75332-128">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="75332-129">(1, 0x00000001) Идентификаторы записей для объектов в хранилище сообщений уникальны, то есть никогда не повторно в течение всего жизненного года хранения.</span><span class="sxs-lookup"><span data-stu-id="75332-129">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="75332-130">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="75332-130">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="75332-131">(65536, 0x00010000) Хранилище сообщений поддерживает HTML-сообщения, хранимые в свойстве **PR_BODY_HTML** ([PidTagBodyHtml).](pidtagbodyhtml-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="75332-131">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="75332-132">Обратите **внимание STORE_HTML_OK** что в версиях MAPIDEFS не заданная STORE_HTML_OK не определена. H, которые входят в состав Microsoft Exchange 2000 Server и более ранних.</span><span class="sxs-lookup"><span data-stu-id="75332-132">Note that **STORE_HTML_OK** is not defined in versions of MAPIDEFS.H that are included with Microsoft Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="75332-133">Если в среде разработки используется MAPIDEFS. H-файл, который не **включает** STORE_HTML_OK, используйте значение "0x00010000".</span><span class="sxs-lookup"><span data-stu-id="75332-133">If your development environment uses a MAPIDEFS.H file that does not include **STORE_HTML_OK**, use the value "0x00010000" instead.</span></span> 
    
<span data-ttu-id="75332-134">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="75332-134">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="75332-135">(2097152, 0x00200000) В упакованном хранилище PST-данных указывает, что когда новое сообщение поступает в магазин, хранилище обрабатывает правила и фильтрацию нежелательной почты отдельно.</span><span class="sxs-lookup"><span data-stu-id="75332-135">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store does rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="75332-136">Магазин вызывает [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** в структуре [NOTIFICATION,](notification.md) которая передается в качестве параметра, а затем передает сведения о новом сообщении клиенту прослушивания.</span><span class="sxs-lookup"><span data-stu-id="75332-136">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="75332-137">Впоследствии, когда прослушивающий клиент получает уведомление, к сообщению не применяются правила.</span><span class="sxs-lookup"><span data-stu-id="75332-137">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="75332-138">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="75332-138">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="75332-139">(524288, 0x00080000) Этот флаг зарезервирован и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="75332-139">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="75332-140">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="75332-140">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="75332-141">(8, 0x00000008) Хранилище сообщений поддерживает изменение существующих сообщений.</span><span class="sxs-lookup"><span data-stu-id="75332-141">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="75332-142">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="75332-142">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="75332-143">(512, 0x00000200) Хранилище сообщений поддерживает многооценные свойства, гарантирует стабильность порядка значений в многоценном свойстве в ходе операции сохранения и поддерживает моментацию многоценных свойств в таблицах.</span><span class="sxs-lookup"><span data-stu-id="75332-143">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="75332-144">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="75332-144">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="75332-145">(256, 0x00000100) Хранилище сообщений поддерживает уведомления.</span><span class="sxs-lookup"><span data-stu-id="75332-145">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="75332-146">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="75332-146">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="75332-147">(64, 0x00000040) Хранилище сообщений поддерживает вложения OLE.</span><span class="sxs-lookup"><span data-stu-id="75332-147">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="75332-148">Данные OLE доступны через **интерфейс IStorage,** например через **свойство PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject).](pidtagattachdataobject-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="75332-148">The OLE data is accessible through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="75332-149">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="75332-149">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="75332-150">(16384, 0x00004000) Папки в этом хранилище являются общедоступными (несколькими пользователями), а не частными (возможно, с несколькими экземплярами, но не с несколькими пользователями).</span><span class="sxs-lookup"><span data-stu-id="75332-150">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="75332-151">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="75332-151">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="75332-152">(8388608, 0x00800000) Обработщик протокола MAPI не будет обходить хранилище, и хранилище будет отправлять индексе все изменения с помощью уведомлений для индексации сообщений.</span><span class="sxs-lookup"><span data-stu-id="75332-152">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="75332-153">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="75332-153">STORE_READONLY</span></span> 
  
> <span data-ttu-id="75332-154">(2, 0x00000002) Все интерфейсы для хранения сообщений имеют доступ только для чтения.</span><span class="sxs-lookup"><span data-stu-id="75332-154">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="75332-155">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="75332-155">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="75332-156">(4096, 0x00001000) Хранилище сообщений поддерживает ограничения.</span><span class="sxs-lookup"><span data-stu-id="75332-156">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="75332-157">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="75332-157">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="75332-158">(2048, 0x00000800) Хранилище сообщений поддерживает сообщения в формате RTF (обычно сжатые),  а само хранилище сохраняет PR_BODY и **PR_RTF_COMPRESSED** синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="75332-158">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="75332-159">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="75332-159">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="75332-160">(4, 0x00000004) Хранилище сообщений поддерживает папки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="75332-160">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="75332-161">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="75332-161">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="75332-162">(8192, 0x00002000) Хранилище сообщений поддерживает сортировку представлений таблиц.</span><span class="sxs-lookup"><span data-stu-id="75332-162">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="75332-163">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="75332-163">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="75332-164">(128, 0x00000080) Хранилище сообщений поддерживает пометку сообщения для отправки.</span><span class="sxs-lookup"><span data-stu-id="75332-164">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="75332-165">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="75332-165">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="75332-166">(32768, 0x00008000) Хранилище сообщений поддерживает хранение измененных текстовых сообщений формы (RTF) в несжимаемой форме.</span><span class="sxs-lookup"><span data-stu-id="75332-166">(32768, 0x00008000) The message store supports storage of revisable form text (RTF) messages in uncompressed form.</span></span> <span data-ttu-id="75332-167">Несхваченный поток RTF идентифицирован значением **dwMagicUncompressedRTF** в загоне потока.</span><span class="sxs-lookup"><span data-stu-id="75332-167">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="75332-168">Значение **dwMagicUncompressedRTF** определяется в RTFLIB. H-файл.</span><span class="sxs-lookup"><span data-stu-id="75332-168">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="75332-169">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="75332-169">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="75332-170">(262144, 0x00040000) Хранилище сообщений поддерживает свойства, содержащие символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="75332-170">(262144, 0x00040000) The message store supports properties containing Unicode characters.</span></span>
    
<span data-ttu-id="75332-171">Версию сообщения в RTF всегда можно сохранить, даже если хранилище сообщений не имеет RTF-данных.</span><span class="sxs-lookup"><span data-stu-id="75332-171">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="75332-172">Если STORE_RTF_OK для определенного магазина не заданной, клиент с версиями RTF должен сам вызывать функцию [RTFSync,](rtfsync.md) чтобы синхронизировать версии **PR_BODY** и **PR_RTF_COMPRESSED** для текстового содержимого.</span><span class="sxs-lookup"><span data-stu-id="75332-172">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="75332-173">RTF всегда хранится в **PR_RTF_COMPRESSED** независимо от того, сжат ли он на самом деле.</span><span class="sxs-lookup"><span data-stu-id="75332-173">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="75332-174">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="75332-174">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="75332-175">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="75332-175">Header files</span></span>

<span data-ttu-id="75332-176">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75332-176">Mapidefs.h</span></span>
  
> <span data-ttu-id="75332-177">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="75332-177">Provides data type definitions.</span></span>
    
<span data-ttu-id="75332-178">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="75332-178">Mapitags.h</span></span>
  
> <span data-ttu-id="75332-179">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="75332-179">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75332-180">См. также</span><span class="sxs-lookup"><span data-stu-id="75332-180">See also</span></span>



[<span data-ttu-id="75332-181">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="75332-181">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75332-182">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="75332-182">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75332-183">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="75332-183">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75332-184">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="75332-184">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

