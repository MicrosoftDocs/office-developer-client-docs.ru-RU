---
title: Обзор архитектуры MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 98a723528a714918ad7e0f10534efb0d38ef139a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410079"
---
# <a name="mapi-architecture-overview"></a><span data-ttu-id="7c84c-103">Обзор архитектуры MAPI</span><span class="sxs-lookup"><span data-stu-id="7c84c-103">MAPI architecture overview</span></span>
 
<span data-ttu-id="7c84c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c84c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c84c-105">MAPI определяет модульную архитектуру, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="7c84c-105">MAPI defines a modular architecture, as shown in the following illustration.</span></span>  
  
<span data-ttu-id="7c84c-106">![Outlook 2010 Outlook](media/amapi_43.gif "2010")</span><span class="sxs-lookup"><span data-stu-id="7c84c-106">![Outlook 2010 architecture](media/amapi_43.gif "Outlook 2010 architecture")</span></span>
  
<span data-ttu-id="7c84c-107">Приложение MAPI известно как клиент, так как является клиентом подсистемы MAPI.</span><span class="sxs-lookup"><span data-stu-id="7c84c-107">The MAPI application is known as a client application because it is a client of the MAPI subsystem.</span></span> <span data-ttu-id="7c84c-108">Приложения, основанные на обмене сообщениями, используют обмен сообщениями в качестве центральной части обработки и предлагают широкие возможности обмена сообщениями, такие как обмен информацией различных типов в различных форматах, а также возможность локального сохранения и организации информации.</span><span class="sxs-lookup"><span data-stu-id="7c84c-108">Messaging-based applications employ messaging as a central part of their processing and offer extensive messaging features, such as the exchange of information of various types in various formats and the ability to save and organize the information locally.</span></span> <span data-ttu-id="7c84c-109">Приложения электронной почты, планирования и потока работы являются примерами приложений на основе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="7c84c-109">Email, scheduling, and work flow applications are examples of messaging-based applications.</span></span>
  
<span data-ttu-id="7c84c-110">Подсистема MAPI состоит из общего пользовательского интерфейса и интерфейсов программирования.</span><span class="sxs-lookup"><span data-stu-id="7c84c-110">The MAPI subsystem is made up of a common user interface and the programming interfaces.</span></span> <span data-ttu-id="7c84c-111">Общий пользовательский интерфейс — это набор диалогов, которые дают клиентские приложения последовательный внешний вид, а пользователям — согласованный способ работы.</span><span class="sxs-lookup"><span data-stu-id="7c84c-111">The common user interface is a set of dialog boxes that gives client applications a consistent look and users a consistent way to work.</span></span>
  
<span data-ttu-id="7c84c-112">MAPI имеет интерфейсы программирования, которые используются подсистемой MAPI, разработчиками клиентского программного обеспечения и разработчиками поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="7c84c-112">MAPI has programming interfaces that are used by the MAPI subsystem, by client software developers, and by service provider developers.</span></span> <span data-ttu-id="7c84c-113">Интерфейс программирования MAPI — это основной объектный интерфейс программирования.</span><span class="sxs-lookup"><span data-stu-id="7c84c-113">The MAPI programming interface is the main object-based programming interface.</span></span> <span data-ttu-id="7c84c-114">Интерфейс программирования MAPI похож на объектную модель компонентов OLE и используется клиентской подсистемой MAPI и приложениями на основе обмена сообщениями, написанными в C или C++.</span><span class="sxs-lookup"><span data-stu-id="7c84c-114">The MAPI programming interface is similar to the OLE Component Object Model and is used by the MAPI subsystem and messaging-based client applications written in C or C++.</span></span> 
  
<span data-ttu-id="7c84c-115">Как разработчик клиентского программного обеспечения вы делаете звонки MAPI непосредственно через интерфейс программирования MAPI.</span><span class="sxs-lookup"><span data-stu-id="7c84c-115">As a client software developer, you make MAPI calls directly through the MAPI programming interface.</span></span> <span data-ttu-id="7c84c-116">Вы можете реализовать обмен сообщениями с помощью одного клиентского интерфейса MAPI или сочетания интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="7c84c-116">You can implement messaging with a single MAPI client interface or a combination of interfaces.</span></span> <span data-ttu-id="7c84c-117">Одно приложение может выполнять вызовы методов или функций, принадлежащих любому из интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="7c84c-117">A single application can make calls to methods or functions belonging to any of the interfaces.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7c84c-118">См. также</span><span class="sxs-lookup"><span data-stu-id="7c84c-118">See also</span></span>

<span data-ttu-id="7c84c-119">-[Функции и архитектура MAPI](mapi-features-and-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="7c84c-119">-[MAPI features and architecture](mapi-features-and-architecture.md)</span></span>

