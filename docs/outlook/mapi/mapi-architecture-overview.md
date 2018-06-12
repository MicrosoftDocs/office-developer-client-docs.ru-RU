---
title: Обзор архитектуры MAPI (en)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: db8ca0945c429e7b277ec95b419386d1ce175169
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809697"
---
# <a name="mapi-architecture-overview"></a><span data-ttu-id="01192-103">Обзор архитектуры MAPI (en)</span><span class="sxs-lookup"><span data-stu-id="01192-103">MAPI architecture overview</span></span>
 
<span data-ttu-id="01192-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="01192-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="01192-105">MAPI определяет модульных архитектуры, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="01192-105">MAPI defines a modular architecture, as shown in the following illustration.</span></span>  
  
<span data-ttu-id="01192-106">![Архитектура Outlook 2010] (media/amapi_43.gif "Архитектура Outlook 2010")</span><span class="sxs-lookup"><span data-stu-id="01192-106">![Outlook 2010 architecture](media/amapi_43.gif "Outlook 2010 architecture")</span></span>
  
<span data-ttu-id="01192-107">Приложения MAPI называется клиентского приложения, так как это клиент подсистемы MAPI.</span><span class="sxs-lookup"><span data-stu-id="01192-107">The MAPI application is known as a client application because it is a client of the MAPI subsystem.</span></span> <span data-ttu-id="01192-108">Приложения на основе системы обмена сообщениями использовать системы обмена сообщениями в рамках центра обработки и предлагают широкое возможности обмена мгновенными сообщениями, например exchange различные виды данных в различные форматы и возможность для сохранения и упорядочить данные локально.</span><span class="sxs-lookup"><span data-stu-id="01192-108">Messaging-based applications employ messaging as a central part of their processing and offer extensive messaging features, such as the exchange of information of various types in various formats and the ability to save and organize the information locally.</span></span> <span data-ttu-id="01192-109">Электронной почты, планирования и приложений рабочего потока, примеры приложений на основе системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="01192-109">Email, scheduling, and work flow applications are examples of messaging-based applications.</span></span>
  
<span data-ttu-id="01192-110">Подсистема MAPI, состоящих из общего пользовательского интерфейса и программных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="01192-110">The MAPI subsystem is made up of a common user interface and the programming interfaces.</span></span> <span data-ttu-id="01192-111">Общий интерфейс пользователя — это набор диалоговых окон, задающей клиентских приложений стандартного оформления и пользователей согласованность работы.</span><span class="sxs-lookup"><span data-stu-id="01192-111">The common user interface is a set of dialog boxes that gives client applications a consistent look and users a consistent way to work.</span></span>
  
<span data-ttu-id="01192-112">MAPI имеет программных интерфейсов, которые используются в подсистеме MAPI, разработчики клиентского программного обеспечения и разработчиков поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="01192-112">MAPI has programming interfaces that are used by the MAPI subsystem, by client software developers, and by service provider developers.</span></span> <span data-ttu-id="01192-113">Программный интерфейс MAPI — это основной интерфейс программирования на основе объекта.</span><span class="sxs-lookup"><span data-stu-id="01192-113">The MAPI programming interface is the main object-based programming interface.</span></span> <span data-ttu-id="01192-114">Программный интерфейс MAPI похож на модель объектов OLE компонента и используется Подсистема MAPI и на основе системы обмена сообщениями клиентских приложений, написанных на языке C или C++.</span><span class="sxs-lookup"><span data-stu-id="01192-114">The MAPI programming interface is similar to the OLE Component Object Model and is used by the MAPI subsystem and messaging-based client applications written in C or C++.</span></span> 
  
<span data-ttu-id="01192-115">Разработчик программного обеспечения клиента выполнять вызовы MAPI непосредственно через программный интерфейс MAPI.</span><span class="sxs-lookup"><span data-stu-id="01192-115">As a client software developer, you make MAPI calls directly through the MAPI programming interface.</span></span> <span data-ttu-id="01192-116">Вы можете реализовать системы обмена сообщениями с помощью единого интерфейса MAPI клиента или сочетание интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="01192-116">You can implement messaging with a single MAPI client interface or a combination of interfaces.</span></span> <span data-ttu-id="01192-117">Одно приложение может выполнять вызовы методов или функций, относящегося к любой интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="01192-117">A single application can make calls to methods or functions belonging to any of the interfaces.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="01192-118">См. также</span><span class="sxs-lookup"><span data-stu-id="01192-118">See also</span></span>

<span data-ttu-id="01192-119">-[Функции MAPI и архитектура](mapi-features-and-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="01192-119">-[MAPI features and architecture](mapi-features-and-architecture.md)</span></span>

