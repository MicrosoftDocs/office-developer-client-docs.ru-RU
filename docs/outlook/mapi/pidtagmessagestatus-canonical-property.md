---
title: Каноническое свойство PidTagMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageStatus
api_type:
- HeaderDef
ms.assetid: e479e863-a8de-4f7e-9eae-3f721cd16e9a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dacd759d978394a5f4ed028915ed1c717bf6efe5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355722"
---
# <a name="pidtagmessagestatus-canonical-property"></a><span data-ttu-id="ea203-103">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="ea203-103">PidTagMessageStatus Canonical Property</span></span>

  
  
<span data-ttu-id="ea203-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea203-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea203-105">Содержит 32-битную битмаку флагов, определяемую состояние сообщения в таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="ea203-105">Contains a 32-bit bitmask of flags that defines the status of a message in a contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ea203-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ea203-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ea203-107">PR_MSG_STATUS</span><span class="sxs-lookup"><span data-stu-id="ea203-107">PR_MSG_STATUS</span></span>  <br/> |
|<span data-ttu-id="ea203-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ea203-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ea203-109">0x0E17</span><span class="sxs-lookup"><span data-stu-id="ea203-109">0x0E17</span></span>  <br/> |
|<span data-ttu-id="ea203-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ea203-110">Data type:</span></span>  <br/> |<span data-ttu-id="ea203-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ea203-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ea203-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ea203-112">Area:</span></span>  <br/> |<span data-ttu-id="ea203-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="ea203-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea203-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ea203-114">Remarks</span></span>

<span data-ttu-id="ea203-115">Сообщение может существовать в таблице содержимого и в одной или нескольких таблицах результатов поиска, и каждый экземпляр сообщения может иметь другой статус.</span><span class="sxs-lookup"><span data-stu-id="ea203-115">A message can exist in a contents table and in one or more search-results tables, and each instance of the message can have a different status.</span></span> <span data-ttu-id="ea203-116">Это свойство не должно считаться свойством сообщения, а столбцом в таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="ea203-116">This property should not be considered a property on a message but a column in a contents table.</span></span> 
  
<span data-ttu-id="ea203-117">Клиентская заявка может установить один или несколько из следующих флагов в этом свойстве:</span><span class="sxs-lookup"><span data-stu-id="ea203-117">A client application can set one or more of the following flags in this property:</span></span> 
  
<span data-ttu-id="ea203-118">MSGSTATUS_ANSWERED</span><span class="sxs-lookup"><span data-stu-id="ea203-118">MSGSTATUS_ANSWERED</span></span> 
  
> <span data-ttu-id="ea203-119">Сообщение было отписано.</span><span class="sxs-lookup"><span data-stu-id="ea203-119">The message has been replied to.</span></span> 
    
<span data-ttu-id="ea203-120">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="ea203-120">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="ea203-121">Сообщение помечено для последующего удаления.</span><span class="sxs-lookup"><span data-stu-id="ea203-121">The message has been marked for subsequent deletion.</span></span> 
    
<span data-ttu-id="ea203-122">MSGSTATUS_DRAFT</span><span class="sxs-lookup"><span data-stu-id="ea203-122">MSGSTATUS_DRAFT</span></span> 
  
> <span data-ttu-id="ea203-123">Сообщение находится в состоянии редакции проекта.</span><span class="sxs-lookup"><span data-stu-id="ea203-123">The message is in draft revision status.</span></span> 
    
<span data-ttu-id="ea203-124">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="ea203-124">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="ea203-125">Сообщение должно быть подавлено с папок получателей.</span><span class="sxs-lookup"><span data-stu-id="ea203-125">The message is to be suppressed from recipients' folder displays.</span></span> 
    
<span data-ttu-id="ea203-126">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="ea203-126">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="ea203-127">Сообщение должно быть выделено в папках получателей.</span><span class="sxs-lookup"><span data-stu-id="ea203-127">The message is to be highlighted in recipients' folder displays.</span></span> 
    
<span data-ttu-id="ea203-128">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="ea203-128">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="ea203-129">Сообщение помечено для удаления в хранилище удаленных сообщений без загрузки в локальный клиент.</span><span class="sxs-lookup"><span data-stu-id="ea203-129">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span> 
    
<span data-ttu-id="ea203-130">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="ea203-130">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="ea203-131">Сообщение помечено для скачивания из удаленного магазина сообщений в локальный клиент.</span><span class="sxs-lookup"><span data-stu-id="ea203-131">The message has been marked for downloading from the remote message store to the local client.</span></span> 
    
<span data-ttu-id="ea203-132">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="ea203-132">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="ea203-133">Сообщение помечено для определенной клиентом цели.</span><span class="sxs-lookup"><span data-stu-id="ea203-133">The message has been tagged for a client-defined purpose.</span></span>
    
