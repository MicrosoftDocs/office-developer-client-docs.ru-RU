---
title: Объекты и архитектура MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 29a61ff8f7894c5582d31895bacd74e1ebcaa49c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583878"
---
# <a name="objects-and-the-mapi-architecture"></a><span data-ttu-id="bed2a-103">Объекты и архитектура MAPI</span><span class="sxs-lookup"><span data-stu-id="bed2a-103">Objects and the MAPI architecture</span></span>

<span data-ttu-id="bed2a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bed2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bed2a-105">Все объекты, которые определяются MAPI могут быть разделены на один или несколько уровней в архитектуре MAPI.</span><span class="sxs-lookup"><span data-stu-id="bed2a-105">All of the objects that MAPI defines fall into one or more layers in the MAPI architecture.</span></span> <span data-ttu-id="bed2a-106">На уровне клиента интерфейс содержит все объекты, которые можно реализовать клиентского приложения, средство просмотра формы или формы сервера.</span><span class="sxs-lookup"><span data-stu-id="bed2a-106">The client interface layer contains all the objects that a client application, form viewer, or form server can implement.</span></span> <span data-ttu-id="bed2a-107">Уровень интерфейса поставщика службы содержит объекты, которые можно реализовать поставщика услуг любого типа.</span><span class="sxs-lookup"><span data-stu-id="bed2a-107">The service provider interface layer contains the objects that a service provider of any type can implement.</span></span> <span data-ttu-id="bed2a-108">Этот уровень включает в себя объектов, реализованных адресных книг, хранилищ сообщений, поставщиками транспорта и библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="bed2a-108">This layer includes objects implemented by address books, message stores, transport providers, and form libraries.</span></span> <span data-ttu-id="bed2a-109">Уровень, представляющий подсистемы MAPI находится между уровнями интерфейса поставщика клиента и службы.</span><span class="sxs-lookup"><span data-stu-id="bed2a-109">The layer that represents the MAPI subsystem is positioned between the client and service provider interface layers.</span></span> <span data-ttu-id="bed2a-110">Уровень MAPI содержит все объекты, внедряемые MAPI для клиентов или поставщиков услуг для использования.</span><span class="sxs-lookup"><span data-stu-id="bed2a-110">The MAPI layer contains all of the objects that MAPI implements for clients or service providers to use.</span></span> 
  
<span data-ttu-id="bed2a-111">На следующем рисунке показано, где каждый объект MAPI умещается в архитектуре MAPI.</span><span class="sxs-lookup"><span data-stu-id="bed2a-111">The following illustration shows where each of the MAPI objects fits into the MAPI architecture.</span></span> <span data-ttu-id="bed2a-112">Объекты, представленные с именами их производные интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="bed2a-112">The objects are represented with the names of their derived interfaces.</span></span> <span data-ttu-id="bed2a-113">Например, объект приемника уведомлений отображается как [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md), интерфейс, который является производным от [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) , который реализует каждый объект приемник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bed2a-113">For example, an advise sink object is shown as [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), the interface that derives from [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) and that every advise sink object implements.</span></span> <span data-ttu-id="bed2a-114">Интерфейсы, мост слои используется или реализован в нескольких компонентах.</span><span class="sxs-lookup"><span data-stu-id="bed2a-114">The interfaces that bridge layers are either used or implemented by multiple components.</span></span> <span data-ttu-id="bed2a-115">Несмотря на то, что отображается на уровне MAPI для разделения уровней клиента и поставщиком, подразумевает, что все соединения должен проходить через MAPI, это не так.</span><span class="sxs-lookup"><span data-stu-id="bed2a-115">Although the MAPI layer appears to separate the client and provider layers, implying that all communication must flow through MAPI, this is not the case.</span></span> <span data-ttu-id="bed2a-116">Клиенты могут и связаны непосредственно с объектов поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="bed2a-116">Clients can and do communicate directly to service provider objects.</span></span> 
  
<span data-ttu-id="bed2a-117">**Уровни объектов в MAPI**</span><span class="sxs-lookup"><span data-stu-id="bed2a-117">**Object layers in MAPI**</span></span>
  
<span data-ttu-id="bed2a-118">![Слои объекта в MAPI] (media/amapi_38.gif "Слои объекта в MAPI")</span><span class="sxs-lookup"><span data-stu-id="bed2a-118">![Object layers in MAPI](media/amapi_38.gif "Object layers in MAPI")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bed2a-119">См. также</span><span class="sxs-lookup"><span data-stu-id="bed2a-119">See also</span></span>

- [<span data-ttu-id="bed2a-120">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bed2a-120">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)
- [<span data-ttu-id="bed2a-121">Обзор интерфейса и объект MAPI</span><span class="sxs-lookup"><span data-stu-id="bed2a-121">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

