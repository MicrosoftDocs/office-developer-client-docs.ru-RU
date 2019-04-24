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
# <a name="pidtagstoresupportmask-canonical-property"></a><span data-ttu-id="312f5-103">Каноническое свойство PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="312f5-103">PidTagStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="312f5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="312f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="312f5-105">Содержит битовую маску для флагов, которые запрос клиентского приложения определяет характеристики хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="312f5-105">Contains a bitmask of flags that client applications query to determine the characteristics of a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="312f5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="312f5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="312f5-107">ПР_СТОРЕ_СУППОРТ_МАСК</span><span class="sxs-lookup"><span data-stu-id="312f5-107">PR_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="312f5-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="312f5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="312f5-109">0x340D</span><span class="sxs-lookup"><span data-stu-id="312f5-109">0x340D</span></span>  <br/> |
|<span data-ttu-id="312f5-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="312f5-110">Data type:</span></span>  <br/> |<span data-ttu-id="312f5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="312f5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="312f5-112">Область:</span><span class="sxs-lookup"><span data-stu-id="312f5-112">Area:</span></span>  <br/> |<span data-ttu-id="312f5-113">Разное</span><span class="sxs-lookup"><span data-stu-id="312f5-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="312f5-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="312f5-114">Remarks</span></span>

<span data-ttu-id="312f5-115">Это свойство раскрывает возможности хранилища сообщений клиентским приложениям, которые планирует отправить ему сообщение.</span><span class="sxs-lookup"><span data-stu-id="312f5-115">This property discloses the capabilities of a message store to client applications that are planning to send it a message.</span></span> <span data-ttu-id="312f5-116">Флаги могут поддерживать решения, принимаемые клиентом или другим хранилищем, например, следует ли отправлять **пр_боди** ([PidTagBody](pidtagbody-canonical-property.md)) или только **пр_ртф_компрессед** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="312f5-116">The flags can support decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="312f5-117">Клиент не должен задавать **пр_сторе_суппорт_маск**; попытка установить этот флаг возвращает МАПИ_Е_КОМПУТЕД.</span><span class="sxs-lookup"><span data-stu-id="312f5-117">A client should never set **PR_STORE_SUPPORT_MASK**; an attempt to set this flag returns MAPI_E_COMPUTED.</span></span> 
  
<span data-ttu-id="312f5-118">Для битовой маски **пр_сторе_суппорт_маск** можно задать один или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="312f5-118">One or more of the following flags can be set for the **PR_STORE_SUPPORT_MASK** bitmask:</span></span> 
  
<span data-ttu-id="312f5-119">СТОРЕ_АНСИ_ОК</span><span class="sxs-lookup"><span data-stu-id="312f5-119">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="312f5-120">(131072, 0x00020000) Хранилище сообщений поддерживает свойства, содержащие ANSI (8-разрядные) символы.</span><span class="sxs-lookup"><span data-stu-id="312f5-120">(131072, 0x00020000) The message store supports properties that contain ANSI (8-bit) characters.</span></span>
    
<span data-ttu-id="312f5-121">СТОРЕ_АТТАЧ_ОК</span><span class="sxs-lookup"><span data-stu-id="312f5-121">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="312f5-122">(32, 0x00000020) Хранилище сообщений поддерживает вложения (OLE или не OLE) для сообщений.</span><span class="sxs-lookup"><span data-stu-id="312f5-122">(32, 0x00000020) The message store supports attachments (OLE or non-OLE) to messages.</span></span> 
    
<span data-ttu-id="312f5-123">СТОРЕ_КАТЕГОРИЗЕ_ОК</span><span class="sxs-lookup"><span data-stu-id="312f5-123">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="312f5-124">(1024, 0x00000400) Хранилище сообщений поддерживает упорядоченные по категориям представления таблиц.</span><span class="sxs-lookup"><span data-stu-id="312f5-124">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="312f5-125">СТОРЕ_КРЕАТЕ_ОК</span><span class="sxs-lookup"><span data-stu-id="312f5-125">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="312f5-126">(16, 0x00000010) Хранилище сообщений поддерживает создание новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="312f5-126">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="312f5-127">СТОРЕ_ЕНТРИД_УНИКУЕ</span><span class="sxs-lookup"><span data-stu-id="312f5-127">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="312f5-128">(1, 0x00000001) Идентификаторы записей для объектов в хранилище сообщений уникальны, то есть которые никогда не используются в течение всего срока хранения.</span><span class="sxs-lookup"><span data-stu-id="312f5-128">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="312f5-129">СТОРЕ_ХТМЛ_ОК</span><span class="sxs-lookup"><span data-stu-id="312f5-129">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="312f5-130">(65536, 0x00010000) Хранилище сообщений поддерживает HTML-сообщения, хранящиеся в свойстве **пр_боди_хтмл** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="312f5-130">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="312f5-131">Если ваша среда разработки использует MAPIDEFS. H файл, который не включает СТОРЕ_ХТМЛ_ОК, используйте значение 0x00010000.</span><span class="sxs-lookup"><span data-stu-id="312f5-131">If your development environment uses a MAPIDEFS.H file that does not include STORE_HTML_OK, use the value 0x00010000 instead.</span></span> 
    
