---
title: Каноническое свойство PidTagStoreSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreSupportMask
api_type:
- COM
ms.assetid: ada5694a-b5b1-471f-be33-906fc052681a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 143e7f0d2cd89cd4e7956cdda05d1bd512db4027
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392335"
---
# <a name="pidtagstoresupportmask-canonical-property"></a><span data-ttu-id="d783f-103">Каноническое свойство PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="d783f-103">PidTagStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="d783f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d783f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d783f-105">Содержит битовую маску флагов запроса клиентских приложений для определения характеристик хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="d783f-105">Contains a bitmask of flags that client applications query to determine the characteristics of a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d783f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d783f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d783f-107">PR_STORE_SUPPORT_MASK</span><span class="sxs-lookup"><span data-stu-id="d783f-107">PR_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="d783f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d783f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d783f-109">0x340D</span><span class="sxs-lookup"><span data-stu-id="d783f-109">0x340D</span></span>  <br/> |
|<span data-ttu-id="d783f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d783f-110">Data type:</span></span>  <br/> |<span data-ttu-id="d783f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d783f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d783f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d783f-112">Area:</span></span>  <br/> |<span data-ttu-id="d783f-113">Разное</span><span class="sxs-lookup"><span data-stu-id="d783f-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d783f-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d783f-114">Remarks</span></span>

<span data-ttu-id="d783f-115">Это свойство, включающие описание возможностей хранилища сообщений на клиентские приложения, которые планируют отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="d783f-115">This property discloses the capabilities of a message store to client applications that are planning to send it a message.</span></span> <span data-ttu-id="d783f-116">Флаги может поддерживать решения с клиента или другого хранилища, например необходимость отправки **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) или только **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d783f-116">The flags can support decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="d783f-117">Клиент никогда не следует устанавливать **PR_STORE_SUPPORT_MASK**; При попытке установить этот флаг возвращает MAPI_E_COMPUTED.</span><span class="sxs-lookup"><span data-stu-id="d783f-117">A client should never set **PR_STORE_SUPPORT_MASK**; an attempt to set this flag returns MAPI_E_COMPUTED.</span></span> 
  
<span data-ttu-id="d783f-118">Один или несколько из следующих флагов можно задать для битовой маски **PR_STORE_SUPPORT_MASK** :</span><span class="sxs-lookup"><span data-stu-id="d783f-118">One or more of the following flags can be set for the **PR_STORE_SUPPORT_MASK** bitmask:</span></span> 
  
<span data-ttu-id="d783f-119">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="d783f-119">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="d783f-120">(131072, 0x00020000) Хранилище сообщений поддерживает свойства, которые содержат символов ANSI (8 бит).</span><span class="sxs-lookup"><span data-stu-id="d783f-120">(131072, 0x00020000) The message store supports properties that contain ANSI (8-bit) characters.</span></span>
    
<span data-ttu-id="d783f-121">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="d783f-121">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="d783f-122">(32, 0x00000020) Хранилище сообщений поддерживает (OLE или не OLE) вложений в сообщения.</span><span class="sxs-lookup"><span data-stu-id="d783f-122">(32, 0x00000020) The message store supports attachments (OLE or non-OLE) to messages.</span></span> 
    
<span data-ttu-id="d783f-123">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="d783f-123">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="d783f-124">(1024, 0x00000400) Хранилище сообщений поддерживает по категориям представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="d783f-124">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="d783f-125">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="d783f-125">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="d783f-126">(16, 0x00000010) Хранилище сообщений поддерживает создание новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="d783f-126">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="d783f-127">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="d783f-127">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="d783f-128">(1, 0x00000001) Идентификаторы записей для объектов в хранилище сообщений являются уникальными, то есть, никогда не повторно использовать на протяжении хранилища.</span><span class="sxs-lookup"><span data-stu-id="d783f-128">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="d783f-129">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="d783f-129">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="d783f-130">(65536, 0x00010000) Хранилище сообщений поддерживает HTML-сообщений, хранящиеся в свойстве **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d783f-130">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="d783f-131">Если в среде разработки используются MAPIDEFS. H файл, который не включает STORE_HTML_OK, используйте значение 0x00010000.</span><span class="sxs-lookup"><span data-stu-id="d783f-131">If your development environment uses a MAPIDEFS.H file that does not include STORE_HTML_OK, use the value 0x00010000 instead.</span></span> 
    
