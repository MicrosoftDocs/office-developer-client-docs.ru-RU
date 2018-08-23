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
ms.openlocfilehash: 626bd945851155c20850ee7f367ec6073ad57bc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570389"
---
# <a name="pidtagmessagestatus-canonical-property"></a><span data-ttu-id="12b61-103">Каноническое свойство PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="12b61-103">PidTagMessageStatus Canonical Property</span></span>

  
  
<span data-ttu-id="12b61-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12b61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12b61-105">Содержит 32-разрядная версия битовую маску флагов, который определяет состояние сообщения в таблице содержимое.</span><span class="sxs-lookup"><span data-stu-id="12b61-105">Contains a 32-bit bitmask of flags that defines the status of a message in a contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="12b61-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="12b61-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="12b61-107">PR_MSG_STATUS</span><span class="sxs-lookup"><span data-stu-id="12b61-107">PR_MSG_STATUS</span></span>  <br/> |
|<span data-ttu-id="12b61-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="12b61-108">Identifier:</span></span>  <br/> |<span data-ttu-id="12b61-109">0x0E17</span><span class="sxs-lookup"><span data-stu-id="12b61-109">0x0E17</span></span>  <br/> |
|<span data-ttu-id="12b61-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="12b61-110">Data type:</span></span>  <br/> |<span data-ttu-id="12b61-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="12b61-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="12b61-112">Область:</span><span class="sxs-lookup"><span data-stu-id="12b61-112">Area:</span></span>  <br/> |<span data-ttu-id="12b61-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="12b61-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12b61-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="12b61-114">Remarks</span></span>

<span data-ttu-id="12b61-115">Сообщения могут существовать в таблицу содержимого и в одной или нескольких таблиц результатов поиска, и каждый экземпляр сообщение может иметь другое состояние.</span><span class="sxs-lookup"><span data-stu-id="12b61-115">A message can exist in a contents table and in one or more search-results tables, and each instance of the message can have a different status.</span></span> <span data-ttu-id="12b61-116">Это свойство не следует считать свойства на сообщение, но на столбец в таблице содержимое.</span><span class="sxs-lookup"><span data-stu-id="12b61-116">This property should not be considered a property on a message but a column in a contents table.</span></span> 
  
<span data-ttu-id="12b61-117">Клиентское приложение можно установить одно или несколько из следующих флагов в этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="12b61-117">A client application can set one or more of the following flags in this property:</span></span> 
  
<span data-ttu-id="12b61-118">MSGSTATUS_ANSWERED</span><span class="sxs-lookup"><span data-stu-id="12b61-118">MSGSTATUS_ANSWERED</span></span> 
  
> <span data-ttu-id="12b61-119">Сообщение был отправлен ответ.</span><span class="sxs-lookup"><span data-stu-id="12b61-119">The message has been replied to.</span></span> 
    
<span data-ttu-id="12b61-120">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="12b61-120">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="12b61-121">Сообщение было помечено для последующего удаления.</span><span class="sxs-lookup"><span data-stu-id="12b61-121">The message has been marked for subsequent deletion.</span></span> 
    
<span data-ttu-id="12b61-122">MSGSTATUS_DRAFT</span><span class="sxs-lookup"><span data-stu-id="12b61-122">MSGSTATUS_DRAFT</span></span> 
  
> <span data-ttu-id="12b61-123">Сообщение находится в статус черновой версии.</span><span class="sxs-lookup"><span data-stu-id="12b61-123">The message is in draft revision status.</span></span> 
    
<span data-ttu-id="12b61-124">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="12b61-124">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="12b61-125">Сообщение является должны быть отключены от получателей папке отображается.</span><span class="sxs-lookup"><span data-stu-id="12b61-125">The message is to be suppressed from recipients' folder displays.</span></span> 
    
<span data-ttu-id="12b61-126">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="12b61-126">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="12b61-127">Сообщение будет выделена в папке отображается получателей.</span><span class="sxs-lookup"><span data-stu-id="12b61-127">The message is to be highlighted in recipients' folder displays.</span></span> 
    
<span data-ttu-id="12b61-128">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="12b61-128">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="12b61-129">Сообщение было помечено для удаления в магазине удаленных сообщений без загрузки локального клиента.</span><span class="sxs-lookup"><span data-stu-id="12b61-129">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span> 
    
<span data-ttu-id="12b61-130">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="12b61-130">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="12b61-131">Сообщение было помечено для загрузки с хранения удаленных сообщений для локального клиента.</span><span class="sxs-lookup"><span data-stu-id="12b61-131">The message has been marked for downloading from the remote message store to the local client.</span></span> 
    
