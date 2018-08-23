---
title: Поддержка форматированный текст в обязанности клиента входящих сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d8fdd9ea4dfbc40d7e800be5e2df666738d2cd23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577459"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a><span data-ttu-id="6c28d-103">Поддержка форматированного текста во входящих сообщениях: обязанности клиентов</span><span class="sxs-lookup"><span data-stu-id="6c28d-103">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="6c28d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c28d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c28d-105">Как сообщения передаются между систем обмена сообщениями, диспетчер очереди MAPI следит за тем, что форматирование текста остается синхронизированной с текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="6c28d-105">As messages are transferred between messaging systems, the MAPI spooler makes sure that the rich text formatting remains synchronized with the message text.</span></span> <span data-ttu-id="6c28d-106">Диспетчер очереди MAPI вызывает функцию [RTFSync](rtfsync.md) в оболочку версии сообщение, которое передается поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="6c28d-106">The MAPI spooler calls the [RTFSync](rtfsync.md) function from within a wrapped version of the message that it passes to the transport provider.</span></span> <span data-ttu-id="6c28d-107">Поставщика транспорта сохраняет изменения, внесенные в сообщение путем вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) и направляет его нового получателя.</span><span class="sxs-lookup"><span data-stu-id="6c28d-107">The transport provider saves the changes made to the message by calling the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and then routes it to the new recipient.</span></span> 
  
<span data-ttu-id="6c28d-108">При получателя RTF клиентское приложение открывает сообщение для отображения текста, его необходимо синхронизировать текст с форматированием и откройте **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) или **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) , в зависимости от того, какие свойства недоступны.</span><span class="sxs-lookup"><span data-stu-id="6c28d-108">When the recipient's RTF-aware client application opens the message to display the text, it must synchronize the text with the formatting and open either **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), depending on which property is available.</span></span>
  
 <span data-ttu-id="6c28d-109">**Чтобы открыть сообщение, поддерживающую RTF клиентов**</span><span class="sxs-lookup"><span data-stu-id="6c28d-109">**To open a message, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="6c28d-110">Вызовите **RTFSync** , чтобы синхронизировать текст сообщения с форматированием, если не учитывать RTF хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="6c28d-110">Call **RTFSync** to synchronize the message text with the formatting if the message store is not RTF-aware.</span></span> <span data-ttu-id="6c28d-111">Флаг RTF_SYNC_BODY_CHANGED должен передаваться в параметре _ulFlags_ , если свойство **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) отсутствует или задано значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="6c28d-111">The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE.</span></span> <span data-ttu-id="6c28d-112">Клиентов, работающих с поддержкой RTF хранилищ сообщений не нужна выполнения вызова **RTFSync** , поскольку хранилище сообщений отвечает за его.</span><span class="sxs-lookup"><span data-stu-id="6c28d-112">Clients working with RTF-aware message stores need not make the **RTFSync** call because the message store takes care of it.</span></span> 
    
2. <span data-ttu-id="6c28d-113">Вызовите [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , если были внесены текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="6c28d-113">Call [IMAPIProp::SaveChanges](imapiprop-savechanges.md) if the message text has been updated.</span></span> 
    
3. <span data-ttu-id="6c28d-114">Вызовите [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , чтобы открыть свойство **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="6c28d-114">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="6c28d-115">Если **PR_RTF_COMPRESSED** не поддерживается, следует вместо этого откройте свойство **PR_BODY** для отображения содержимого сообщения.</span><span class="sxs-lookup"><span data-stu-id="6c28d-115">If **PR_RTF_COMPRESSED** is not available, you should open the **PR_BODY** property instead to display the message content.</span></span> 
    
4. <span data-ttu-id="6c28d-116">Вызовите функцию [WrapCompressedRTFStream](wrapcompressedrtfstream.md) для создания несжатую версию сжатых данных RTF, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="6c28d-116">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function to create an uncompressed version of the compressed RTF data, if available.</span></span> 
    
5. <span data-ttu-id="6c28d-117">Отображение несжатого данные в формате RTF или обычного текста данных для пользователя.</span><span class="sxs-lookup"><span data-stu-id="6c28d-117">Display the uncompressed RTF data or the plain text data to the user.</span></span>
    
 <span data-ttu-id="6c28d-118">**RTFSync** возвращает логическое значение, указывающее, обновлен ли сообщение.</span><span class="sxs-lookup"><span data-stu-id="6c28d-118">**RTFSync** returns a Boolean value that indicates whether or not the message has been updated.</span></span> <span data-ttu-id="6c28d-119">Если это значение возвращает значение TRUE, вызов **SaveChanges** в определенный момент, чтобы обновление было постоянным.</span><span class="sxs-lookup"><span data-stu-id="6c28d-119">If this value returns TRUE, call **SaveChanges** at some point to make the update permanent.</span></span> <span data-ttu-id="6c28d-120">Вызов не должны быть выполнены немедленно после возвращает **RTFSync** .</span><span class="sxs-lookup"><span data-stu-id="6c28d-120">The call does not have to be made immediately after **RTFSync** returns.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6c28d-121">Так как слишком большом числе компоненты обрабатывать форматированного текста, прежде чем вы получаете, нет возможности повреждения.</span><span class="sxs-lookup"><span data-stu-id="6c28d-121">Because so many components handle the formatted text before you receive it, there is the possibility of corruption.</span></span> <span data-ttu-id="6c28d-122">В этом повреждения могут быть получены от поставщика хранилища сообщений, приложения сторонних производителей, шлюза или Ошибка передачи.</span><span class="sxs-lookup"><span data-stu-id="6c28d-122">This corruption could come from the message store provider, a third party application, a gateway, or a transmission error.</span></span> 
  

