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
ms.openlocfilehash: 4f8bc2a5268d220c17a59148f8b8ba1d320d225b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279792"
---
# <a name="objects-and-the-mapi-architecture"></a><span data-ttu-id="41af8-103">Объекты и архитектура MAPI</span><span class="sxs-lookup"><span data-stu-id="41af8-103">Objects and the MAPI architecture</span></span>

<span data-ttu-id="41af8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41af8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41af8-105">Все объекты, которые определяет MAPI, попадают в один или несколько уровней в архитектуре MAPI.</span><span class="sxs-lookup"><span data-stu-id="41af8-105">All of the objects that MAPI defines fall into one or more layers in the MAPI architecture.</span></span> <span data-ttu-id="41af8-106">Уровень клиентского интерфейса содержит все объекты, которые могут быть реализованы в клиентском приложении, в средстве просмотра форм или на сервере форм.</span><span class="sxs-lookup"><span data-stu-id="41af8-106">The client interface layer contains all the objects that a client application, form viewer, or form server can implement.</span></span> <span data-ttu-id="41af8-107">Интерфейсный уровень поставщика услуг содержит объекты, которые может реализовать поставщик услуг любого типа.</span><span class="sxs-lookup"><span data-stu-id="41af8-107">The service provider interface layer contains the objects that a service provider of any type can implement.</span></span> <span data-ttu-id="41af8-108">Этот уровень включает объекты, реализованные в адресных книгах, хранилищах сообщений, поставщиках транспорта и библиотеках форм.</span><span class="sxs-lookup"><span data-stu-id="41af8-108">This layer includes objects implemented by address books, message stores, transport providers, and form libraries.</span></span> <span data-ttu-id="41af8-109">Слой, представляющий подсистему MAPI, располагается между слоями интерфейса клиента и поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="41af8-109">The layer that represents the MAPI subsystem is positioned between the client and service provider interface layers.</span></span> <span data-ttu-id="41af8-110">Уровень MAPI содержит все объекты, которые MAPI реализует для клиентов или поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="41af8-110">The MAPI layer contains all of the objects that MAPI implements for clients or service providers to use.</span></span> 
  
<span data-ttu-id="41af8-111">На следующем рисунке показано, где каждый объект MAPI соответствует архитектуре MAPI.</span><span class="sxs-lookup"><span data-stu-id="41af8-111">The following illustration shows where each of the MAPI objects fits into the MAPI architecture.</span></span> <span data-ttu-id="41af8-112">Объекты представлены с именами производных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="41af8-112">The objects are represented with the names of their derived interfaces.</span></span> <span data-ttu-id="41af8-113">Например, объект приемника уведомлений отображается как [имапиадвисесинк: IUnknown](imapiadvisesinkiunknown.md), интерфейс, производный от [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) и который реализует каждый объект приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="41af8-113">For example, an advise sink object is shown as [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), the interface that derives from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) and that every advise sink object implements.</span></span> <span data-ttu-id="41af8-114">Интерфейсы, которые мосты используют или реализуются несколькими компонентами.</span><span class="sxs-lookup"><span data-stu-id="41af8-114">The interfaces that bridge layers are either used or implemented by multiple components.</span></span> <span data-ttu-id="41af8-115">Несмотря на то, что уровень MAPI разделяет слои клиента и поставщика, подразумевая, что весь обмен данными должен проходить через MAPI, это не так.</span><span class="sxs-lookup"><span data-stu-id="41af8-115">Although the MAPI layer appears to separate the client and provider layers, implying that all communication must flow through MAPI, this is not the case.</span></span> <span data-ttu-id="41af8-116">Клиенты могут и напрямую связываться с объектами поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="41af8-116">Clients can and do communicate directly to service provider objects.</span></span> 
  
<span data-ttu-id="41af8-117">**Уровни объектов в MAPI**</span><span class="sxs-lookup"><span data-stu-id="41af8-117">**Object layers in MAPI**</span></span>
  
<span data-ttu-id="41af8-118">![Уровни объектов в](media/amapi_38.gif "объектных слоях MAPI в MAPI")</span><span class="sxs-lookup"><span data-stu-id="41af8-118">![Object layers in MAPI](media/amapi_38.gif "Object layers in MAPI")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="41af8-119">См. также</span><span class="sxs-lookup"><span data-stu-id="41af8-119">See also</span></span>

- [<span data-ttu-id="41af8-120">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="41af8-120">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)
- [<span data-ttu-id="41af8-121">Общие сведения об объекте и интерфейсе MAPI</span><span class="sxs-lookup"><span data-stu-id="41af8-121">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

