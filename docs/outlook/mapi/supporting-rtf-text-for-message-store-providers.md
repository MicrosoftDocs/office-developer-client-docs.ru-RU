---
title: Поддержка текста RTF для поставщиков магазинов сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: dc1d8a5e237b7b34f3a57e9789e03e2f16237764
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414216"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a><span data-ttu-id="57ec7-103">Поддержка текста RTF для поставщиков магазинов сообщений</span><span class="sxs-lookup"><span data-stu-id="57ec7-103">Supporting RTF Text for Message Store Providers</span></span>

  
  
<span data-ttu-id="57ec7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57ec7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57ec7-105">Некоторые клиентские приложения позволяют пользователям использовать текст Rich Text Format (RTF) в своих сообщениях.</span><span class="sxs-lookup"><span data-stu-id="57ec7-105">Some client applications allow users to use Rich Text Format (RTF) text in their messages.</span></span> <span data-ttu-id="57ec7-106">Если поставщику хранения сообщений необходимо поддерживать текст RTF в сообщениях, ему необходимо обрабатывать свойство **PR_RTF_COMPRESSED** [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)в дополнение к свойству **PR_BODY** [(PidTagBody).](pidtagbody-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="57ec7-106">If your message store provider needs to support RTF text in messages, it needs to handle the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, in addition to the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span> <span data-ttu-id="57ec7-107">В первую очередь это означает хранение обоих свойств и обеспечение того, чтобы PR_BODY содержит простую текстовую версию текста в **PR_RTF_COMPRESSED**. </span><span class="sxs-lookup"><span data-stu-id="57ec7-107">Primarily, this means storing both properties, and making sure that **PR_BODY** contains a plain text version of the text in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="57ec7-108">Функция [RTFSync](rtfsync.md) полезна для этой цели.</span><span class="sxs-lookup"><span data-stu-id="57ec7-108">The [RTFSync](rtfsync.md) function is useful for this purpose.</span></span> 
  
<span data-ttu-id="57ec7-109">В свойстве PR_STORE_SUPPORT_MASK объекта магазина сообщений [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)можно установить два флага, которые расскажут клиентам, чего они  могут ожидать от поставщика хранения сообщений в отношении свойств PR_BODY и **PR_RTF_COMPRESSED** сообщений в хранилище сообщений. </span><span class="sxs-lookup"><span data-stu-id="57ec7-109">There are two flags that can be set in the message store object's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property that tell clients what they can expect from the message store provider with respect to the **PR_BODY** and **PR_RTF_COMPRESSED** properties on messages in the message store.</span></span> <span data-ttu-id="57ec7-110">Флаг STORE_RTF_OK указывает, что хранилище может динамически генерировать  значение свойства PR_BODY  из свойства PR_RTF_COMPRESSED, что освобождает клиентов от нагрузки на их явное синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="57ec7-110">The STORE_RTF_OK flag indicates that the store can generate the value of the **PR_BODY** property from the **PR_RTF_COMPRESSED** property dynamically, which relieves clients from the burden of synchronizing them explicitly.</span></span> <span data-ttu-id="57ec7-111">Флаг STORE_UNCOMPRESSED_RTF указывает, что поставщик магазина сообщений может поддерживать незапечатаные данные **в PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="57ec7-111">The STORE_UNCOMPRESSED_RTF flag indicates that the message store provider can support uncompressed data in **PR_RTF_COMPRESSED**.</span></span>
  
<span data-ttu-id="57ec7-112">Поставщики магазинов сообщений, которые не поддерживают текст RTF, должны удалить свойство[PR_RTF_IN_SYNC (PidTagRtfInSync)](pidtagrtfinsync-canonical-property.md)при изменениях свойства PR_BODY, чтобы должным образом скооперироваться с клиентские приложения, поддерживают текст RTF.  </span><span class="sxs-lookup"><span data-stu-id="57ec7-112">Message store providers that do not support RTF text need to delete the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property when the **PR_BODY** property changes in order to interoperate properly with client applications that do support RTF text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="57ec7-113">См. также</span><span class="sxs-lookup"><span data-stu-id="57ec7-113">See also</span></span>



[<span data-ttu-id="57ec7-114">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="57ec7-114">Message Store Features</span></span>](message-store-features.md)

