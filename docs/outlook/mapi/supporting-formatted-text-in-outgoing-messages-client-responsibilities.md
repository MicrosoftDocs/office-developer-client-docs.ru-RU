---
title: Поддержка форматированный текст в обязанности клиента исходящих сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 975dd172b6ad342351f014d0966d62a150f713c6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571292"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a><span data-ttu-id="97d31-103">Поддержка форматированного текста в исходящих сообщениях: обязанности клиентов</span><span class="sxs-lookup"><span data-stu-id="97d31-103">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="97d31-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97d31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97d31-105">Клиентские приложения задать свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) или свойство **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) для исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="97d31-105">Client applications set the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, or the **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) property for an outgoing message.</span></span> <span data-ttu-id="97d31-106">Клиенты, которые поддерживают только обычного текста для свойства только **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="97d31-106">Clients that support only plain text set only the **PR_BODY** property.</span></span> <span data-ttu-id="97d31-107">Текст в формате RTF (RTF)-принять во внимание, клиенты могут установить **PR_BODY** и **PR_RTF_COMPRESSED** свойства, или только **PR_RTF_COMPRESSED**, в зависимости от сообщения сохраняются используемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="97d31-107">Rich Text Format (RTF)-aware clients might set both **PR_BODY** and **PR_RTF_COMPRESSED** properties, or only **PR_RTF_COMPRESSED**, depending on the message store provider being used.</span></span> <span data-ttu-id="97d31-108">Клиенты с поддержкой HTML необходимо задать свойство **PR_HTML** .</span><span class="sxs-lookup"><span data-stu-id="97d31-108">HTML-aware clients set the **PR_HTML** property.</span></span> 
  
<span data-ttu-id="97d31-109">Важно, чтобы клиент мог свойство **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) хранилища сообщений, чтобы определить, поддерживает ли хранилище RTF.</span><span class="sxs-lookup"><span data-stu-id="97d31-109">It is important for a client to check its message store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to determine whether the store supports RTF.</span></span> <span data-ttu-id="97d31-110">Если хранилище сообщений не принять во внимание RTF, поддерживающую RTF клиента задает свойства как **PR_BODY** , так и **PR_RTF_COMPRESSED** для всех исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="97d31-110">If the message store is not RTF-aware, an RTF-aware client sets both the **PR_BODY** and **PR_RTF_COMPRESSED** properties for each outgoing message.</span></span> 
  
<span data-ttu-id="97d31-111">Если принять во внимание RTF хранилища сообщений, только свойство **PR_RTF_COMPRESSED** необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="97d31-111">If the message store is RTF-aware, only the **PR_RTF_COMPRESSED** property needs to be set.</span></span> 
  
 <span data-ttu-id="97d31-112">**Для задания PR_RTF_COMPRESSED и убедитесь, что синхронизация процесса возникает при необходимости, поддерживающую RTF клиентов**</span><span class="sxs-lookup"><span data-stu-id="97d31-112">**To set PR_RTF_COMPRESSED and ensure that the synchronization process occurs as necessary, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="97d31-113">Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для открытия установки флаги MAPI_CREATE и MAPI_MODIFY свойства **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="97d31-113">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, setting both the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="97d31-114">MAPI_CREATE гарантирует, что все новые данные заменяет все старые данные и MAPI_MODIFY позволяет выполнять их замены.</span><span class="sxs-lookup"><span data-stu-id="97d31-114">MAPI_CREATE ensures that any new data replaces any old data and MAPI_MODIFY enables you to make those replacements.</span></span> 
    
2. <span data-ttu-id="97d31-115">Вызовите функцию [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , передав STORE_UNCOMPRESSED_RTF, если хранилище сообщений устанавливает бит STORE_UNCOMPRESSED_RTF в своем свойстве **PR_STORE_SUPPORT_MASK** , чтобы получить несжатую версию **PR_RTF_COMPRESSED **потока, возвращаемые **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="97d31-115">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing STORE_UNCOMPRESSED_RTF if the message store sets the STORE_UNCOMPRESSED_RTF bit in its **PR_STORE_SUPPORT_MASK** property, to get an uncompressed version of the **PR_RTF_COMPRESSED** stream returned from **OpenProperty**.</span></span>
    
3. <span data-ttu-id="97d31-116">Запись данных текста сообщения в несжатую поток, возвращенный из **WrapCompressedRTFStream**.</span><span class="sxs-lookup"><span data-stu-id="97d31-116">Write the message text data to the uncompressed stream returned from **WrapCompressedRTFStream**.</span></span>
    
4. <span data-ttu-id="97d31-117">Фиксация и выпуска и несжатого потоков.</span><span class="sxs-lookup"><span data-stu-id="97d31-117">Commit and release both the uncompressed and compressed streams.</span></span>
    
<span data-ttu-id="97d31-118">На этом этапе Если поставщик хранения сообщений поддерживает RTF, выполнен все, что является обязательным.</span><span class="sxs-lookup"><span data-stu-id="97d31-118">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="97d31-119">Может зависеть от поставщика хранилища сообщений для обработки процесс синхронизации и созданием свойство **PR_BODY** , если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="97d31-119">You can depend on the message store provider to handle the synchronization process and the creation of the **PR_BODY** property, if necessary.</span></span> <span data-ttu-id="97d31-120">Тем не менее если поставщик хранения сообщения не поддерживает формат RTF, необходимо вызвать функцию [RTFSync](rtfsync.md) , чтобы синхронизировать текст с форматированием, установка флага RTF_SYNC_RTF_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="97d31-120">However, if the message store provider does not support RTF, you must call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting, setting the RTF_SYNC_RTF_CHANGED flag.</span></span> 
  