<span data-ttu-id="d783f-132">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="d783f-132">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="d783f-133">(2097152, 0x00200000) В оболочке хранилище PST-файлов указывает, что при поступлении нового сообщения в хранилище, хранилище выполняет правил и фильтров нежелательной почты отдельно обработки в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="d783f-133">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store performs rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="d783f-134">Хранилище вызовы [IMAPISupport::Notify](imapisupport-notify.md)параметр **fnevNewMail** в структуре [УВЕДОМЛЕНИЙ](notification.md) , который передается как параметр, а затем передает сведения о новых сообщений для прослушивания клиента.</span><span class="sxs-lookup"><span data-stu-id="d783f-134">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="d783f-135">Следовательно когда прослушивания клиент получает уведомление, не будет обрабатывать правил для сообщения.</span><span class="sxs-lookup"><span data-stu-id="d783f-135">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="d783f-136">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="d783f-136">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="d783f-137">(524288, 0x00080000) Этот флаг зарезервирован и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="d783f-137">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="d783f-138">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="d783f-138">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="d783f-139">(8, 0x00000008) Хранилище сообщений поддерживает изменения существующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="d783f-139">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="d783f-140">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="d783f-140">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="d783f-141">(512, 0x00000200) Хранилище сообщений поддерживает многозначные свойства, гарантирует стабильность значение заказ в свойством во всем сохранения операции и поддерживает создание многозначных свойств в таблицах.</span><span class="sxs-lookup"><span data-stu-id="d783f-141">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="d783f-142">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="d783f-142">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="d783f-143">(256, 0x00000100) Хранилище сообщений поддерживает уведомления.</span><span class="sxs-lookup"><span data-stu-id="d783f-143">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="d783f-144">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="d783f-144">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="d783f-145">(64, 0x00000040) Хранилище сообщений поддерживает вложения OLE.</span><span class="sxs-lookup"><span data-stu-id="d783f-145">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="d783f-146">Данные OLE может осуществляться через интерфейс **IStorage** , например, который доступен через свойство **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d783f-146">The OLE data can be accessed through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="d783f-147">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="d783f-147">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="d783f-148">(16384, 0x00004000) Папки в этом хранилище — общедоступный (многопользовательский) не закрытый (возможно нескольких экземпляров, но не нескольких пользователей).</span><span class="sxs-lookup"><span data-stu-id="d783f-148">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="d783f-149">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="d783f-149">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="d783f-150">(8388608, 0x00800000) Обработчик протокола MAPI не будет выполнять обход контента хранилище и хранилище несет ответственность за передача все изменения через уведомления для компонента индексирования индексируются сообщений.</span><span class="sxs-lookup"><span data-stu-id="d783f-150">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible for pushing any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="d783f-151">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="d783f-151">STORE_READONLY</span></span> 
  
> <span data-ttu-id="d783f-152">(2, 0x00000002) Все интерфейсы для хранилища сообщений с уровнем доступа только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d783f-152">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="d783f-153">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="d783f-153">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="d783f-154">(4096, 0x00001000) Хранилище сообщений поддерживает ограничения.</span><span class="sxs-lookup"><span data-stu-id="d783f-154">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="d783f-155">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="d783f-155">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="d783f-156">(2048, 0x00000800) Хранилище сообщений поддерживает форматированный текст (RTF) сообщения, обычно сжатием и само хранилище отслеживает **PR_BODY** и **PR_RTF_COMPRESSED** синхронизации.</span><span class="sxs-lookup"><span data-stu-id="d783f-156">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="d783f-157">STORE_RULES_OK</span><span class="sxs-lookup"><span data-stu-id="d783f-157">STORE_RULES_OK</span></span>
  