<span data-ttu-id="ea203-134">Флаги **MSGSTATUS_DELMARKED,** **MSGSTATUS_HIDDEN,** **MSGSTATUS_HIGHLIGHTED** и **MSGSTATUS_TAGGED** определяются клиентом.</span><span class="sxs-lookup"><span data-stu-id="ea203-134">The **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**, and **MSGSTATUS_TAGGED** flags are defined by the client.</span></span> <span data-ttu-id="ea203-135">Поставщики транспорта и магазина передают эти биты без каких-либо действий.</span><span class="sxs-lookup"><span data-stu-id="ea203-135">Transport and store providers pass these bits without any action.</span></span> 
  
<span data-ttu-id="ea203-136">Клиенты могут интерпретировать эти значения любым способом, подходящим для их приложений.</span><span class="sxs-lookup"><span data-stu-id="ea203-136">Clients can interpret these values in any way that is appropriate for their applications.</span></span> <span data-ttu-id="ea203-137">Одним из способов использования этого свойства для многих клиентов является отображение сообщений, помеченных для удаления с помощью символа представителя.</span><span class="sxs-lookup"><span data-stu-id="ea203-137">One way that many clients use this property is to display messages marked for deletion with a representative icon.</span></span> 
  
<span data-ttu-id="ea203-138">Клиент удаленного просмотра  может MSGSTATUS_REMOTE_DELETE **или MSGSTATUS_REMOTE_DOWNLOAD** на сообщения в папке header, представленной ему поставщиком удаленного транспорта.</span><span class="sxs-lookup"><span data-stu-id="ea203-138">A remote viewer client can set **MSGSTATUS_REMOTE_DELETE** or **MSGSTATUS_REMOTE_DOWNLOAD** on messages in the header folder presented to it by the remote transport provider.</span></span> <span data-ttu-id="ea203-139">Клиентская заявка может проверять каждый заглавный текст сообщения в этой папке, чтобы определить, следует ли скачивать или удалять сообщение в удаленном хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ea203-139">The client application can examine each message header in this folder to determine whether the message should be downloaded or deleted at the remote message store.</span></span> <span data-ttu-id="ea203-140">Затем используется метод [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) для набора соответствующего флага.</span><span class="sxs-lookup"><span data-stu-id="ea203-140">It then uses the [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) method to set the appropriate flag.</span></span> <span data-ttu-id="ea203-141">**SetMessageStatus** — это единственный способ установить любой из флагов в этом свойстве; нельзя [использовать метод IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="ea203-141">**SetMessageStatus** is the only way to set any of the flags in this property; the [IMAPIProp::SetProps](imapiprop-setprops.md) method cannot be used.</span></span> <span data-ttu-id="ea203-142">Чтобы получить это свойство, клиенты называют [IMAPIFolder::GetMessageStatus,](imapifolder-getmessagestatus.md) а не [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="ea203-142">To retrieve this property, clients call [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) rather than [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
  
<span data-ttu-id="ea203-143">Биты от 16 до 31 (0x10000 0x80000000) этого свойства доступны для использования клиентского приложения для межличностного сообщения (IPM).</span><span class="sxs-lookup"><span data-stu-id="ea203-143">Bits 16 through 31 (0x10000 through 0x80000000) of this property are available for use by the interpersonal message (IPM) client application.</span></span> <span data-ttu-id="ea203-144">Все остальные биты зарезервированы для использования MAPI; те, которые не определены в предыдущей таблице, сначала должны быть задатки нулю, а не изменены впоследствии.</span><span class="sxs-lookup"><span data-stu-id="ea203-144">All other bits are reserved for use by MAPI; those not defined in the preceding table should be initially set to zero and not altered subsequently.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ea203-145">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ea203-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ea203-146">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ea203-146">Protocol specifications</span></span>

<span data-ttu-id="ea203-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea203-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea203-148">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="ea203-148">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ea203-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea203-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea203-150">Обрабатывает синхронизацию данных объектов обмена сообщениями между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="ea203-150">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ea203-151">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="ea203-151">Header files</span></span>

<span data-ttu-id="ea203-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ea203-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="ea203-153">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ea203-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="ea203-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ea203-154">Mapitags.h</span></span>
  
> <span data-ttu-id="ea203-155">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="ea203-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ea203-156">См. также</span><span class="sxs-lookup"><span data-stu-id="ea203-156">See also</span></span>



[<span data-ttu-id="ea203-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="ea203-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)


[<span data-ttu-id="ea203-158">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ea203-158">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ea203-159">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ea203-159">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ea203-160">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ea203-160">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ea203-161">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="ea203-161">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

