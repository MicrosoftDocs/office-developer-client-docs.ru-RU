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
ms.openlocfilehash: 010b17de08ee5836a26c56f300b36822df2e981e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811977"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a><span data-ttu-id="b8d89-103">Каноническое свойство PidTagStoreUnicodeMask</span><span class="sxs-lookup"><span data-stu-id="b8d89-103">PidTagStoreUnicodeMask Canonical Property</span></span>

  
  
<span data-ttu-id="b8d89-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b8d89-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b8d89-105">Содержит битовую маску флагов, клиентские приложения необходимо запросить для определения характеристик хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="b8d89-105">Contains a bitmask of flags that client applications should query to determine the characteristics of a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b8d89-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b8d89-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b8d89-107">PR_STORE_UNICODE_MASK</span><span class="sxs-lookup"><span data-stu-id="b8d89-107">PR_STORE_UNICODE_MASK</span></span>  <br/> |
|<span data-ttu-id="b8d89-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b8d89-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b8d89-109">0x340F</span><span class="sxs-lookup"><span data-stu-id="b8d89-109">0x340F</span></span>  <br/> |
|<span data-ttu-id="b8d89-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b8d89-110">Data type:</span></span>  <br/> |<span data-ttu-id="b8d89-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b8d89-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b8d89-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b8d89-112">Area:</span></span>  <br/> |<span data-ttu-id="b8d89-113">Хранение сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="b8d89-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8d89-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b8d89-114">Remarks</span></span>

<span data-ttu-id="b8d89-115">Это свойство, включающие описание возможностей хранилища сообщений на клиентские приложения планирования отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="b8d89-115">This property discloses the capabilities of a message store to client applications planning to send it a message.</span></span> <span data-ttu-id="b8d89-116">Флаги могут быть упрощены решения с клиента или другого хранилища, например необходимость отправки **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) или только **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b8d89-116">The flags can facilitate decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="b8d89-117">Клиент никогда не следует устанавливать это свойство.</span><span class="sxs-lookup"><span data-stu-id="b8d89-117">A client should never set this property.</span></span> <span data-ttu-id="b8d89-118">Попытка возвращает **MAPI_E_COMPUTED**.</span><span class="sxs-lookup"><span data-stu-id="b8d89-118">An attempt returns **MAPI_E_COMPUTED**.</span></span> 
  
<span data-ttu-id="b8d89-119">Для этого свойства может быть установлено одно или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="b8d89-119">One or more of the following flags can be set for this property:</span></span> 
  
<span data-ttu-id="b8d89-120">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="b8d89-120">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="b8d89-121">(131072, 0x00020000) Хранилище сообщений поддерживает свойства символами (8 бит) American National стандартов института (ANSI).</span><span class="sxs-lookup"><span data-stu-id="b8d89-121">(131072, 0x00020000) The message store supports properties that contain American National Standards Institute (ANSI) (8-bit) characters.</span></span>
    
<span data-ttu-id="b8d89-122">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="b8d89-122">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="b8d89-123">(32, 0x00000020) Хранилище сообщений поддерживает Object Linking и внедрения (OLE) или не OLE вложений в сообщения.</span><span class="sxs-lookup"><span data-stu-id="b8d89-123">(32, 0x00000020) The message store supports Object Linking and Embedding (OLE) or non-OLE attachments to messages.</span></span> 
    