<span data-ttu-id="12b61-132">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="12b61-132">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="12b61-133">Сообщение уже помечен для определенного клиента цели.</span><span class="sxs-lookup"><span data-stu-id="12b61-133">The message has been tagged for a client-defined purpose.</span></span>
    
<span data-ttu-id="12b61-134">Флаги **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**и **MSGSTATUS_TAGGED** определяются клиента.</span><span class="sxs-lookup"><span data-stu-id="12b61-134">The **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**, and **MSGSTATUS_TAGGED** flags are defined by the client.</span></span> <span data-ttu-id="12b61-135">Поставщики транспорта и хранилища передайте эти биты без каких-либо действий.</span><span class="sxs-lookup"><span data-stu-id="12b61-135">Transport and store providers pass these bits without any action.</span></span> 
  
<span data-ttu-id="12b61-136">Клиенты могут интерпретировать эти значения никаких уведомлений, подходящую для своих приложений.</span><span class="sxs-lookup"><span data-stu-id="12b61-136">Clients can interpret these values in any way that is appropriate for their applications.</span></span> <span data-ttu-id="12b61-137">Для отображения сообщения, помеченные для удаления со значком пример является одним из способов, что количество клиентов использовать это свойство.</span><span class="sxs-lookup"><span data-stu-id="12b61-137">One way that many clients use this property is to display messages marked for deletion with a representative icon.</span></span> 
  
<span data-ttu-id="12b61-138">Средство просмотра удаленных клиентов можно установить **MSGSTATUS_REMOTE_DELETE** или **MSGSTATUS_REMOTE_DOWNLOAD** для сообщений в папке заголовок, предоставленных поставщиком удаленного транспорта.</span><span class="sxs-lookup"><span data-stu-id="12b61-138">A remote viewer client can set **MSGSTATUS_REMOTE_DELETE** or **MSGSTATUS_REMOTE_DOWNLOAD** on messages in the header folder presented to it by the remote transport provider.</span></span> <span data-ttu-id="12b61-139">Клиентское приложение может проверить заголовок каждого сообщения в эту папку, чтобы определить загружен или удаляются, хранения удаленных сообщений сообщения.</span><span class="sxs-lookup"><span data-stu-id="12b61-139">The client application can examine each message header in this folder to determine whether the message should be downloaded or deleted at the remote message store.</span></span> <span data-ttu-id="12b61-140">Он используется метод [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) установить соответствующий флаг.</span><span class="sxs-lookup"><span data-stu-id="12b61-140">It then uses the [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) method to set the appropriate flag.</span></span> <span data-ttu-id="12b61-141">**SetMessageStatus** — это единственный способ задайте флаги в этого свойства. метод [IMAPIProp::SetProps](imapiprop-setprops.md) не может использоваться.</span><span class="sxs-lookup"><span data-stu-id="12b61-141">**SetMessageStatus** is the only way to set any of the flags in this property; the [IMAPIProp::SetProps](imapiprop-setprops.md) method cannot be used.</span></span> <span data-ttu-id="12b61-142">Для получения этого свойства, клиенты вызывать [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) , а не [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="12b61-142">To retrieve this property, clients call [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) rather than [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
  
<span data-ttu-id="12b61-143">Бит 16 до 31 (0x10000 через 0x80000000) этого свойства доступны для использования клиентским приложением электронной почты — это сообщение (IPM).</span><span class="sxs-lookup"><span data-stu-id="12b61-143">Bits 16 through 31 (0x10000 through 0x80000000) of this property are available for use by the interpersonal message (IPM) client application.</span></span> <span data-ttu-id="12b61-144">Все другие биты, зарезервированы для использования с MAPI; не определенных в предыдущей таблице следует сначала задать нулевое значение и не изменить в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="12b61-144">All other bits are reserved for use by MAPI; those not defined in the preceding table should be initially set to zero and not altered subsequently.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="12b61-145">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="12b61-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="12b61-146">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="12b61-146">Protocol specifications</span></span>

<span data-ttu-id="12b61-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12b61-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12b61-148">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="12b61-148">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="12b61-149">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12b61-149">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12b61-150">Обрабатывает синхронизации обмена сообщениями объект данных между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="12b61-150">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="12b61-151">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="12b61-151">Header files</span></span>

<span data-ttu-id="12b61-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="12b61-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="12b61-153">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="12b61-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="12b61-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="12b61-154">Mapitags.h</span></span>
  
> <span data-ttu-id="12b61-155">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="12b61-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12b61-156">См. также</span><span class="sxs-lookup"><span data-stu-id="12b61-156">See also</span></span>



[<span data-ttu-id="12b61-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="12b61-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)


[<span data-ttu-id="12b61-158">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="12b61-158">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="12b61-159">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="12b61-159">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="12b61-160">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="12b61-160">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="12b61-161">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="12b61-161">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

