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
ms.openlocfilehash: 3e65ebd3ea485ca54978d622e8aaf093dc5eff74
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594070"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a><span data-ttu-id="b17bf-103">Поддержка текста в формате RTF для поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="b17bf-103">Supporting RTF Text for Message Store Providers</span></span>

  
  
<span data-ttu-id="b17bf-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b17bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b17bf-105">Некоторые клиентские приложения позволяет пользователю использовать форматированный текст (RTF) текст в сообщения.</span><span class="sxs-lookup"><span data-stu-id="b17bf-105">Some client applications allow users to use Rich Text Format (RTF) text in their messages.</span></span> <span data-ttu-id="b17bf-106">Если сообщение хранения поставщика должно поддерживать текст RTF в сообщениях, он должен обрабатывать свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), в дополнение к свойству **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b17bf-106">If your message store provider needs to support RTF text in messages, it needs to handle the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, in addition to the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span> <span data-ttu-id="b17bf-107">Прежде всего это означает, что хранения обоих свойств и проверьте, что **PR_BODY** содержит текстовая версия текста в **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="b17bf-107">Primarily, this means storing both properties, and making sure that **PR_BODY** contains a plain text version of the text in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="b17bf-108">Функция [RTFSync](rtfsync.md) используется для этой цели.</span><span class="sxs-lookup"><span data-stu-id="b17bf-108">The [RTFSync](rtfsync.md) function is useful for this purpose.</span></span> 
  
<span data-ttu-id="b17bf-109">Существует два флаги, которые можно задать в свойстве **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) объекта хранилища сообщений, которые сообщают клиентов, их можно ожидать от поставщика хранилища сообщений по отношению к **PR_BODY** и **PR_ RTF_COMPRESSED** свойства сообщения в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="b17bf-109">There are two flags that can be set in the message store object's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property that tell clients what they can expect from the message store provider with respect to the **PR_BODY** and **PR_RTF_COMPRESSED** properties on messages in the message store.</span></span> <span data-ttu-id="b17bf-110">Флаг STORE_RTF_OK указывает, что хранилище можно создать значение свойства **PR_BODY** из свойства **PR_RTF_COMPRESSED** динамически, что уменьшает клиентов от необходимости их явным образом синхронизация.</span><span class="sxs-lookup"><span data-stu-id="b17bf-110">The STORE_RTF_OK flag indicates that the store can generate the value of the **PR_BODY** property from the **PR_RTF_COMPRESSED** property dynamically, which relieves clients from the burden of synchronizing them explicitly.</span></span> <span data-ttu-id="b17bf-111">Флаг STORE_UNCOMPRESSED_RTF указывает, что поставщик хранения сообщений может поддерживать несжатую данных в **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="b17bf-111">The STORE_UNCOMPRESSED_RTF flag indicates that the message store provider can support uncompressed data in **PR_RTF_COMPRESSED**.</span></span>
  
<span data-ttu-id="b17bf-112">Необходимо удалить свойство **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), чтобы должным образом взаимодействовать с клиентскими приложениями, которые поддерживают текст RTF при изменении свойства **PR_BODY** поставщиков хранилища сообщений, которые не поддерживают текст RTF .</span><span class="sxs-lookup"><span data-stu-id="b17bf-112">Message store providers that do not support RTF text need to delete the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property when the **PR_BODY** property changes in order to interoperate properly with client applications that do support RTF text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b17bf-113">См. также</span><span class="sxs-lookup"><span data-stu-id="b17bf-113">See also</span></span>



[<span data-ttu-id="b17bf-114">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="b17bf-114">Message Store Features</span></span>](message-store-features.md)