<span data-ttu-id="b8d89-124">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="b8d89-124">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="b8d89-125">(1024, 0x00000400) Хранилище сообщений поддерживает по категориям представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="b8d89-125">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="b8d89-126">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="b8d89-126">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="b8d89-127">(16, 0x00000010) Хранилище сообщений поддерживает создание новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="b8d89-127">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="b8d89-128">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="b8d89-128">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="b8d89-129">(1, 0x00000001) Идентификаторы записей для объектов в хранилище сообщений являются уникальными, то есть, никогда не повторно использовать на протяжении хранилища.</span><span class="sxs-lookup"><span data-stu-id="b8d89-129">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="b8d89-130">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="b8d89-130">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="b8d89-131">(65536, 0x00010000) Хранилище сообщений поддерживает HTML-сообщений, хранящиеся в свойстве **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b8d89-131">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="b8d89-132">Обратите внимание на то, что **STORE_HTML_OK** не определен в версиях MAPIDEFS. H, которые включены в Microsoft Exchange 2000 Server и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="b8d89-132">Note that **STORE_HTML_OK** is not defined in versions of MAPIDEFS.H that are included with Microsoft Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="b8d89-133">Если в среде разработки используются MAPIDEFS. H-файл, не включают **STORE_HTML_OK**, вместо этого используйте значение «0x00010000».</span><span class="sxs-lookup"><span data-stu-id="b8d89-133">If your development environment uses a MAPIDEFS.H file that does not include **STORE_HTML_OK**, use the value "0x00010000" instead.</span></span> 
    
<span data-ttu-id="b8d89-134">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="b8d89-134">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="b8d89-135">(2097152, 0x00200000) В банке оболочку PST-файлов указывает, что при поступлении нового сообщения в хранилище, store работает правил и нежелательной почты фильтрации отдельно обработки в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="b8d89-135">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store does rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="b8d89-136">Хранилище вызовы [IMAPISupport::Notify](imapisupport-notify.md)параметр **fnevNewMail** в структуре [УВЕДОМЛЕНИЙ](notification.md) , который передается как параметр, а затем передает сведения о новых сообщений для прослушивания клиента.</span><span class="sxs-lookup"><span data-stu-id="b8d89-136">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="b8d89-137">Следовательно когда прослушивания клиент получает уведомление, не будет обрабатывать правил для сообщения.</span><span class="sxs-lookup"><span data-stu-id="b8d89-137">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="b8d89-138">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="b8d89-138">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="b8d89-139">(524288, 0x00080000) Этот флаг зарезервирован и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="b8d89-139">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="b8d89-140">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="b8d89-140">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="b8d89-141">(8, 0x00000008) Хранилище сообщений поддерживает изменения существующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="b8d89-141">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="b8d89-142">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="b8d89-142">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="b8d89-143">(512, 0x00000200) Хранилище сообщений поддерживает многозначные свойства, гарантирует стабильность значение заказ в свойством во всем сохранения операции и поддерживает создание многозначных свойств в таблицах.</span><span class="sxs-lookup"><span data-stu-id="b8d89-143">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="b8d89-144">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="b8d89-144">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="b8d89-145">(256, 0x00000100) Хранилище сообщений поддерживает уведомления.</span><span class="sxs-lookup"><span data-stu-id="b8d89-145">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="b8d89-146">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="b8d89-146">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="b8d89-147">(64, 0x00000040) Хранилище сообщений поддерживает вложения OLE.</span><span class="sxs-lookup"><span data-stu-id="b8d89-147">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="b8d89-148">Данные OLE доступен через интерфейс **IStorage** , например, то доступен через свойство **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b8d89-148">The OLE data is accessible through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="b8d89-149">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="b8d89-149">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="b8d89-150">(16384, 0x00004000) Папки в этом хранилище — общедоступный (многопользовательский) не закрытый (возможно нескольких экземпляров, но не нескольких пользователей).</span><span class="sxs-lookup"><span data-stu-id="b8d89-150">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="b8d89-151">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="b8d89-151">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="b8d89-152">(8388608, 0x00800000) Обработчик протокола MAPI не будет выполнять обход контента хранилище и хранилище отвечает отказываться все изменения через уведомления для компонента индексирования индексируются сообщений.</span><span class="sxs-lookup"><span data-stu-id="b8d89-152">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="b8d89-153">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="b8d89-153">STORE_READONLY</span></span> 
  
