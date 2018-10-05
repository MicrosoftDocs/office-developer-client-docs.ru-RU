---
title: Иерархия наследования MAPI объекта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4b610415089ff19165ffcabc9e13901ed63c907d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391789"
---
# <a name="mapi-object-inheritance-hierarchy"></a><span data-ttu-id="fe87f-103">Иерархия наследования MAPI объекта</span><span class="sxs-lookup"><span data-stu-id="fe87f-103">MAPI object inheritance hierarchy</span></span>

<span data-ttu-id="fe87f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe87f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe87f-105">Все интерфейсы, реализованные объектов MAPI в конечном счете наследовать от [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), интерфейс OLE, которая позволяет объекты для связи.</span><span class="sxs-lookup"><span data-stu-id="fe87f-105">All interfaces implemented by MAPI objects ultimately inherit from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), the OLE interface that enables objects to communicate.</span></span> <span data-ttu-id="fe87f-106">Большинство интерфейсов напрямую наследовать от **IUnknown**, но некоторые наследование от одного из двух базовых интерфейсов: [IMAPIProp: IUnknown](imapipropiunknown.md) или [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="fe87f-106">Most interfaces directly inherit from **IUnknown**, but some inherit from one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) or [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span></span> <span data-ttu-id="fe87f-107">На следующем рисунке показана иерархия наследования завершения в MAPI.</span><span class="sxs-lookup"><span data-stu-id="fe87f-107">The following illustration shows the complete inheritance hierarchy in MAPI.</span></span>
  
<span data-ttu-id="fe87f-108">**Иерархия наследования MAPI**</span><span class="sxs-lookup"><span data-stu-id="fe87f-108">**MAPI inheritance hierarchy**</span></span>
  
<span data-ttu-id="fe87f-109">![Иерархия наследования MAPI] (media/amapi_06.gif "Иерархия наследования MAPI")</span><span class="sxs-lookup"><span data-stu-id="fe87f-109">![MAPI inheritance hierarchy](media/amapi_06.gif "MAPI inheritance hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fe87f-110">См. также</span><span class="sxs-lookup"><span data-stu-id="fe87f-110">See also</span></span>

- [<span data-ttu-id="fe87f-111">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fe87f-111">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md) 
- [<span data-ttu-id="fe87f-112">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fe87f-112">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)
- [<span data-ttu-id="fe87f-113">Обзор интерфейса и объект MAPI</span><span class="sxs-lookup"><span data-stu-id="fe87f-113">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