<span data-ttu-id="312f5-132">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="312f5-132">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="312f5-133">(2097152, 0x00200000) В упакованном PST-хранилище указывает на то, что при поступлении нового сообщения в хранилище хранилище выполняет правила и обработку фильтра нежелательной почты по отдельности.</span><span class="sxs-lookup"><span data-stu-id="312f5-133">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store performs rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="312f5-134">Store вызывает метод [имаписуппорт:: notify](imapisupport-notify.md), задавая **Фневневмаил** в структуре [уведомлений](notification.md) , передаваемой в качестве параметра, а затем передает сведения о новом сообщении клиенту прослушивания.</span><span class="sxs-lookup"><span data-stu-id="312f5-134">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="312f5-135">Впоследствии, когда прослушивающий клиент получает уведомление, к сообщению не применяются правила.</span><span class="sxs-lookup"><span data-stu-id="312f5-135">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="312f5-136">СТОРЕ_ЛОКАЛСТОРЕ</span><span class="sxs-lookup"><span data-stu-id="312f5-136">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="312f5-137">(524288, 0x00080000) Этот флаг зарезервирован и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="312f5-137">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="312f5-138">СТОРЕ_МОДИФИ_ОК</span><span class="sxs-lookup"><span data-stu-id="312f5-138">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="312f5-139">(8, 0x00000008) Хранилище сообщений поддерживает изменение существующих сообщений.</span><span class="sxs-lookup"><span data-stu-id="312f5-139">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="312f5-140">СТОРЕ_МВ_ПРОПС_ОК</span><span class="sxs-lookup"><span data-stu-id="312f5-140">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="312f5-141">(512, 0x00000200) Хранилище сообщений поддерживает многозначные свойства, гарантирует стабильность порядка значений в многозначном свойстве во время операции сохранения и поддерживает создание экземпляров многозначных свойств в таблицах.</span><span class="sxs-lookup"><span data-stu-id="312f5-141">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="312f5-142">СТОРЕ_НОТИФИ_ОК</span><span class="sxs-lookup"><span data-stu-id="312f5-142">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="312f5-143">(256, 0x00000100) Хранилище сообщений поддерживает уведомления.</span><span class="sxs-lookup"><span data-stu-id="312f5-143">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="312f5-144">СТОРЕ_ОЛЕ_ОК</span><span class="sxs-lookup"><span data-stu-id="312f5-144">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="312f5-145">(64, 0x00000040) Хранилище сообщений поддерживает вложения OLE.</span><span class="sxs-lookup"><span data-stu-id="312f5-145">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="312f5-146">Доступ к данным OLE можно получить с помощью интерфейса **IStorage** , например, доступного через свойство **пр_аттач_дата_обж** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="312f5-146">The OLE data can be accessed through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="312f5-147">СТОРЕ_ПУБЛИК_ФОЛДЕРС</span><span class="sxs-lookup"><span data-stu-id="312f5-147">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="312f5-148">(16384, 0x00004000) Папки в этом хранилище являются общедоступными (несколькими пользователями), а не частными (возможно, с несколькими экземплярами, но не с несколькими пользователями).</span><span class="sxs-lookup"><span data-stu-id="312f5-148">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="312f5-149">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="312f5-149">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="312f5-150">(8388608, 0x00800000) Обработчик протокола MAPI не выполняет обход хранилища, а хранилище отвечает за отправку любых изменений через уведомления индексатору, чтобы индексировать сообщения.</span><span class="sxs-lookup"><span data-stu-id="312f5-150">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible for pushing any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="312f5-151">СТОРЕ_РЕАДОНЛИ</span><span class="sxs-lookup"><span data-stu-id="312f5-151">STORE_READONLY</span></span> 
  
> <span data-ttu-id="312f5-152">(2, 0x00000002) Все интерфейсы для хранилища сообщений имеют уровень доступа только для чтения.</span><span class="sxs-lookup"><span data-stu-id="312f5-152">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="312f5-153">СТОРЕ_РЕСТРИКТИОН_ОК</span><span class="sxs-lookup"><span data-stu-id="312f5-153">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="312f5-154">(4096, 0x00001000) Хранилище сообщений поддерживает ограничения.</span><span class="sxs-lookup"><span data-stu-id="312f5-154">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="312f5-155">СТОРЕ_РТФ_ОК</span><span class="sxs-lookup"><span data-stu-id="312f5-155">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="312f5-156">(2048, 0x00000800) Хранилище сообщений поддерживает сообщения в формате RTF (RTF), обычно сжатые и хранящиеся в хранилище **пр_боди** и **пр_ртф_компрессед** .</span><span class="sxs-lookup"><span data-stu-id="312f5-156">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="312f5-157">СТОРЕ_РУЛЕС_ОК</span><span class="sxs-lookup"><span data-stu-id="312f5-157">STORE_RULES_OK</span></span>
  