> <span data-ttu-id="b8d89-154">(2, 0x00000002) Все интерфейсы для хранилища сообщений с уровнем доступа только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b8d89-154">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="b8d89-155">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="b8d89-155">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="b8d89-156">(4096, 0x00001000) Хранилище сообщений поддерживает ограничения.</span><span class="sxs-lookup"><span data-stu-id="b8d89-156">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="b8d89-157">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="b8d89-157">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="b8d89-158">(2048, 0x00000800) Хранилище сообщений поддерживает форматированный текст (RTF) сообщения, обычно сжатием и само хранилище отслеживает **PR_BODY** и **PR_RTF_COMPRESSED** синхронизации.</span><span class="sxs-lookup"><span data-stu-id="b8d89-158">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="b8d89-159">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="b8d89-159">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="b8d89-160">(4, 0x00000004) Хранилище сообщений поддерживает папки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="b8d89-160">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="b8d89-161">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="b8d89-161">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="b8d89-162">(8192, 0x00002000) Хранилище сообщений поддерживает сортировки представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="b8d89-162">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="b8d89-163">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="b8d89-163">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="b8d89-164">(128, 0x00000080) Хранилище сообщений поддерживает пометки сообщения для отправки.</span><span class="sxs-lookup"><span data-stu-id="b8d89-164">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="b8d89-165">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="b8d89-165">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="b8d89-166">(32768, 0x00008000) Хранилище сообщений поддерживает хранение сообщений текста (RTF) revisable формы в несжатую форму.</span><span class="sxs-lookup"><span data-stu-id="b8d89-166">(32768, 0x00008000) The message store supports storage of revisable form text (RTF) messages in uncompressed form.</span></span> <span data-ttu-id="b8d89-167">Поток несжатую RTF определяется значение **dwMagicUncompressedRTF** в заголовке потока.</span><span class="sxs-lookup"><span data-stu-id="b8d89-167">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="b8d89-168">Значение **dwMagicUncompressedRTF** определен в RTFLIB. H-файл.</span><span class="sxs-lookup"><span data-stu-id="b8d89-168">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="b8d89-169">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="b8d89-169">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="b8d89-170">(262144, 0x00040000) Хранилище сообщений поддерживает свойства, содержащее знаки Юникода.</span><span class="sxs-lookup"><span data-stu-id="b8d89-170">(262144, 0x00040000) The message store supports properties containing Unicode characters.</span></span>
    
<span data-ttu-id="b8d89-171">Более RTF версии сообщения могут всегда храниться, даже в том случае, если хранилище сообщений не поддерживающими формат RTF.</span><span class="sxs-lookup"><span data-stu-id="b8d89-171">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="b8d89-172">Если бит STORE_RTF_OK не установлен для конкретного хранилища, обслуживание RTF версий клиента самого вызовите функцию [RTFSync](rtfsync.md) сохранение версий **PR_BODY** и **PR_RTF_COMPRESSED** , синхронизированы для текстовое содержимое.</span><span class="sxs-lookup"><span data-stu-id="b8d89-172">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="b8d89-173">Формат RTF всегда сохраняется в **PR_RTF_COMPRESSED**ли фактически сжимается или нет.</span><span class="sxs-lookup"><span data-stu-id="b8d89-173">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b8d89-174">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b8d89-174">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b8d89-175">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b8d89-175">Header files</span></span>

<span data-ttu-id="b8d89-176">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b8d89-176">Mapidefs.h</span></span>
  
> <span data-ttu-id="b8d89-177">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b8d89-177">Provides data type definitions.</span></span>
    
<span data-ttu-id="b8d89-178">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b8d89-178">Mapitags.h</span></span>
  
> <span data-ttu-id="b8d89-179">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="b8d89-179">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b8d89-180">См. также</span><span class="sxs-lookup"><span data-stu-id="b8d89-180">See also</span></span>



[<span data-ttu-id="b8d89-181">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b8d89-181">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b8d89-182">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b8d89-182">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b8d89-183">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b8d89-183">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b8d89-184">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b8d89-184">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

