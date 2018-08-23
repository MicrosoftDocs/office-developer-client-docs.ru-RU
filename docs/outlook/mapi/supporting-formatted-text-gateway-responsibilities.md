---
title: Поддержка обязанности шлюза форматированного текста
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d369093589ffad03bf087b02905c443cf6f46c34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564271"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a><span data-ttu-id="5238f-103">Поддержка форматированного текста: обязанности шлюза</span><span class="sxs-lookup"><span data-stu-id="5238f-103">Supporting Formatted Text: Gateway Responsibilities</span></span>

  
  
<span data-ttu-id="5238f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5238f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="5238f-105">**Для обработки формат RTF для исходящих сообщений, шлюзов**</span><span class="sxs-lookup"><span data-stu-id="5238f-105">**To handle Rich Text Format for outgoing messages, gateways**</span></span>
  
1. <span data-ttu-id="5238f-106">Извлечение только свойство message **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) из хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="5238f-106">Retrieve only a message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property from the message store.</span></span> <span data-ttu-id="5238f-107">Основное преимущество для извлечения только свойство **PR_RTF_COMPRESSED** — это, что текста сообщения не обязательно должна отправляться между компьютерами, если существует шлюз и хранилища сообщений на разных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="5238f-107">The main advantage in retrieving only the **PR_RTF_COMPRESSED** property is that the message text does not need to be sent between machines if the gateway and the message store exist on different machines.</span></span> 
    
2. <span data-ttu-id="5238f-108">Создание текста сообщения из форматированный текст, либо с помощью вызова функции библиотека RTF **HrTextFromCompressedRTFStream** или, если сообщение хранятся **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="5238f-108">Generate the message text from the formatted text either by calling the RTF library function **HrTextFromCompressedRTFStream** or, if the message is stored locally, **RTFSync**.</span></span> <span data-ttu-id="5238f-109">Флаг RTF_SYNC_RTF_CHANGED должен быть установлен в вызове **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="5238f-109">The RTF_SYNC_RTF_CHANGED flag should be set in the call to **RTFSync**.</span></span> <span data-ttu-id="5238f-110">Для получения дополнительных сведений см [RTFSync](rtfsync.md).</span><span class="sxs-lookup"><span data-stu-id="5238f-110">For more information, see [RTFSync](rtfsync.md).</span></span>
    
3. <span data-ttu-id="5238f-111">Любые изменения нельзя обратить к тексту сообщения, например удаление неподдерживаемые символы.</span><span class="sxs-lookup"><span data-stu-id="5238f-111">Make any irreversible modifications to the message text, such as dropping unsupported characters.</span></span> 
    
4. <span data-ttu-id="5238f-112">Убедитесь, что **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) и все свойства auxilliary RTF — либо набор или отсутствует.</span><span class="sxs-lookup"><span data-stu-id="5238f-112">Ensure that both **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) and all of the RTF auxilliary properties are either set or absent.</span></span>
    
5. <span data-ttu-id="5238f-113">После внесения каких-либо изменений вызовов **RTFSync** с набором флаги RTF_SYNC_RTF_CHANGED и RTF_SYNC_BODY_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="5238f-113">If any modifications were made, call **RTFSync** with both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags set.</span></span> <span data-ttu-id="5238f-114">**RTFSync** будет пересчитывать свойства auxilliary RTF из измененного текста.</span><span class="sxs-lookup"><span data-stu-id="5238f-114">**RTFSync** will recalculate the RTF auxilliary properties from the modified text.</span></span> 
    
6. <span data-ttu-id="5238f-115">Любые изменения reversable текста сообщения, такие как вставка заполнители вложения и выполняется преобразование обратимое кодовой страницы.</span><span class="sxs-lookup"><span data-stu-id="5238f-115">Make any reversable modifications to the message text, such as inserting attachment placeholders and performing nondestructive code page conversions.</span></span>
    
7. <span data-ttu-id="5238f-116">Отправьте сообщение.</span><span class="sxs-lookup"><span data-stu-id="5238f-116">Send the message.</span></span>
    
 <span data-ttu-id="5238f-117">**Для обработки формат RTF для входящих сообщений, шлюзов**</span><span class="sxs-lookup"><span data-stu-id="5238f-117">**To handle Rich Text Format for incoming messages, gateways**</span></span>
  
1. <span data-ttu-id="5238f-118">Обратные каких-либо изменений текста сообщения, которые были внесены непосредственно перед отправкой сообщения.</span><span class="sxs-lookup"><span data-stu-id="5238f-118">Reverse any message text modifications that were made directly before the message was sent.</span></span> 
    
2. <span data-ttu-id="5238f-119">Вызовите **RTFSync** , если сообщение содержит свойства **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) и **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="5238f-119">Call **RTFSync** if the message contains both the **PR_RTF_COMPRESSED** and **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) properties.</span></span> 
    
3. <span data-ttu-id="5238f-120">Обновить сообщения в хранилище сообщений с помощью свойства **PR_RTF_COMPRESSED** , если сообщение содержит обновление с помощью свойства **PR_BODY** только в том случае, если отсутствует **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="5238f-120">Update the message in the message store with the **PR_RTF_COMPRESSED** property if the message contains it; update with the **PR_BODY** property only if **PR_RTF_COMPRESSED** is absent.</span></span> 
    
4. <span data-ttu-id="5238f-121">Отменить **PR_BODY** , если сообщение содержит то, как это свойство, так и для **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="5238f-121">Discard **PR_BODY** if the message contains both this property and **PR_RTF_COMPRESSED**.</span></span>
    
<span data-ttu-id="5238f-122">Шлюзы вызовите **RTFSync** , чтобы избежать передачи текста сообщения и форматированный текст, если хранилище сообщений на другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="5238f-122">Gateways call **RTFSync** to avoid transmitting both the message text and formatted text if the message store is on a different machine.</span></span> <span data-ttu-id="5238f-123">Если шлюз является локальным, его эти свойства и разрешить хранилище сообщений синхронизации.</span><span class="sxs-lookup"><span data-stu-id="5238f-123">If the gateway is local, it can set both properties and allow the message store to perform the synchronization.</span></span> 
  

