---
title: Поддержка отформатированный текст в входящих сообщениях клиентские обязанности
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
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a><span data-ttu-id="08581-103">Поддержка форматного текста в входящих сообщениях: клиентские обязанности</span><span class="sxs-lookup"><span data-stu-id="08581-103">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="08581-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08581-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08581-105">По мере передачи сообщений между системами обмена сообщениями spooler MAPI позволяет синхронизировать форматирование текста с текстом сообщения.</span><span class="sxs-lookup"><span data-stu-id="08581-105">As messages are transferred between messaging systems, the MAPI spooler makes sure that the rich text formatting remains synchronized with the message text.</span></span> <span data-ttu-id="08581-106">Spooler MAPI вызывает [функцию RTFSync](rtfsync.md) из завернутой версии сообщения, которое передается поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="08581-106">The MAPI spooler calls the [RTFSync](rtfsync.md) function from within a wrapped version of the message that it passes to the transport provider.</span></span> <span data-ttu-id="08581-107">Поставщик транспорта сохраняет изменения, внесенные в сообщение, вызывая [метод IMAPIProp::SaveChanges,](imapiprop-savechanges.md) а затем передает его новому получателю.</span><span class="sxs-lookup"><span data-stu-id="08581-107">The transport provider saves the changes made to the message by calling the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and then routes it to the new recipient.</span></span> 
  
<span data-ttu-id="08581-108">Когда клиентное приложение получателя с RTF открывает сообщение для отображения текста, оно должно синхронизировать текст с форматированием и открыть либо **PR_RTF_COMPRESSED** [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)или **PR_BODY** [(PidTagBody),](pidtagbody-canonical-property.md)в зависимости от того, какое свойство доступно.</span><span class="sxs-lookup"><span data-stu-id="08581-108">When the recipient's RTF-aware client application opens the message to display the text, it must synchronize the text with the formatting and open either **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), depending on which property is available.</span></span>
  
 <span data-ttu-id="08581-109">**Чтобы открыть сообщение, клиенты, осведомленные о RTF**</span><span class="sxs-lookup"><span data-stu-id="08581-109">**To open a message, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="08581-110">Позвоните **в RTFSync,** чтобы синхронизировать текст сообщения с форматированием, если хранилище сообщений не знает RTF.</span><span class="sxs-lookup"><span data-stu-id="08581-110">Call **RTFSync** to synchronize the message text with the formatting if the message store is not RTF-aware.</span></span> <span data-ttu-id="08581-111">Флаг RTF_SYNC_BODY_CHANGED должен быть передан в _параметре ulFlags,_ если свойство [PR_RTF_IN_SYNC (PidTagRtfInSync)](pidtagrtfinsync-canonical-property.md)отсутствует или настроено на FALSE. </span><span class="sxs-lookup"><span data-stu-id="08581-111">The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE.</span></span> <span data-ttu-id="08581-112">Клиенты, работающие с RTF-магазинами сообщений, не должны вызывать **RTFSync,** так как магазин сообщений позаботится об этом.</span><span class="sxs-lookup"><span data-stu-id="08581-112">Clients working with RTF-aware message stores need not make the **RTFSync** call because the message store takes care of it.</span></span> 
    
2. <span data-ttu-id="08581-113">Вызов [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) если текст сообщения обновлен.</span><span class="sxs-lookup"><span data-stu-id="08581-113">Call [IMAPIProp::SaveChanges](imapiprop-savechanges.md) if the message text has been updated.</span></span> 
    
3. <span data-ttu-id="08581-114">Чтобы открыть свойство PR_RTF_COMPRESSED, позвоните в [IMAPIProp::OpenProperty.](imapiprop-openproperty.md) </span><span class="sxs-lookup"><span data-stu-id="08581-114">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="08581-115">Если **PR_RTF_COMPRESSED** недоступна, необходимо открыть свойство **PR_BODY** для отображения контента сообщения.</span><span class="sxs-lookup"><span data-stu-id="08581-115">If **PR_RTF_COMPRESSED** is not available, you should open the **PR_BODY** property instead to display the message content.</span></span> 
    
4. <span data-ttu-id="08581-116">Вызов [функции WrapCompressedRTFStream](wrapcompressedrtfstream.md) для создания некомпрессивной версии сжатых данных RTF, если это доступно.</span><span class="sxs-lookup"><span data-stu-id="08581-116">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function to create an uncompressed version of the compressed RTF data, if available.</span></span> 
    
5. <span data-ttu-id="08581-117">Отображение пользователю незапечатаных данных RTF или обычных текстовых данных.</span><span class="sxs-lookup"><span data-stu-id="08581-117">Display the uncompressed RTF data or the plain text data to the user.</span></span>
    
 <span data-ttu-id="08581-118">**RTFSync** возвращает значение Boolean, которое указывает, обновлено ли сообщение.</span><span class="sxs-lookup"><span data-stu-id="08581-118">**RTFSync** returns a Boolean value that indicates whether or not the message has been updated.</span></span> <span data-ttu-id="08581-119">Если это значение возвращает ЗНАЧЕНИЕ TRUE, в какой-то момент позвоните **в SaveChanges,** чтобы сделать обновление постоянным.</span><span class="sxs-lookup"><span data-stu-id="08581-119">If this value returns TRUE, call **SaveChanges** at some point to make the update permanent.</span></span> <span data-ttu-id="08581-120">Вызов не должен быть выполнен сразу после **возвращения RTFSync.**</span><span class="sxs-lookup"><span data-stu-id="08581-120">The call does not have to be made immediately after **RTFSync** returns.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="08581-121">Поскольку перед его получением многие компоненты обрабатывают отформатированный текст, существует вероятность повреждения.</span><span class="sxs-lookup"><span data-stu-id="08581-121">Because so many components handle the formatted text before you receive it, there is the possibility of corruption.</span></span> <span data-ttu-id="08581-122">Эта коррупция может происходить от поставщика магазина сообщений, сторонних приложений, шлюза или ошибки передачи.</span><span class="sxs-lookup"><span data-stu-id="08581-122">This corruption could come from the message store provider, a third party application, a gateway, or a transmission error.</span></span> 
  

