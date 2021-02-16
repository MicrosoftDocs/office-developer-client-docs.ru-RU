---
title: Поддержка обязанностей отформатированный текстовый шлюз
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d5c3480018be399a85ee0bfda7ce1ff9b701cecc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419431"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a><span data-ttu-id="dd441-103">Поддержка форматированный текст: обязанности шлюза</span><span class="sxs-lookup"><span data-stu-id="dd441-103">Supporting Formatted Text: Gateway Responsibilities</span></span>

  
  
<span data-ttu-id="dd441-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd441-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="dd441-105">**Обработка RICH Text Format для исходяющих сообщений, шлюзов**</span><span class="sxs-lookup"><span data-stu-id="dd441-105">**To handle Rich Text Format for outgoing messages, gateways**</span></span>
  
1. <span data-ttu-id="dd441-106">Извлекать только свойство PR_RTF_COMPRESSED **сообщения** ([PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)из хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="dd441-106">Retrieve only a message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property from the message store.</span></span> <span data-ttu-id="dd441-107">Основное преимущество при искомом  только свойстве PR_RTF_COMPRESSED заключается в том, что текст сообщения не требуется отправлять между компьютерами, если шлюз и хранилище сообщений существуют на разных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="dd441-107">The main advantage in retrieving only the **PR_RTF_COMPRESSED** property is that the message text does not need to be sent between machines if the gateway and the message store exist on different machines.</span></span> 
    
2. <span data-ttu-id="dd441-108">Сгенерирование текста сообщения из форматированный текст либо путем вызова функции библиотеки RTF **HrTextFromCompressedRTFStream** или, если сообщение хранится локально, **RTFSync**.</span><span class="sxs-lookup"><span data-stu-id="dd441-108">Generate the message text from the formatted text either by calling the RTF library function **HrTextFromCompressedRTFStream** or, if the message is stored locally, **RTFSync**.</span></span> <span data-ttu-id="dd441-109">Флаг RTF_SYNC_RTF_CHANGED должен быть установлен в вызове **RTFSync.**</span><span class="sxs-lookup"><span data-stu-id="dd441-109">The RTF_SYNC_RTF_CHANGED flag should be set in the call to **RTFSync**.</span></span> <span data-ttu-id="dd441-110">Дополнительные сведения см. в [RTFSync.](rtfsync.md)</span><span class="sxs-lookup"><span data-stu-id="dd441-110">For more information, see [RTFSync](rtfsync.md).</span></span>
    
3. <span data-ttu-id="dd441-111">Внести любые необратимые изменения в текст сообщения, например отбросить неподтверченные символы.</span><span class="sxs-lookup"><span data-stu-id="dd441-111">Make any irreversible modifications to the message text, such as dropping unsupported characters.</span></span> 
    
4. <span data-ttu-id="dd441-112">Убедитесь, **что** PR_RTF_IN_SYNC ([PidTagRtfInSync)](pidtagrtfinsync-canonical-property.md)и все вспомогательные свойства RTF либо заданы, либо отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="dd441-112">Ensure that both **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) and all of the RTF auxilliary properties are either set or absent.</span></span>
    
5. <span data-ttu-id="dd441-113">Если были внесены какие-либо изменения, вызовите **RTFSync** с установленными RTF_SYNC_RTF_CHANGED и RTF_SYNC_BODY_CHANGED флагами.</span><span class="sxs-lookup"><span data-stu-id="dd441-113">If any modifications were made, call **RTFSync** with both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags set.</span></span> <span data-ttu-id="dd441-114">**RTFSync** пересчитает вспомогательные свойства RTF из измененного текста.</span><span class="sxs-lookup"><span data-stu-id="dd441-114">**RTFSync** will recalculate the RTF auxilliary properties from the modified text.</span></span> 
    
6. <span data-ttu-id="dd441-115">Внести любые обратимые изменения в текст сообщения, такие как вставка вложений и выполнение недеструкционных преобразований страницы кода.</span><span class="sxs-lookup"><span data-stu-id="dd441-115">Make any reversable modifications to the message text, such as inserting attachment placeholders and performing nondestructive code page conversions.</span></span>
    
7. <span data-ttu-id="dd441-116">Отправьте сообщение.</span><span class="sxs-lookup"><span data-stu-id="dd441-116">Send the message.</span></span>
    
 <span data-ttu-id="dd441-117">**Обработка формата RICH Text для входящих сообщений шлюзами**</span><span class="sxs-lookup"><span data-stu-id="dd441-117">**To handle Rich Text Format for incoming messages, gateways**</span></span>
  
1. <span data-ttu-id="dd441-118">Отменять любые изменения текста сообщения, сделанные непосредственно перед его отправлением.</span><span class="sxs-lookup"><span data-stu-id="dd441-118">Reverse any message text modifications that were made directly before the message was sent.</span></span> 
    
2. <span data-ttu-id="dd441-119">Вызовите **RTFSync,** если  сообщение содержит свойства PR_RTF_COMPRESSED **и PR_BODY** ([PidTagBody).](pidtagbody-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="dd441-119">Call **RTFSync** if the message contains both the **PR_RTF_COMPRESSED** and **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) properties.</span></span> 
    
3. <span data-ttu-id="dd441-120">Обновив сообщение в хранилище сообщений с **помощью свойства PR_RTF_COMPRESSED,** если сообщение содержит его; обновление с помощью **PR_BODY,** только **если** PR_RTF_COMPRESSED отсутствует.</span><span class="sxs-lookup"><span data-stu-id="dd441-120">Update the message in the message store with the **PR_RTF_COMPRESSED** property if the message contains it; update with the **PR_BODY** property only if **PR_RTF_COMPRESSED** is absent.</span></span> 
    
4. <span data-ttu-id="dd441-121">Отменить **PR_BODY,** если сообщение содержит как это свойство, так **и PR_RTF_COMPRESSED.**</span><span class="sxs-lookup"><span data-stu-id="dd441-121">Discard **PR_BODY** if the message contains both this property and **PR_RTF_COMPRESSED**.</span></span>
    
<span data-ttu-id="dd441-122">Шлюзы **звонят по RTFSync,** чтобы избежать передачи текста сообщения и форматированный текст, если хранилище сообщений находится на другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="dd441-122">Gateways call **RTFSync** to avoid transmitting both the message text and formatted text if the message store is on a different machine.</span></span> <span data-ttu-id="dd441-123">Если шлюз локальный, он может установить оба свойства и разрешить синхронизацию с хранилищем сообщений.</span><span class="sxs-lookup"><span data-stu-id="dd441-123">If the gateway is local, it can set both properties and allow the message store to perform the synchronization.</span></span> 
  

