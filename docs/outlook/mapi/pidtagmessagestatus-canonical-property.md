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
# <a name="pidtagmessagestatus-canonical-property"></a><span data-ttu-id="3831f-103">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="3831f-103">PidTagMessageStatus Canonical Property</span></span>

  
  
<span data-ttu-id="3831f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3831f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3831f-105">Содержит 32-битовую битовуюmask флагов, которая определяет состояние сообщения в таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="3831f-105">Contains a 32-bit bitmask of flags that defines the status of a message in a contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3831f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3831f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3831f-107">PR_MSG_STATUS</span><span class="sxs-lookup"><span data-stu-id="3831f-107">PR_MSG_STATUS</span></span>  <br/> |
|<span data-ttu-id="3831f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3831f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3831f-109">0x0E17</span><span class="sxs-lookup"><span data-stu-id="3831f-109">0x0E17</span></span>  <br/> |
|<span data-ttu-id="3831f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3831f-110">Data type:</span></span>  <br/> |<span data-ttu-id="3831f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3831f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3831f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3831f-112">Area:</span></span>  <br/> |<span data-ttu-id="3831f-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="3831f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3831f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="3831f-114">Remarks</span></span>

<span data-ttu-id="3831f-115">Сообщение может существовать в таблице содержимого и в одной или нескольких таблицах результатов поиска, а каждый экземпляр сообщения может иметь разное состояние.</span><span class="sxs-lookup"><span data-stu-id="3831f-115">A message can exist in a contents table and in one or more search-results tables, and each instance of the message can have a different status.</span></span> <span data-ttu-id="3831f-116">Это свойство не должно считаться свойством сообщения, а столбцом в таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="3831f-116">This property should not be considered a property on a message but a column in a contents table.</span></span> 
  
<span data-ttu-id="3831f-117">Клиентские приложения могут установить один или несколько из следующих флагов в этом свойстве:</span><span class="sxs-lookup"><span data-stu-id="3831f-117">A client application can set one or more of the following flags in this property:</span></span> 
  
<span data-ttu-id="3831f-118">MSGSTATUS_ANSWERED</span><span class="sxs-lookup"><span data-stu-id="3831f-118">MSGSTATUS_ANSWERED</span></span> 
  
> <span data-ttu-id="3831f-119">На сообщение был ответ.</span><span class="sxs-lookup"><span data-stu-id="3831f-119">The message has been replied to.</span></span> 
    
<span data-ttu-id="3831f-120">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="3831f-120">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="3831f-121">Сообщение помечено для последующего удаления.</span><span class="sxs-lookup"><span data-stu-id="3831f-121">The message has been marked for subsequent deletion.</span></span> 
    
<span data-ttu-id="3831f-122">MSGSTATUS_DRAFT</span><span class="sxs-lookup"><span data-stu-id="3831f-122">MSGSTATUS_DRAFT</span></span> 
  
> <span data-ttu-id="3831f-123">Сообщение находится в состоянии черновика редакции.</span><span class="sxs-lookup"><span data-stu-id="3831f-123">The message is in draft revision status.</span></span> 
    
<span data-ttu-id="3831f-124">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="3831f-124">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="3831f-125">Сообщение должно быть отобрачено из папки получателей.</span><span class="sxs-lookup"><span data-stu-id="3831f-125">The message is to be suppressed from recipients' folder displays.</span></span> 
    
<span data-ttu-id="3831f-126">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="3831f-126">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="3831f-127">Сообщение должно быть выделено в папке получателей.</span><span class="sxs-lookup"><span data-stu-id="3831f-127">The message is to be highlighted in recipients' folder displays.</span></span> 
    
<span data-ttu-id="3831f-128">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="3831f-128">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="3831f-129">Сообщение помечено для удаления в удаленном хранилище сообщений без загрузки в локальный клиент.</span><span class="sxs-lookup"><span data-stu-id="3831f-129">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span> 
    
<span data-ttu-id="3831f-130">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="3831f-130">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="3831f-131">Сообщение помечено для скачивания из удаленного хранения сообщений в локальный клиент.</span><span class="sxs-lookup"><span data-stu-id="3831f-131">The message has been marked for downloading from the remote message store to the local client.</span></span> 
    
<span data-ttu-id="3831f-132">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="3831f-132">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="3831f-133">Сообщение помечено для определенной клиентом цели.</span><span class="sxs-lookup"><span data-stu-id="3831f-133">The message has been tagged for a client-defined purpose.</span></span>
    
