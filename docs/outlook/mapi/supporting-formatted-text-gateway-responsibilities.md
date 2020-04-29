---
title: Поддержка функциональных обязанностей для шлюза форматированного текста
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
# <a name="supporting-formatted-text-gateway-responsibilities"></a><span data-ttu-id="47ca2-103">Поддержка форматированного текста: обязанности шлюза</span><span class="sxs-lookup"><span data-stu-id="47ca2-103">Supporting Formatted Text: Gateway Responsibilities</span></span>

  
  
<span data-ttu-id="47ca2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47ca2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="47ca2-105">**Для обработки форматированного текста исходящих сообщений шлюзы**</span><span class="sxs-lookup"><span data-stu-id="47ca2-105">**To handle Rich Text Format for outgoing messages, gateways**</span></span>
  
1. <span data-ttu-id="47ca2-106">Получение только свойства **PR_RTF_COMPRESSED** сообщения ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) из хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="47ca2-106">Retrieve only a message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property from the message store.</span></span> <span data-ttu-id="47ca2-107">Основное преимущество получения только свойства **PR_RTF_COMPRESSED** состоит в том, что текст сообщения не должен передаваться между машинами, если шлюз и хранилище сообщений существуют на разных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="47ca2-107">The main advantage in retrieving only the **PR_RTF_COMPRESSED** property is that the message text does not need to be sent between machines if the gateway and the message store exist on different machines.</span></span> 
    
2. <span data-ttu-id="47ca2-108">Создайте текст сообщения из форматированного текста, вызвав функцию библиотеки RTF **хртекстфромкомпресседртфстреам** или, если сообщение хранится локально, **ртфсинк**.</span><span class="sxs-lookup"><span data-stu-id="47ca2-108">Generate the message text from the formatted text either by calling the RTF library function **HrTextFromCompressedRTFStream** or, if the message is stored locally, **RTFSync**.</span></span> <span data-ttu-id="47ca2-109">Флаг RTF_SYNC_RTF_CHANGED должен быть установлен в вызове **ртфсинк**.</span><span class="sxs-lookup"><span data-stu-id="47ca2-109">The RTF_SYNC_RTF_CHANGED flag should be set in the call to **RTFSync**.</span></span> <span data-ttu-id="47ca2-110">Дополнительные сведения см. в разделе [ртфсинк](rtfsync.md).</span><span class="sxs-lookup"><span data-stu-id="47ca2-110">For more information, see [RTFSync](rtfsync.md).</span></span>
    
3. <span data-ttu-id="47ca2-111">Внесите необратимые изменения в текст сообщения, например при удалении неподдерживаемых символов.</span><span class="sxs-lookup"><span data-stu-id="47ca2-111">Make any irreversible modifications to the message text, such as dropping unsupported characters.</span></span> 
    
4. <span data-ttu-id="47ca2-112">Убедитесь, что **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) и все свойства RTF ауксиллиари установлены или отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="47ca2-112">Ensure that both **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) and all of the RTF auxilliary properties are either set or absent.</span></span>
    
5. <span data-ttu-id="47ca2-113">При внесении любых изменений вызовите **ртфсинк** с набором флагов RTF_SYNC_RTF_CHANGED и RTF_SYNC_BODY_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="47ca2-113">If any modifications were made, call **RTFSync** with both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags set.</span></span> <span data-ttu-id="47ca2-114">**Ртфсинк** будет пересчитывать свойства RTF ауксиллиари из измененного текста.</span><span class="sxs-lookup"><span data-stu-id="47ca2-114">**RTFSync** will recalculate the RTF auxilliary properties from the modified text.</span></span> 
    
6. <span data-ttu-id="47ca2-115">Внесите в текст сообщения все обратимые изменения, такие как вставка заполнители вложения и выполнение необратимых преобразований кодовых страниц.</span><span class="sxs-lookup"><span data-stu-id="47ca2-115">Make any reversable modifications to the message text, such as inserting attachment placeholders and performing nondestructive code page conversions.</span></span>
    
7. <span data-ttu-id="47ca2-116">Отправьте сообщение.</span><span class="sxs-lookup"><span data-stu-id="47ca2-116">Send the message.</span></span>
    
 <span data-ttu-id="47ca2-117">**Для обработки сообщений в формате RTF для входящих сообщений шлюзы**</span><span class="sxs-lookup"><span data-stu-id="47ca2-117">**To handle Rich Text Format for incoming messages, gateways**</span></span>
  
1. <span data-ttu-id="47ca2-118">Отмените все изменения текста сообщения, сделанные непосредственно перед отправкой сообщения.</span><span class="sxs-lookup"><span data-stu-id="47ca2-118">Reverse any message text modifications that were made directly before the message was sent.</span></span> 
    
2. <span data-ttu-id="47ca2-119">Вызовите **ртфсинк** , если сообщение содержит свойства **PR_RTF_COMPRESSED** и **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="47ca2-119">Call **RTFSync** if the message contains both the **PR_RTF_COMPRESSED** and **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) properties.</span></span> 
    
3. <span data-ttu-id="47ca2-120">Обновление сообщения в хранилище сообщений с помощью свойства **PR_RTF_COMPRESSED** , если оно содержится в сообщении; обновление со свойством **PR_BODY** только в том случае, если **PR_RTF_COMPRESSED** отсутствует.</span><span class="sxs-lookup"><span data-stu-id="47ca2-120">Update the message in the message store with the **PR_RTF_COMPRESSED** property if the message contains it; update with the **PR_BODY** property only if **PR_RTF_COMPRESSED** is absent.</span></span> 
    
4. <span data-ttu-id="47ca2-121">Удалить **PR_BODY** , если сообщение содержит и это свойство, и **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="47ca2-121">Discard **PR_BODY** if the message contains both this property and **PR_RTF_COMPRESSED**.</span></span>
    
<span data-ttu-id="47ca2-122">Шлюзы вызывают **ртфсинк** , чтобы избежать передачи текста сообщения и форматированного текста, если хранилище сообщений находится на другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="47ca2-122">Gateways call **RTFSync** to avoid transmitting both the message text and formatted text if the message store is on a different machine.</span></span> <span data-ttu-id="47ca2-123">Если шлюз является локальным, он может задать оба свойства и разрешить хранилищу сообщений выполнение синхронизации.</span><span class="sxs-lookup"><span data-stu-id="47ca2-123">If the gateway is local, it can set both properties and allow the message store to perform the synchronization.</span></span> 
  

