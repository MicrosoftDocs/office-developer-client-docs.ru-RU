---
title: Поддержка текста в формате RTF для поставщиков хранилищ сообщений
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
# <a name="supporting-rtf-text-for-message-store-providers"></a><span data-ttu-id="fb001-103">Поддержка текста в формате RTF для поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="fb001-103">Supporting RTF Text for Message Store Providers</span></span>

  
  
<span data-ttu-id="fb001-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb001-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb001-105">Некоторые клиентские приложения позволяют пользователям использовать текст в формате RTF в своих сообщениях.</span><span class="sxs-lookup"><span data-stu-id="fb001-105">Some client applications allow users to use Rich Text Format (RTF) text in their messages.</span></span> <span data-ttu-id="fb001-106">Если поставщик хранилища сообщений должен поддерживать Текст RTF в сообщениях, необходимо обработать свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) в дополнение к свойству **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fb001-106">If your message store provider needs to support RTF text in messages, it needs to handle the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, in addition to the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span> <span data-ttu-id="fb001-107">В основном это означает хранение обоих свойств и обеспечение того, что **PR_BODY** содержит текстовую версию текста в **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="fb001-107">Primarily, this means storing both properties, and making sure that **PR_BODY** contains a plain text version of the text in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="fb001-108">Для этой цели удобно использовать функцию [ртфсинк](rtfsync.md) .</span><span class="sxs-lookup"><span data-stu-id="fb001-108">The [RTFSync](rtfsync.md) function is useful for this purpose.</span></span> 
  
<span data-ttu-id="fb001-109">Существует два флага, которые можно задать в свойстве **PR_STORE_SUPPORT_MASK** объекта хранилища сообщений ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), которые сообщают клиентам, что они могут ожидать от поставщика хранилища сообщений относительно свойств **PR_BODY** и **PR_RTF_COMPRESSED** в сообщениях в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="fb001-109">There are two flags that can be set in the message store object's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property that tell clients what they can expect from the message store provider with respect to the **PR_BODY** and **PR_RTF_COMPRESSED** properties on messages in the message store.</span></span> <span data-ttu-id="fb001-110">Флаг STORE_RTF_OK указывает на то, что хранилище может динамически создавать значение свойства **PR_BODY** из свойства **PR_RTF_COMPRESSED** , что освобождает клиенты от нагрузки для их синхронизации явным образом.</span><span class="sxs-lookup"><span data-stu-id="fb001-110">The STORE_RTF_OK flag indicates that the store can generate the value of the **PR_BODY** property from the **PR_RTF_COMPRESSED** property dynamically, which relieves clients from the burden of synchronizing them explicitly.</span></span> <span data-ttu-id="fb001-111">Флаг STORE_UNCOMPRESSED_RTF указывает, что поставщик хранилища сообщений может поддерживать несжатые данные в **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="fb001-111">The STORE_UNCOMPRESSED_RTF flag indicates that the message store provider can support uncompressed data in **PR_RTF_COMPRESSED**.</span></span>
  
<span data-ttu-id="fb001-112">Поставщики хранилищ сообщений, не поддерживающие текст RTF, должны удалить свойство **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) при изменении свойства **PR_BODY** , чтобы обеспечить правильное взаимодействие с клиентскими приложениями, поддерживающими текст RTF.</span><span class="sxs-lookup"><span data-stu-id="fb001-112">Message store providers that do not support RTF text need to delete the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property when the **PR_BODY** property changes in order to interoperate properly with client applications that do support RTF text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fb001-113">См. также</span><span class="sxs-lookup"><span data-stu-id="fb001-113">See also</span></span>



[<span data-ttu-id="fb001-114">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="fb001-114">Message Store Features</span></span>](message-store-features.md)

