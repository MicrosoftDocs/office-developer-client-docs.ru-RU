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
# <a name="mapi-architecture-overview"></a><span data-ttu-id="b2c84-103">Обзор архитектуры MAPI</span><span class="sxs-lookup"><span data-stu-id="b2c84-103">MAPI architecture overview</span></span>
 
<span data-ttu-id="b2c84-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2c84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2c84-105">MAPI определяет модульную архитектуру, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="b2c84-105">MAPI defines a modular architecture, as shown in the following illustration.</span></span>  
  
<span data-ttu-id="b2c84-106">![Архитектура Outlook 2010] (media/amapi_43.gif "Архитектура Outlook 2010")</span><span class="sxs-lookup"><span data-stu-id="b2c84-106">![Outlook 2010 architecture](media/amapi_43.gif "Outlook 2010 architecture")</span></span>
  
<span data-ttu-id="b2c84-107">Приложение MAPI известно как клиентское приложение, так как это клиент подсистемы MAPI.</span><span class="sxs-lookup"><span data-stu-id="b2c84-107">The MAPI application is known as a client application because it is a client of the MAPI subsystem.</span></span> <span data-ttu-id="b2c84-108">Приложения, основанные на обмене сообщениями, используют обмен сообщениями в качестве центральной части обработки и предоставляют расширенные функции обмена сообщениями, например обмен информацией различных типов в различных форматах и возможность сохранять и упорядочивать данные локально.</span><span class="sxs-lookup"><span data-stu-id="b2c84-108">Messaging-based applications employ messaging as a central part of their processing and offer extensive messaging features, such as the exchange of information of various types in various formats and the ability to save and organize the information locally.</span></span> <span data-ttu-id="b2c84-109">Примерами приложений, основанных на сообщениях электронной почты, расписания и рабочего процесса, являются приложения для работы с сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b2c84-109">Email, scheduling, and work flow applications are examples of messaging-based applications.</span></span>
  
<span data-ttu-id="b2c84-110">Подсистема MAPI состоит из общего пользовательского интерфейса и интерфейсов программирования.</span><span class="sxs-lookup"><span data-stu-id="b2c84-110">The MAPI subsystem is made up of a common user interface and the programming interfaces.</span></span> <span data-ttu-id="b2c84-111">Общий пользовательский интерфейс — это набор диалоговых окон, обеспечивающих единообразный внешний вид и пользователей для клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="b2c84-111">The common user interface is a set of dialog boxes that gives client applications a consistent look and users a consistent way to work.</span></span>
  
<span data-ttu-id="b2c84-112">MAPI содержит программные интерфейсы, которые используются подсистемой MAPI, разработчиками клиентских программ и разработчиками служб.</span><span class="sxs-lookup"><span data-stu-id="b2c84-112">MAPI has programming interfaces that are used by the MAPI subsystem, by client software developers, and by service provider developers.</span></span> <span data-ttu-id="b2c84-113">Программный интерфейс MAPI — это основной интерфейс программирования, основанный на объектах.</span><span class="sxs-lookup"><span data-stu-id="b2c84-113">The MAPI programming interface is the main object-based programming interface.</span></span> <span data-ttu-id="b2c84-114">Программный интерфейс MAPI похож на объектную модель компонента OLE и используется подсистемой MAPI и клиентскими приложениями на основе обмена сообщениями, написанными на C или C++.</span><span class="sxs-lookup"><span data-stu-id="b2c84-114">The MAPI programming interface is similar to the OLE Component Object Model and is used by the MAPI subsystem and messaging-based client applications written in C or C++.</span></span> 
  
<span data-ttu-id="b2c84-115">Разработчик клиентского программного обеспечения выполняет вызовы MAPI напрямую через программный интерфейс MAPI.</span><span class="sxs-lookup"><span data-stu-id="b2c84-115">As a client software developer, you make MAPI calls directly through the MAPI programming interface.</span></span> <span data-ttu-id="b2c84-116">Вы можете реализовать обмен сообщениями с одним клиентским интерфейсом MAPI или сочетанием интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="b2c84-116">You can implement messaging with a single MAPI client interface or a combination of interfaces.</span></span> <span data-ttu-id="b2c84-117">Одно приложение может совершать вызовы к методам или функциям, принадлежащим любому из интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="b2c84-117">A single application can make calls to methods or functions belonging to any of the interfaces.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b2c84-118">См. также</span><span class="sxs-lookup"><span data-stu-id="b2c84-118">See also</span></span>

<span data-ttu-id="b2c84-119">-[Функции и архитектура MAPI](mapi-features-and-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="b2c84-119">-[MAPI features and architecture](mapi-features-and-architecture.md)</span></span>

