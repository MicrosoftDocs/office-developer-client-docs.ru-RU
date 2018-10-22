---
title: Хранилища сообщений по умолчанию
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3f7bf720f9105f6a81b832233cc648bc1d9ac91d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576913"
---
# <a name="default-message-stores"></a><span data-ttu-id="27feb-103">Хранилища сообщений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="27feb-103">Default Message Stores</span></span>

  
  
<span data-ttu-id="27feb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27feb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27feb-p101">Хранилище сообщений по умолчанию – это хранилище, которое клиентское приложение может использовать в общие целях, обмена сообщениями. Существует ряд дополнительных вариантов поставщиков хранилища сообщений, которые могут потребоваться, если поставщик хранилища сообщений будет использоваться в качестве хранилища сообщений по умолчанию. Это происходит в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="27feb-p101">A default message store is one that client applications can use for general purpose messaging tasks. There are a number of optional features for message store providers that become required if the message store provider is to be used as the default message store. They are as follows:</span></span>
  
- <span data-ttu-id="27feb-108">Реализация специальных папок: Входящие, Оправленные и папки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="27feb-108">Implementing the special folders: the Inbox, Outbox, and search-results folders.</span></span>
    
- <span data-ttu-id="27feb-109">Предоставление отчетов для чтения и не предназначенных для чтения.</span><span class="sxs-lookup"><span data-stu-id="27feb-109">Providing read and nonread reports.</span></span>
    
- <span data-ttu-id="27feb-110">Разрешение на отправки входящих и исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="27feb-110">Allowing incoming and outgoing message submissions.</span></span>
    
- <span data-ttu-id="27feb-111">Разрешение создания сообщений с произвольными классами сообщений.</span><span class="sxs-lookup"><span data-stu-id="27feb-111">Allowing the creation of messages with arbitrary message classes.</span></span>
    
- <span data-ttu-id="27feb-112">Свойства, поддерживающие имена и несколько значений.</span><span class="sxs-lookup"><span data-stu-id="27feb-112">Supporting named and multiple-value properties.</span></span>
    
- <span data-ttu-id="27feb-113">Поддержка функции[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md), даже если поставщик хранилища сообщений  тесно связан с поставщиком передачи данных.</span><span class="sxs-lookup"><span data-stu-id="27feb-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span></span> 
    
- <span data-ttu-id="27feb-p102">Поддержка таблиц со связанным содержимым. Дополнительные сведения см. в статье [Содержимое таблиц](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="27feb-p102">Supporting associated contents tables. For more information, see [Contents Tables](contents-tables.md).</span></span>
    
- <span data-ttu-id="27feb-116">Поддержка уведомлений программы буферизации MAPI при наличии очереди исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="27feb-116">Supporting notification of the MAPI spooler when there are messages in the outgoing message queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27feb-117">См. также</span><span class="sxs-lookup"><span data-stu-id="27feb-117">See also</span></span>



[<span data-ttu-id="27feb-118">Разработка поставщика хранилища сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="27feb-118">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