> <span data-ttu-id="312f5-158">(268435456, 0x10000000) Указывает, что правила должны храниться в этом PST-хранилище, даже если оно не является хранилищем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="312f5-158">(268435456, 0x10000000) Indicates that rules should be stored in this PST store even if it is not the default store.</span></span> <span data-ttu-id="312f5-159">Если **сторе_рулес_ок** используется совместно с **нон_емс_ксп_саве**, то правила могут работать не по умолчанию с упакованными хранилищами PST.</span><span class="sxs-lookup"><span data-stu-id="312f5-159">When **STORE_RULES_OK** is used in conjunction with **NON_EMS_XP_SAVE**, rules are able to run on non-default PST wrapped stores.</span></span>
    
<span data-ttu-id="312f5-160">СТОРЕ_СЕАРЧ_ОК</span><span class="sxs-lookup"><span data-stu-id="312f5-160">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="312f5-161">(4, 0x00000004) Хранилище сообщений поддерживает папки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="312f5-161">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="312f5-162">СТОРЕ_СОРТ_ОК</span><span class="sxs-lookup"><span data-stu-id="312f5-162">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="312f5-163">(8192, 0x00002000) Хранилище сообщений поддерживает сортировку представлений таблиц.</span><span class="sxs-lookup"><span data-stu-id="312f5-163">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="312f5-164">СТОРЕ_СУБМИТ_ОК</span><span class="sxs-lookup"><span data-stu-id="312f5-164">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="312f5-165">(128, 0x00000080) Хранилище сообщений поддерживает пометку сообщения для отправки.</span><span class="sxs-lookup"><span data-stu-id="312f5-165">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="312f5-166">СТОРЕ_УНКОМПРЕССЕД_РТФ</span><span class="sxs-lookup"><span data-stu-id="312f5-166">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="312f5-167">(32768, 0x00008000) Хранилище сообщений поддерживает хранение RTF сообщений в несжатой форме.</span><span class="sxs-lookup"><span data-stu-id="312f5-167">(32768, 0x00008000) The message store supports storage of RTF messages in uncompressed form.</span></span> <span data-ttu-id="312f5-168">Несжатый поток RTF идентифицируется значением **двмагикункомпресседртф** в заголовке потока.</span><span class="sxs-lookup"><span data-stu-id="312f5-168">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="312f5-169">Значение **двмагикункомпресседртф** определено в ртфлиб. H файл.</span><span class="sxs-lookup"><span data-stu-id="312f5-169">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="312f5-170">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="312f5-170">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="312f5-171">(262144, 0x00040000) Указывает, что хранилище сообщений поддерживает Юникод.</span><span class="sxs-lookup"><span data-stu-id="312f5-171">(262144, 0x00040000) Indicates that the message store supports Unicode storage.</span></span> <span data-ttu-id="312f5-172">Клиент можно проверить наличие флага, чтобы принять решение о запросе или сохранении сведений Юникода в хранилище.</span><span class="sxs-lookup"><span data-stu-id="312f5-172">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span> 
    
<span data-ttu-id="312f5-173">Всегда можно сохранить RTF-версию сообщения, даже если хранилище сообщений не поддерживает RTF.</span><span class="sxs-lookup"><span data-stu-id="312f5-173">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="312f5-174">Если для конкретного хранилища не задан бит СТОРЕ_РТФ_ОК, клиент, поддерживающий версии RTF, должен вызвать функцию [ртфсинк](rtfsync.md) , чтобы синхронизировать версии **пр_боди** и **пр_ртф_компрессед** с текстовым содержимым.</span><span class="sxs-lookup"><span data-stu-id="312f5-174">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="312f5-175">RTF всегда хранится в **пр_ртф_компрессед**, независимо от того, является ли он фактически сжатым или нет.</span><span class="sxs-lookup"><span data-stu-id="312f5-175">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="312f5-176">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="312f5-176">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="312f5-177">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="312f5-177">Protocol specifications</span></span>

<span data-ttu-id="312f5-178">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="312f5-178">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="312f5-179">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="312f5-179">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="312f5-180">[[MS — ОКСМСГ]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="312f5-180">[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="312f5-181">Описывает формат сообщений, используемых для отправки сведений, связанных с общими папками на клиенте.</span><span class="sxs-lookup"><span data-stu-id="312f5-181">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="312f5-182">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="312f5-182">Header files</span></span>

<span data-ttu-id="312f5-183">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="312f5-183">Mapidefs.h</span></span>
  
> <span data-ttu-id="312f5-184">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="312f5-184">Provides data type definitions.</span></span>
    
<span data-ttu-id="312f5-185">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="312f5-185">Mapitags.h</span></span>
  
> <span data-ttu-id="312f5-186">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="312f5-186">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="312f5-187">См. также</span><span class="sxs-lookup"><span data-stu-id="312f5-187">See also</span></span>



[<span data-ttu-id="312f5-188">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="312f5-188">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="312f5-189">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="312f5-189">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="312f5-190">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="312f5-190">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="312f5-191">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="312f5-191">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

