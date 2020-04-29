---
title: Поддержка форматированного текста во входящих сообщениях обязанности клиента
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
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a><span data-ttu-id="4aad3-103">Поддержка форматированного текста во входящих сообщениях: обязанности клиентов</span><span class="sxs-lookup"><span data-stu-id="4aad3-103">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="4aad3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4aad3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4aad3-105">Когда сообщения передаются между системами обмена сообщениями, диспетчер очереди MAPI гарантирует, что форматирование форматированного текста будет синхронизировано с текстом сообщения.</span><span class="sxs-lookup"><span data-stu-id="4aad3-105">As messages are transferred between messaging systems, the MAPI spooler makes sure that the rich text formatting remains synchronized with the message text.</span></span> <span data-ttu-id="4aad3-106">Диспетчер очереди MAPI вызывает функцию [ртфсинк](rtfsync.md) из упакованной версии сообщения, которая передается поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="4aad3-106">The MAPI spooler calls the [RTFSync](rtfsync.md) function from within a wrapped version of the message that it passes to the transport provider.</span></span> <span data-ttu-id="4aad3-107">Поставщик транспорта сохраняет изменения, внесенные в сообщение, вызывая метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) и направляет его новому получателю.</span><span class="sxs-lookup"><span data-stu-id="4aad3-107">The transport provider saves the changes made to the message by calling the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and then routes it to the new recipient.</span></span> 
  
<span data-ttu-id="4aad3-108">Когда клиентское приложение, поддерживающее формат RTF, открывает сообщение для отображения текста, оно должно синхронизировать текст с форматированием и открыть **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) или **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) в зависимости от того, какое свойство доступно.</span><span class="sxs-lookup"><span data-stu-id="4aad3-108">When the recipient's RTF-aware client application opens the message to display the text, it must synchronize the text with the formatting and open either **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), depending on which property is available.</span></span>
  
 <span data-ttu-id="4aad3-109">**Открытие сообщения и клиентов, поддерживающих RTF**</span><span class="sxs-lookup"><span data-stu-id="4aad3-109">**To open a message, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="4aad3-110">Вызов **ртфсинк** для синхронизации текста сообщения с форматированием, если хранилище сообщений не имеет формата RTF.</span><span class="sxs-lookup"><span data-stu-id="4aad3-110">Call **RTFSync** to synchronize the message text with the formatting if the message store is not RTF-aware.</span></span> <span data-ttu-id="4aad3-111">Флаг RTF_SYNC_BODY_CHANGED следует передавать в параметре _ulFlags_ , если свойство **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) отсутствует или имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="4aad3-111">The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE.</span></span> <span data-ttu-id="4aad3-112">Для клиентов, работающих с хранилищами сообщений в формате RTF, не требуется выполнять вызов **ртфсинк** , так как он занимается хранилищем сообщений.</span><span class="sxs-lookup"><span data-stu-id="4aad3-112">Clients working with RTF-aware message stores need not make the **RTFSync** call because the message store takes care of it.</span></span> 
    
2. <span data-ttu-id="4aad3-113">Call [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) , если текст сообщения был обновлен.</span><span class="sxs-lookup"><span data-stu-id="4aad3-113">Call [IMAPIProp::SaveChanges](imapiprop-savechanges.md) if the message text has been updated.</span></span> 
    
3. <span data-ttu-id="4aad3-114">Call [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , чтобы открыть свойство **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="4aad3-114">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="4aad3-115">Если **PR_RTF_COMPRESSED** недоступен, то для отображения содержимого сообщения следует открыть свойство **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="4aad3-115">If **PR_RTF_COMPRESSED** is not available, you should open the **PR_BODY** property instead to display the message content.</span></span> 
    
4. <span data-ttu-id="4aad3-116">Вызовите функцию [врапкомпресседртфстреам](wrapcompressedrtfstream.md) , чтобы создать несжатую версию сжатых данных RTF, если они доступны.</span><span class="sxs-lookup"><span data-stu-id="4aad3-116">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function to create an uncompressed version of the compressed RTF data, if available.</span></span> 
    
5. <span data-ttu-id="4aad3-117">Отображение несжатых данных в формате RTF или данных в формате обычного текста для пользователя.</span><span class="sxs-lookup"><span data-stu-id="4aad3-117">Display the uncompressed RTF data or the plain text data to the user.</span></span>
    
 <span data-ttu-id="4aad3-118">**Ртфсинк** возвращает логическое значение, указывающее, было ли обновление сообщения.</span><span class="sxs-lookup"><span data-stu-id="4aad3-118">**RTFSync** returns a Boolean value that indicates whether or not the message has been updated.</span></span> <span data-ttu-id="4aad3-119">Если это значение возвращает значение TRUE, метод **SaveChanges** вызывается в некоторый момент, чтобы сделать обновление постоянным.</span><span class="sxs-lookup"><span data-stu-id="4aad3-119">If this value returns TRUE, call **SaveChanges** at some point to make the update permanent.</span></span> <span data-ttu-id="4aad3-120">Вызов необязательно должен быть выполнен сразу после возврата **ртфсинк** .</span><span class="sxs-lookup"><span data-stu-id="4aad3-120">The call does not have to be made immediately after **RTFSync** returns.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4aad3-121">Так как многие компоненты обрабатывают форматированный текст перед его получением, существует вероятность повреждения.</span><span class="sxs-lookup"><span data-stu-id="4aad3-121">Because so many components handle the formatted text before you receive it, there is the possibility of corruption.</span></span> <span data-ttu-id="4aad3-122">Это может происходить из поставщика хранилища сообщений, стороннего приложения, шлюза или ошибки передачи.</span><span class="sxs-lookup"><span data-stu-id="4aad3-122">This corruption could come from the message store provider, a third party application, a gateway, or a transmission error.</span></span> 
  

