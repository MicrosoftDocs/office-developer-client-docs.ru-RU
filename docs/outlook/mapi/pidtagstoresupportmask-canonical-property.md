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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340973"
---
# <a name="pidtagstoresupportmask-canonical-property"></a><span data-ttu-id="63d92-103">Каноническое свойство PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="63d92-103">PidTagStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="63d92-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63d92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63d92-105">Содержит битовуюmass флагов, которые клиентские приложения запрашивают для определения характеристик хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="63d92-105">Contains a bitmask of flags that client applications query to determine the characteristics of a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="63d92-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="63d92-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="63d92-107">PR_STORE_SUPPORT_MASK</span><span class="sxs-lookup"><span data-stu-id="63d92-107">PR_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="63d92-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="63d92-108">Identifier:</span></span>  <br/> |<span data-ttu-id="63d92-109">0x340D</span><span class="sxs-lookup"><span data-stu-id="63d92-109">0x340D</span></span>  <br/> |
|<span data-ttu-id="63d92-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="63d92-110">Data type:</span></span>  <br/> |<span data-ttu-id="63d92-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="63d92-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="63d92-112">Область:</span><span class="sxs-lookup"><span data-stu-id="63d92-112">Area:</span></span>  <br/> |<span data-ttu-id="63d92-113">Разное</span><span class="sxs-lookup"><span data-stu-id="63d92-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63d92-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="63d92-114">Remarks</span></span>

