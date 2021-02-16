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
ms.openlocfilehash: 7f3cf5b245bdcd2c2707f0e2028d52a15c7e0f6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434503"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a><span data-ttu-id="07a68-103">Поддержка форматированный текст во входящих сообщениях: обязанности клиента</span><span class="sxs-lookup"><span data-stu-id="07a68-103">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="07a68-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07a68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07a68-105">При передаче сообщений между системами обмена сообщениями пул MAPI позволяет синхронизировать форматирование форматирования с текстом сообщения.</span><span class="sxs-lookup"><span data-stu-id="07a68-105">As messages are transferred between messaging systems, the MAPI spooler makes sure that the rich text formatting remains synchronized with the message text.</span></span> <span data-ttu-id="07a68-106">Пулер MAPI вызывает функцию [RTFSync](rtfsync.md) из оболочки сообщения, которое передает поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="07a68-106">The MAPI spooler calls the [RTFSync](rtfsync.md) function from within a wrapped version of the message that it passes to the transport provider.</span></span> <span data-ttu-id="07a68-107">Поставщик транспорта сохраняет изменения, внесенные в сообщение, вызывая метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) и перенаправ его новому получателю.</span><span class="sxs-lookup"><span data-stu-id="07a68-107">The transport provider saves the changes made to the message by calling the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and then routes it to the new recipient.</span></span> 
  
<span data-ttu-id="07a68-108">Когда клиентская приложение получателя с RTF открывает сообщение для отображения текста, оно должно синхронизировать текст с форматированием и открыть **PR_RTF_COMPRESSED** ([PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)или **PR_BODY** ([PidTagBody),](pidtagbody-canonical-property.md)в зависимости от того, какое свойство доступно.</span><span class="sxs-lookup"><span data-stu-id="07a68-108">When the recipient's RTF-aware client application opens the message to display the text, it must synchronize the text with the formatting and open either **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), depending on which property is available.</span></span>
  
 <span data-ttu-id="07a68-109">**Чтобы открыть сообщение, клиенты с RTF**</span><span class="sxs-lookup"><span data-stu-id="07a68-109">**To open a message, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="07a68-110">Вызовите **RTFSync,** чтобы синхронизировать текст сообщения с форматированием, если хранилище сообщений не знает RTF.</span><span class="sxs-lookup"><span data-stu-id="07a68-110">Call **RTFSync** to synchronize the message text with the formatting if the message store is not RTF-aware.</span></span> <span data-ttu-id="07a68-111">Флаг RTF_SYNC_BODY_CHANGED должен передаваться в  _параметре ulFlags,_ если свойство **PR_RTF_IN_SYNC** ([PidTagRtfInSync)](pidtagrtfinsync-canonical-property.md)отсутствует или задано как FALSE.</span><span class="sxs-lookup"><span data-stu-id="07a68-111">The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE.</span></span> <span data-ttu-id="07a68-112">Клиенты, работающие с хранилищами сообщений с RTF, не должны вызывать **RTFSync,** так как хранилище сообщений об этом позаботится.</span><span class="sxs-lookup"><span data-stu-id="07a68-112">Clients working with RTF-aware message stores need not make the **RTFSync** call because the message store takes care of it.</span></span> 
    
2. <span data-ttu-id="07a68-113">Вызовите [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) если текст сообщения обновлен.</span><span class="sxs-lookup"><span data-stu-id="07a68-113">Call [IMAPIProp::SaveChanges](imapiprop-savechanges.md) if the message text has been updated.</span></span> 
    
3. <span data-ttu-id="07a68-114">Вызовите [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) чтобы открыть **PR_RTF_COMPRESSED** свойства.</span><span class="sxs-lookup"><span data-stu-id="07a68-114">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="07a68-115">Если **PR_RTF_COMPRESSED** недоступны, следует открыть свойство  PR_BODY, чтобы отобразить содержимое сообщения.</span><span class="sxs-lookup"><span data-stu-id="07a68-115">If **PR_RTF_COMPRESSED** is not available, you should open the **PR_BODY** property instead to display the message content.</span></span> 
    
4. <span data-ttu-id="07a68-116">Вызовите [функцию WrapCompressedRTFStream,](wrapcompressedrtfstream.md) чтобы создать несжатую версию сжатых данных RTF, если они доступны.</span><span class="sxs-lookup"><span data-stu-id="07a68-116">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function to create an uncompressed version of the compressed RTF data, if available.</span></span> 
    
5. <span data-ttu-id="07a68-117">Отображение несмеченных данных RTF или обычных текстовых данных для пользователя.</span><span class="sxs-lookup"><span data-stu-id="07a68-117">Display the uncompressed RTF data or the plain text data to the user.</span></span>
    
 <span data-ttu-id="07a68-118">**RTFSync** возвращает boolean значение, которое указывает, было ли сообщение обновлено.</span><span class="sxs-lookup"><span data-stu-id="07a68-118">**RTFSync** returns a Boolean value that indicates whether or not the message has been updated.</span></span> <span data-ttu-id="07a68-119">Если это значение возвращает значение TRUE, вызовите **SaveChanges** в определенный момент, чтобы сделать обновление постоянным.</span><span class="sxs-lookup"><span data-stu-id="07a68-119">If this value returns TRUE, call **SaveChanges** at some point to make the update permanent.</span></span> <span data-ttu-id="07a68-120">Вызов не нужно делать сразу после возврата **RTFSync.**</span><span class="sxs-lookup"><span data-stu-id="07a68-120">The call does not have to be made immediately after **RTFSync** returns.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="07a68-121">Так как перед его получением многие компоненты обрабатывают отформатированный текст, существует вероятность повреждения.</span><span class="sxs-lookup"><span data-stu-id="07a68-121">Because so many components handle the formatted text before you receive it, there is the possibility of corruption.</span></span> <span data-ttu-id="07a68-122">Это может произойть из-за поставщика хранения сообщений, стороннего приложения, шлюза или ошибки передачи.</span><span class="sxs-lookup"><span data-stu-id="07a68-122">This corruption could come from the message store provider, a third party application, a gateway, or a transmission error.</span></span> 
  

