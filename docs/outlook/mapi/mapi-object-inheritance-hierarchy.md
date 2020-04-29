---
title: Иерархия наследования объектов MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4b610415089ff19165ffcabc9e13901ed63c907d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345844"
---
# <a name="mapi-object-inheritance-hierarchy"></a><span data-ttu-id="33458-103">Иерархия наследования объектов MAPI</span><span class="sxs-lookup"><span data-stu-id="33458-103">MAPI object inheritance hierarchy</span></span>

<span data-ttu-id="33458-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33458-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33458-105">Все интерфейсы, реализованные объектами MAPI, в конечном счете, наследуются от [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), интерфейс OLE, позволяющий объектам взаимодействовать.</span><span class="sxs-lookup"><span data-stu-id="33458-105">All interfaces implemented by MAPI objects ultimately inherit from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), the OLE interface that enables objects to communicate.</span></span> <span data-ttu-id="33458-106">Большинство интерфейсов напрямую наследуют от **IUnknown**, но некоторые из них наследуются от одного из двух других базовых интерфейсов: [IMAPIProp: IUnknown](imapipropiunknown.md) или [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="33458-106">Most interfaces directly inherit from **IUnknown**, but some inherit from one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) or [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span></span> <span data-ttu-id="33458-107">На следующем рисунке показана полная иерархия наследования в MAPI.</span><span class="sxs-lookup"><span data-stu-id="33458-107">The following illustration shows the complete inheritance hierarchy in MAPI.</span></span>
  
<span data-ttu-id="33458-108">**Иерархия наследования MAPI**</span><span class="sxs-lookup"><span data-stu-id="33458-108">**MAPI inheritance hierarchy**</span></span>
  
<span data-ttu-id="33458-109">![MAPI inheritance hierarchy](media/amapi_06.gif "Иерархия") наследования MAPI иерархии наследования MAPI</span><span class="sxs-lookup"><span data-stu-id="33458-109">![MAPI inheritance hierarchy](media/amapi_06.gif "MAPI inheritance hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="33458-110">См. также</span><span class="sxs-lookup"><span data-stu-id="33458-110">See also</span></span>

- [<span data-ttu-id="33458-111">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="33458-111">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md) 
- [<span data-ttu-id="33458-112">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="33458-112">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)
- [<span data-ttu-id="33458-113">Общие сведения об объекте и интерфейсе MAPI</span><span class="sxs-lookup"><span data-stu-id="33458-113">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

