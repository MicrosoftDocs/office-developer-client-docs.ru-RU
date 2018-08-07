---
title: Структура поставщиков хранилища сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2f78428b8067b7937e9bd2ee36934cc29a16bfb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812424"
---
# <a name="structure-of-message-store-providers"></a><span data-ttu-id="fe63d-103">Структура поставщиков хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="fe63d-103">Structure of message store providers</span></span>
  
<span data-ttu-id="fe63d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fe63d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fe63d-105">Поставщик хранилища сообщений, при работе в памяти, — [IMSProvider: IUnknown](imsprovideriunknown.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fe63d-105">A message store provider, when it is running in memory, is an [IMSProvider : IUnknown](imsprovideriunknown.md) interface.</span></span> <span data-ttu-id="fe63d-106">Интерфейс **IMSProvider** позволяет клиентских приложений и диспетчер очереди MAPI для входа и из хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="fe63d-106">The **IMSProvider** interface allows client applications and the MAPI spooler to log on to and off of the message store.</span></span> <span data-ttu-id="fe63d-107">Интерфейсы, которые клиентских приложений и диспетчер очереди MAPI для доступа к папкам и сообщения в хранилище сообщений, [IMSLogon](imslogoniunknown.md) и [IMsgStore](imsgstoreimapiprop.md) интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="fe63d-107">The interfaces that client applications and the MAPI spooler use to access folders and messages in the message store are [IMSLogon](imslogoniunknown.md) and [IMsgStore](imsgstoreimapiprop.md) interfaces.</span></span> <span data-ttu-id="fe63d-108">Эти интерфейсы обычно создаются при хранилища сообщений сначала вход в систему, несмотря на то, что точка входа [MSProviderInit](msproviderinit.md) сообщения хранения DLL-Библиотека может также создать их.</span><span class="sxs-lookup"><span data-stu-id="fe63d-108">These interfaces are typically created when the message store is first logged on to, although the [MSProviderInit](msproviderinit.md) entry point of the message store DLL could also create them.</span></span> 
  
<span data-ttu-id="fe63d-109">Так как **IMSLogon** и **IMsgStore** интерфейсов совместно использовать несколько методов, может быть проще создавать один объект класса, наследуемого от этих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="fe63d-109">Because the **IMSLogon** and **IMsgStore** interfaces share some methods, it may be easier to create one class object that inherits from both of these interfaces.</span></span> <span data-ttu-id="fe63d-110">Также можно реализовать эти интерфейсы в отдельные объекты и запись вспомогательные функции для внутренних библиотеки DLL, которые реализуют общих методов, которые можно вызвать из методов в интерфейсах **IMSLogon** и **IMsgStore** .</span><span class="sxs-lookup"><span data-stu-id="fe63d-110">You can also implement these interfaces in separate objects, and write helper functions internal to your DLL that implement the shared methods that can then be called from the methods in the **IMSLogon** and **IMsgStore** interfaces.</span></span> 
  
<span data-ttu-id="fe63d-111">На следующем рисунке показана высокоуровневая структура иерархии объектов в запущенном хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="fe63d-111">The following illustration shows a high-level outline of the object hierarchy within a running message store.</span></span>
  
<span data-ttu-id="fe63d-112">**Иерархия объектов хранилища сообщений**</span><span class="sxs-lookup"><span data-stu-id="fe63d-112">**Message store object hierarchy**</span></span>
  
<span data-ttu-id="fe63d-113">![Иерархия объектов хранилища сообщений] (media/storeobj.gif "Иерархия объектов хранилища сообщений")</span><span class="sxs-lookup"><span data-stu-id="fe63d-113">![Message store object hierarchy](media/storeobj.gif "Message store object hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fe63d-114">См. также</span><span class="sxs-lookup"><span data-stu-id="fe63d-114">See also</span></span>

- [<span data-ttu-id="fe63d-115">���������� ���������� ��������� ��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="fe63d-115">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