<span data-ttu-id="63d92-115">Это свойство раскрывает возможности хранения сообщений для клиентских приложений, которые планируют отправить ему сообщение.</span><span class="sxs-lookup"><span data-stu-id="63d92-115">This property discloses the capabilities of a message store to client applications that are planning to send it a message.</span></span> <span data-ttu-id="63d92-116">Флаги могут поддерживать решения клиента или другого магазина, такие как отправка PR_BODY **(** [PidTagBody)](pidtagbody-canonical-property.md)или только PR_RTF_COMPRESSED **(** [PidTagRtfCompressed).](pidtagrtfcompressed-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="63d92-116">The flags can support decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="63d92-117">Клиент никогда не должен **устанавливать** PR_STORE_SUPPORT_MASK; Попытка установить этот флаг возвращает MAPI_E_COMPUTED.</span><span class="sxs-lookup"><span data-stu-id="63d92-117">A client should never set **PR_STORE_SUPPORT_MASK**; an attempt to set this flag returns MAPI_E_COMPUTED.</span></span> 
  
<span data-ttu-id="63d92-118">Один или несколько из следующих флагов  можно установить для битовой PR_STORE_SUPPORT_MASK битов:</span><span class="sxs-lookup"><span data-stu-id="63d92-118">One or more of the following flags can be set for the **PR_STORE_SUPPORT_MASK** bitmask:</span></span> 
  
<span data-ttu-id="63d92-119">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="63d92-119">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="63d92-120">(131072, 0x00020000) Хранилище сообщений поддерживает свойства, содержащие символы ANSI (8-битные).</span><span class="sxs-lookup"><span data-stu-id="63d92-120">(131072, 0x00020000) The message store supports properties that contain ANSI (8-bit) characters.</span></span>
    
<span data-ttu-id="63d92-121">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="63d92-121">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="63d92-122">(32, 0x00000020) Хранилище сообщений поддерживает вложения (OLE или non-OLE) для сообщений.</span><span class="sxs-lookup"><span data-stu-id="63d92-122">(32, 0x00000020) The message store supports attachments (OLE or non-OLE) to messages.</span></span> 
    
<span data-ttu-id="63d92-123">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="63d92-123">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="63d92-124">(1024, 0x00000400) Хранилище сообщений поддерживает классификацию представлений таблиц.</span><span class="sxs-lookup"><span data-stu-id="63d92-124">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="63d92-125">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="63d92-125">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="63d92-126">(16, 0x00000010) Хранилище сообщений поддерживает создание новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="63d92-126">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="63d92-127">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="63d92-127">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="63d92-128">(1, 0x00000001) Идентификаторы записей для объектов в хранилище сообщений уникальны, то есть никогда не повторно в течение всего жизненного года хранения.</span><span class="sxs-lookup"><span data-stu-id="63d92-128">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="63d92-129">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="63d92-129">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="63d92-130">(65536, 0x00010000) Хранилище сообщений поддерживает HTML-сообщения, хранимые в свойстве **PR_BODY_HTML** ([PidTagBodyHtml).](pidtagbodyhtml-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="63d92-130">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="63d92-131">Если в среде разработки используется MAPIDEFS. H-файл, который не включает STORE_HTML_OK, используйте значение 0x00010000.</span><span class="sxs-lookup"><span data-stu-id="63d92-131">If your development environment uses a MAPIDEFS.H file that does not include STORE_HTML_OK, use the value 0x00010000 instead.</span></span> 
    
<span data-ttu-id="63d92-132">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="63d92-132">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="63d92-133">(2097152, 0x00200000) В упакованном хранилище PST-данных указывает, что когда новое сообщение поступает в магазин, хранилище выполняет правила и обработку фильтра нежелательной почты отдельно для сообщения.</span><span class="sxs-lookup"><span data-stu-id="63d92-133">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store performs rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="63d92-134">Магазин вызывает [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** в структуре [NOTIFICATION,](notification.md) которая передается в качестве параметра, а затем передает сведения о новом сообщении клиенту прослушивания.</span><span class="sxs-lookup"><span data-stu-id="63d92-134">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="63d92-135">Впоследствии, когда прослушивающий клиент получает уведомление, к сообщению не применяются правила.</span><span class="sxs-lookup"><span data-stu-id="63d92-135">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="63d92-136">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="63d92-136">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="63d92-137">(524288, 0x00080000) Этот флаг зарезервирован и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="63d92-137">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="63d92-138">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="63d92-138">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="63d92-139">(8, 0x00000008) Хранилище сообщений поддерживает изменение существующих сообщений.</span><span class="sxs-lookup"><span data-stu-id="63d92-139">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="63d92-140">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="63d92-140">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="63d92-141">(512, 0x00000200) Хранилище сообщений поддерживает многооценные свойства, гарантирует стабильность порядка значений в многоценном свойстве в ходе операции сохранения и поддерживает возможность искомости многоценных свойств в таблицах.</span><span class="sxs-lookup"><span data-stu-id="63d92-141">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="63d92-142">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="63d92-142">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="63d92-143">(256, 0x00000100) Хранилище сообщений поддерживает уведомления.</span><span class="sxs-lookup"><span data-stu-id="63d92-143">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="63d92-144">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="63d92-144">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="63d92-145">(64, 0x00000040) Хранилище сообщений поддерживает вложения OLE.</span><span class="sxs-lookup"><span data-stu-id="63d92-145">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="63d92-146">Доступ к данным OLE можно получить через **интерфейс IStorage,** например через **свойство PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject).](pidtagattachdataobject-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="63d92-146">The OLE data can be accessed through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="63d92-147">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="63d92-147">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="63d92-148">(16384, 0x00004000) Папки в этом хранилище являются общедоступными (несколькими пользователями), а не частными (возможно, с несколькими экземплярами, но не с несколькими пользователями).</span><span class="sxs-lookup"><span data-stu-id="63d92-148">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="63d92-149">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="63d92-149">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="63d92-150">(8388608, 0x00800000) Обработщик протокола MAPI не будет обходить хранилище, и хранилище будет отвечать за то, чтобы индексировать сообщения с помощью уведомлений.</span><span class="sxs-lookup"><span data-stu-id="63d92-150">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible for pushing any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="63d92-151">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="63d92-151">STORE_READONLY</span></span> 
  
> <span data-ttu-id="63d92-152">(2, 0x00000002) Все интерфейсы для хранения сообщений имеют доступ только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63d92-152">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="63d92-153">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="63d92-153">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="63d92-154">(4096, 0x00001000) Хранилище сообщений поддерживает ограничения.</span><span class="sxs-lookup"><span data-stu-id="63d92-154">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="63d92-155">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="63d92-155">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="63d92-156">(2048, 0x00000800) Хранилище сообщений поддерживает сообщения в формате RTF (обычно сжатые),  а само хранилище сохраняет PR_BODY и **PR_RTF_COMPRESSED** синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="63d92-156">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="63d92-157">STORE_RULES_OK</span><span class="sxs-lookup"><span data-stu-id="63d92-157">STORE_RULES_OK</span></span>
  
> <span data-ttu-id="63d92-158">(268435456, 0x10000000) Указывает, что правила должны храниться в этом PST-хранилище, даже если оно не является хранилищем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="63d92-158">(268435456, 0x10000000) Indicates that rules should be stored in this PST store even if it is not the default store.</span></span> <span data-ttu-id="63d92-159">Если **STORE_RULES_OK** в сочетании с **NON_EMS_XP_SAVE,** правила могут запускаться в хранилищах, не используемых по умолчанию в PST-оболочке.</span><span class="sxs-lookup"><span data-stu-id="63d92-159">When **STORE_RULES_OK** is used in conjunction with **NON_EMS_XP_SAVE**, rules are able to run on non-default PST wrapped stores.</span></span>
    
<span data-ttu-id="63d92-160">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="63d92-160">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="63d92-161">(4, 0x00000004) Хранилище сообщений поддерживает папки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="63d92-161">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="63d92-162">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="63d92-162">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="63d92-163">(8192, 0x00002000) Хранилище сообщений поддерживает сортировку представлений таблиц.</span><span class="sxs-lookup"><span data-stu-id="63d92-163">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="63d92-164">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="63d92-164">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="63d92-165">(128, 0x00000080) Хранилище сообщений поддерживает пометку сообщения для отправки.</span><span class="sxs-lookup"><span data-stu-id="63d92-165">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="63d92-166">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="63d92-166">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="63d92-167">(32768, 0x00008000) Хранилище сообщений поддерживает хранение сообщений RTF в несмеченной форме.</span><span class="sxs-lookup"><span data-stu-id="63d92-167">(32768, 0x00008000) The message store supports storage of RTF messages in uncompressed form.</span></span> <span data-ttu-id="63d92-168">Несхваченный поток RTF идентифицирован значением **dwMagicUncompressedRTF** в загоне потока.</span><span class="sxs-lookup"><span data-stu-id="63d92-168">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="63d92-169">Значение **dwMagicUncompressedRTF** определяется в RTFLIB. H-файл.</span><span class="sxs-lookup"><span data-stu-id="63d92-169">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="63d92-170">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="63d92-170">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="63d92-171">(262144, 0x00040000) Указывает, что хранилище сообщений поддерживает хранилище Юникод.</span><span class="sxs-lookup"><span data-stu-id="63d92-171">(262144, 0x00040000) Indicates that the message store supports Unicode storage.</span></span> <span data-ttu-id="63d92-172">Клиент можно проверить наличие флага, чтобы принять решение о запросе или сохранении сведений Юникода в хранилище.</span><span class="sxs-lookup"><span data-stu-id="63d92-172">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span> 
    
<span data-ttu-id="63d92-173">Версию сообщения в RTF всегда можно сохранить, даже если хранилище сообщений не имеет RTF-данных.</span><span class="sxs-lookup"><span data-stu-id="63d92-173">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="63d92-174">Если STORE_RTF_OK для определенного магазина не заданной, клиент с версиями RTF должен сам вызывать функцию [RTFSync,](rtfsync.md) чтобы синхронизировать версии **PR_BODY** и **PR_RTF_COMPRESSED** для текстового содержимого.</span><span class="sxs-lookup"><span data-stu-id="63d92-174">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="63d92-175">RTF всегда хранится в **PR_RTF_COMPRESSED** независимо от того, сжат ли он на самом деле.</span><span class="sxs-lookup"><span data-stu-id="63d92-175">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="63d92-176">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="63d92-176">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="63d92-177">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="63d92-177">Protocol specifications</span></span>

<span data-ttu-id="63d92-178">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63d92-178">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63d92-179">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="63d92-179">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="63d92-180">[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63d92-180">[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63d92-181">Описывает формат сообщений, используемых для отправки сведений, связанных с папками общего доступа на клиенте.</span><span class="sxs-lookup"><span data-stu-id="63d92-181">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="63d92-182">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="63d92-182">Header files</span></span>

<span data-ttu-id="63d92-183">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="63d92-183">Mapidefs.h</span></span>
  
> <span data-ttu-id="63d92-184">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="63d92-184">Provides data type definitions.</span></span>
    
<span data-ttu-id="63d92-185">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="63d92-185">Mapitags.h</span></span>
  
> <span data-ttu-id="63d92-186">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="63d92-186">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63d92-187">См. также</span><span class="sxs-lookup"><span data-stu-id="63d92-187">See also</span></span>



[<span data-ttu-id="63d92-188">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="63d92-188">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63d92-189">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="63d92-189">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63d92-190">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="63d92-190">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63d92-191">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="63d92-191">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