> <span data-ttu-id="d783f-158">(268435456, 0x10000000) Указывает, что правила должны храниться в PST-хранилище даже в том случае, если это не хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d783f-158">(268435456, 0x10000000) Indicates that rules should be stored in this PST store even if it is not the default store.</span></span> <span data-ttu-id="d783f-159">При использовании в сочетании с **NON_EMS_XP_SAVE** **STORE_RULES_OK** правил, могут работать на хранилищ PST-файлов в оболочку не по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d783f-159">When **STORE_RULES_OK** is used in conjunction with **NON_EMS_XP_SAVE**, rules are able to run on non-default PST wrapped stores.</span></span>
    
<span data-ttu-id="d783f-160">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="d783f-160">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="d783f-161">(4, 0x00000004) Хранилище сообщений поддерживает папки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="d783f-161">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="d783f-162">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="d783f-162">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="d783f-163">(8192, 0x00002000) Хранилище сообщений поддерживает сортировки представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="d783f-163">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="d783f-164">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="d783f-164">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="d783f-165">(128, 0x00000080) Хранилище сообщений поддерживает пометки сообщения для отправки.</span><span class="sxs-lookup"><span data-stu-id="d783f-165">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="d783f-166">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="d783f-166">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="d783f-167">(32768, 0x00008000) Хранилище сообщений поддерживает хранение сообщения в формате RTF в несжатую форму.</span><span class="sxs-lookup"><span data-stu-id="d783f-167">(32768, 0x00008000) The message store supports storage of RTF messages in uncompressed form.</span></span> <span data-ttu-id="d783f-168">Поток несжатую RTF определяется значение **dwMagicUncompressedRTF** в заголовке потока.</span><span class="sxs-lookup"><span data-stu-id="d783f-168">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="d783f-169">Значение **dwMagicUncompressedRTF** определен в RTFLIB. H-файл.</span><span class="sxs-lookup"><span data-stu-id="d783f-169">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="d783f-170">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="d783f-170">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="d783f-171">(262144, 0x00040000) Указывает, что хранилище сообщений поддерживает Юникод хранилища.</span><span class="sxs-lookup"><span data-stu-id="d783f-171">(262144, 0x00040000) Indicates that the message store supports Unicode storage.</span></span> <span data-ttu-id="d783f-172">Клиент может выполнять на наличие флагом, чтобы решить, следует ли для запроса или сохранения данных Юникод в хранилище.</span><span class="sxs-lookup"><span data-stu-id="d783f-172">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span> 
    
<span data-ttu-id="d783f-173">Более RTF версии сообщения могут всегда храниться, даже в том случае, если хранилище сообщений не поддерживающими формат RTF.</span><span class="sxs-lookup"><span data-stu-id="d783f-173">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="d783f-174">Если бит STORE_RTF_OK не установлен для конкретного хранилища, обслуживание RTF версий клиента самого вызовите функцию [RTFSync](rtfsync.md) сохранение версий **PR_BODY** и **PR_RTF_COMPRESSED** , синхронизированы для текстовое содержимое.</span><span class="sxs-lookup"><span data-stu-id="d783f-174">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="d783f-175">Формат RTF всегда сохраняется в **PR_RTF_COMPRESSED**ли фактически сжимается или нет.</span><span class="sxs-lookup"><span data-stu-id="d783f-175">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d783f-176">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d783f-176">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d783f-177">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d783f-177">Protocol specifications</span></span>

<span data-ttu-id="d783f-178">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d783f-178">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d783f-179">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d783f-179">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d783f-180">[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d783f-180">[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d783f-181">Описывает формат сообщений, используемые для отправки сведения, относящиеся к общим папкам на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="d783f-181">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d783f-182">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d783f-182">Header files</span></span>

<span data-ttu-id="d783f-183">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d783f-183">Mapidefs.h</span></span>
  
> <span data-ttu-id="d783f-184">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d783f-184">Provides data type definitions.</span></span>
    
<span data-ttu-id="d783f-185">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d783f-185">Mapitags.h</span></span>
  
> <span data-ttu-id="d783f-186">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="d783f-186">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d783f-187">См. также</span><span class="sxs-lookup"><span data-stu-id="d783f-187">See also</span></span>



[<span data-ttu-id="d783f-188">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d783f-188">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d783f-189">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d783f-189">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d783f-190">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d783f-190">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d783f-191">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d783f-191">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