<span data-ttu-id="3831f-134">Флаги **MSGSTATUS_DELMARKED,** **MSGSTATUS_HIDDEN,** **MSGSTATUS_HIGHLIGHTED** и MSGSTATUS_TAGGED определяются  клиентом.</span><span class="sxs-lookup"><span data-stu-id="3831f-134">The **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**, and **MSGSTATUS_TAGGED** flags are defined by the client.</span></span> <span data-ttu-id="3831f-135">Поставщики транспорта и хранения передают эти биты без каких-либо действий.</span><span class="sxs-lookup"><span data-stu-id="3831f-135">Transport and store providers pass these bits without any action.</span></span> 
  
<span data-ttu-id="3831f-136">Клиенты могут интерпретировать эти значения любым способом, который подходит для их приложений.</span><span class="sxs-lookup"><span data-stu-id="3831f-136">Clients can interpret these values in any way that is appropriate for their applications.</span></span> <span data-ttu-id="3831f-137">Один из способов использования этого свойства многими клиентами — отображение сообщений, помеченных для удаления с помощью символьного значка.</span><span class="sxs-lookup"><span data-stu-id="3831f-137">One way that many clients use this property is to display messages marked for deletion with a representative icon.</span></span> 
  
<span data-ttu-id="3831f-138">Клиент удаленного просмотра  может MSGSTATUS_REMOTE_DELETE или **MSGSTATUS_REMOTE_DOWNLOAD** для сообщений в папке header, представляемой ему поставщиком удаленного транспорта.</span><span class="sxs-lookup"><span data-stu-id="3831f-138">A remote viewer client can set **MSGSTATUS_REMOTE_DELETE** or **MSGSTATUS_REMOTE_DOWNLOAD** on messages in the header folder presented to it by the remote transport provider.</span></span> <span data-ttu-id="3831f-139">Клиентские приложения могут проверять каждый заголок сообщений в этой папке, чтобы определить, следует ли скачивать или удалять сообщение в удаленном хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="3831f-139">The client application can examine each message header in this folder to determine whether the message should be downloaded or deleted at the remote message store.</span></span> <span data-ttu-id="3831f-140">Затем он использует метод [IMAPIFolder::SetMessageStatus,](imapifolder-setmessagestatus.md) чтобы установить соответствующий флаг.</span><span class="sxs-lookup"><span data-stu-id="3831f-140">It then uses the [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) method to set the appropriate flag.</span></span> <span data-ttu-id="3831f-141">**SetMessageStatus** — единственный способ установить любой из флагов в этом свойстве; Невозможно [использовать метод IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="3831f-141">**SetMessageStatus** is the only way to set any of the flags in this property; the [IMAPIProp::SetProps](imapiprop-setprops.md) method cannot be used.</span></span> <span data-ttu-id="3831f-142">Чтобы получить это свойство, клиенты вызывают [IMAPIFolder::GetMessageStatus,](imapifolder-getmessagestatus.md) а [не IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="3831f-142">To retrieve this property, clients call [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) rather than [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
  
<span data-ttu-id="3831f-143">Биты от 16 до 31 (0x10000 0x80000000) этого свойства доступны для использования клиентского приложения IPM.</span><span class="sxs-lookup"><span data-stu-id="3831f-143">Bits 16 through 31 (0x10000 through 0x80000000) of this property are available for use by the interpersonal message (IPM) client application.</span></span> <span data-ttu-id="3831f-144">Все остальные биты зарезервированы для использования в MAPI; те, которые не определены в предыдущей таблице, должны изначально иметь нулевое значение и не изменяться в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="3831f-144">All other bits are reserved for use by MAPI; those not defined in the preceding table should be initially set to zero and not altered subsequently.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3831f-145">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3831f-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3831f-146">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3831f-146">Protocol specifications</span></span>

<span data-ttu-id="3831f-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3831f-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3831f-148">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="3831f-148">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3831f-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3831f-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3831f-150">Обрабатывает синхронизацию данных объектов обмена сообщениями между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="3831f-150">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3831f-151">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="3831f-151">Header files</span></span>

<span data-ttu-id="3831f-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3831f-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="3831f-153">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3831f-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="3831f-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3831f-154">Mapitags.h</span></span>
  
> <span data-ttu-id="3831f-155">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="3831f-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3831f-156">См. также</span><span class="sxs-lookup"><span data-stu-id="3831f-156">See also</span></span>



[<span data-ttu-id="3831f-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="3831f-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)


[<span data-ttu-id="3831f-158">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3831f-158">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3831f-159">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3831f-159">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3831f-160">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3831f-160">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3831f-161">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3831f-161">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

