---
title: Структура поставщиков хранилищ сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: eda62a4cd31e0de695d52391a6717e7a0f5ea581
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426424"
---
# <a name="structure-of-message-store-providers"></a><span data-ttu-id="33c8a-103">Структура поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="33c8a-103">Structure of message store providers</span></span>
  
<span data-ttu-id="33c8a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33c8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33c8a-105">Поставщик хранения сообщений при работе в памяти — это [интерфейс IMSProvider: IUnknown.](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="33c8a-105">A message store provider, when it is running in memory, is an [IMSProvider : IUnknown](imsprovideriunknown.md) interface.</span></span> <span data-ttu-id="33c8a-106">Интерфейс **IMSProvider** позволяет клиентские приложения и шпалер MAPI войти в хранилище сообщений и выйти из него.</span><span class="sxs-lookup"><span data-stu-id="33c8a-106">The **IMSProvider** interface allows client applications and the MAPI spooler to log on to and off of the message store.</span></span> <span data-ttu-id="33c8a-107">Интерфейсы, которые клиентские приложения и шпалер MAPI используют для доступа к папкам и сообщениям в хранилище сообщений, это [интерфейсы IMSLogon](imslogoniunknown.md) и [IMsgStore.](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="33c8a-107">The interfaces that client applications and the MAPI spooler use to access folders and messages in the message store are [IMSLogon](imslogoniunknown.md) and [IMsgStore](imsgstoreimapiprop.md) interfaces.</span></span> <span data-ttu-id="33c8a-108">Эти интерфейсы обычно создаются при первом входе в хранилище сообщений, хотя точка входа [MSProviderInit](msproviderinit.md) В хранилище сообщений DLL также может создавать их.</span><span class="sxs-lookup"><span data-stu-id="33c8a-108">These interfaces are typically created when the message store is first logged on to, although the [MSProviderInit](msproviderinit.md) entry point of the message store DLL could also create them.</span></span> 
  
<span data-ttu-id="33c8a-109">Так как **интерфейсы IMSLogon** и **IMsgStore** имеют несколько методов, может быть проще создать объект класса, унаследованный от обоих этих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="33c8a-109">Because the **IMSLogon** and **IMsgStore** interfaces share some methods, it may be easier to create one class object that inherits from both of these interfaces.</span></span> <span data-ttu-id="33c8a-110">Вы также можете реализовать эти интерфейсы в отдельных объектах и написать внутренние функции помощника в DLL, которые реализуют общие методы, которые затем можно назвать из методов в **интерфейсах IMSLogon** и **IMsgStore.**</span><span class="sxs-lookup"><span data-stu-id="33c8a-110">You can also implement these interfaces in separate objects, and write helper functions internal to your DLL that implement the shared methods that can then be called from the methods in the **IMSLogon** and **IMsgStore** interfaces.</span></span> 
  
<span data-ttu-id="33c8a-111">На следующем рисунке показан план иерархии объектов высокого уровня в хранилище запущенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="33c8a-111">The following illustration shows a high-level outline of the object hierarchy within a running message store.</span></span>
  
<span data-ttu-id="33c8a-112">**Иерархия объектов хранилища сообщений**</span><span class="sxs-lookup"><span data-stu-id="33c8a-112">**Message store object hierarchy**</span></span>
  
<span data-ttu-id="33c8a-113">![Иерархия объектов хранения сообщений.](media/storeobj.gif "Иерархия объектов хранения сообщений")</span><span class="sxs-lookup"><span data-stu-id="33c8a-113">![Message store object hierarchy](media/storeobj.gif "Message store object hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="33c8a-114">См. также</span><span class="sxs-lookup"><span data-stu-id="33c8a-114">See also</span></span>

- [<span data-ttu-id="33c8a-115">Разработка поставщика хранилища сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="33c8a-115">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

