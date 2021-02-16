---
title: Связывание OSC с Outlook и социальными сетями
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Outlook Social Connector (OSC) может отображаться в карточке контакта Office и в действиях, состояниях или фотографиях для коллег, друга или любого человека, с которым вы связаны.
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428013"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a><span data-ttu-id="2f2be-103">Связывание OSC с Outlook и социальными сетями</span><span class="sxs-lookup"><span data-stu-id="2f2be-103">Relating the OSC with Outlook and social networks</span></span>

<span data-ttu-id="2f2be-104">Outlook Social Connector (OSC) может отображаться в карточке контакта Office и в действиях, состояниях или фотографиях для коллег, друга или любого человека, с которым вы связаны.</span><span class="sxs-lookup"><span data-stu-id="2f2be-104">The Outlook Social Connector (OSC) can display in the Office Contact Card and Outlook People Pane activities, status, or photo updates for a coworker, friend, or any person you are associated with.</span></span> <span data-ttu-id="2f2be-105">По умолчанию OSC отображает сообщения электронной почты, вложения и запросы на собрания Outlook, полученные от выбранного человека.</span><span class="sxs-lookup"><span data-stu-id="2f2be-105">By default, the OSC displays the Outlook emails, attachments, and meeting requests received from a selected person.</span></span> <span data-ttu-id="2f2be-106">Если выбранный пользователь и пользователь Office совместно работают на сайте SharePoint, OSC также отображает обновления документов и другие действия с этого сайта SharePoint.</span><span class="sxs-lookup"><span data-stu-id="2f2be-106">If the selected person and the Office user collaborate on a SharePoint site, the OSC also displays document updates and other site activities from that SharePoint site.</span></span> <span data-ttu-id="2f2be-107">В зависимости от контекста связи, интересующий пользователя Office, пользователь Office может установить поставщики OSC для бизнес-приложений, внутренних корпоративных веб-сайтов или различных профессиональных и социальных сетей, таких как LinkedIn, Facebook и Windows Live.</span><span class="sxs-lookup"><span data-stu-id="2f2be-107">Depending on the contexts of association that the Office user is interested in, the Office user can install OSC providers for line-of-business applications, internal corporate websites, or a variety of professional and social network sites, such as LinkedIn, Facebook, and Windows Live.</span></span>
  
<span data-ttu-id="2f2be-108">Для поддержки общего доступа к функциональным возможностям в клиентских приложениях Office ядро OSC реализовано как часть общего компонента Office, а "Люди" — в качестве надстройки Outlook.</span><span class="sxs-lookup"><span data-stu-id="2f2be-108">To support sharing of functionality across Office client applications, the OSC core engine is implemented as part of an Office shared component, and the People Pane is implemented as an Outlook add-in.</span></span> <span data-ttu-id="2f2be-109">Чтобы использовать OSC, пользователь Office должен установить Outlook на этом клиентский компьютер и настроить Outlook с профилем, чтобы OSC мог кэшировать контакты в папке "Контакты".</span><span class="sxs-lookup"><span data-stu-id="2f2be-109">To use the OSC, an Office user must have installed Outlook on that client computer and configured Outlook with a profile, so that the OSC can cache contacts in a Contacts folder.</span></span> 
  
<span data-ttu-id="2f2be-110">Поставщик OSC — это DLL-объектная модель компонентов (COM), которая позволяет OSC получать доступ к данным социальных сетей независимо от API каждой социальной сети.</span><span class="sxs-lookup"><span data-stu-id="2f2be-110">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="2f2be-111">DLL поставщика OSC должен быть установлен локально на клиентский компьютер.</span><span class="sxs-lookup"><span data-stu-id="2f2be-111">An OSC provider DLL must be installed locally on a client computer.</span></span> <span data-ttu-id="2f2be-112">Поставщик OSC социальной сети подключает OSC, которая является частью Outlook, с социальной сетью в Интернете.</span><span class="sxs-lookup"><span data-stu-id="2f2be-112">A social network's OSC provider connects the OSC, which is part of Outlook, with the social network on the Internet.</span></span>
  
<span data-ttu-id="2f2be-113">Поставщик OSC должен реализовать набор интерфейсов, определенных как часть возможности поставщика OSC, для связи с OSC.</span><span class="sxs-lookup"><span data-stu-id="2f2be-113">An OSC provider must implement a set of interfaces, defined as part of the OSC provider extensibility, to communicate with the OSC.</span></span> <span data-ttu-id="2f2be-114">В качестве открытой платформы доступна возможность extensibility поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="2f2be-114">OSC provider extensibility is available as an open platform.</span></span>
  
<span data-ttu-id="2f2be-115">Архитектура поставщика OSC позволяет нескольким поставщикам работать с ядром OSC и агрегировать социальные данные, такие как друзья и действия.</span><span class="sxs-lookup"><span data-stu-id="2f2be-115">The provider architecture of the OSC enables multiple providers to work with the OSC core engine and aggregate social information such as friends and activities.</span></span> <span data-ttu-id="2f2be-116">На рисунке 1 показано архитектуру поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="2f2be-116">Figure 1 illustrates the OSC provider architecture.</span></span>
  
<span data-ttu-id="2f2be-117">**Рисунок 1. Архитектура поставщика Outlook Social Connector**</span><span class="sxs-lookup"><span data-stu-id="2f2be-117">**Figure 1. Outlook Social Connector provider architecture**</span></span>

![Социальные сети, поставщики OSC, OSC и Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a><span data-ttu-id="2f2be-119">Терминология</span><span class="sxs-lookup"><span data-stu-id="2f2be-119">Terminology</span></span>

<span data-ttu-id="2f2be-120">В этом справочнике по поставщику Outlook Social Connector социальные сети используются для ссылки на следующие типы сайтов:</span><span class="sxs-lookup"><span data-stu-id="2f2be-120">In this Outlook Social Connector Provider Reference, a social network is used to refer to the following types of sites:</span></span> 
  
- <span data-ttu-id="2f2be-121">Сайты для совместной работы, такие как SharePoint.</span><span class="sxs-lookup"><span data-stu-id="2f2be-121">Collaborative sites such as SharePoint.</span></span>
    
- <span data-ttu-id="2f2be-122">Сайты социальных сетей, такие как Facebook и Windows Live.</span><span class="sxs-lookup"><span data-stu-id="2f2be-122">Social network sites such as Facebook and Windows Live.</span></span>
    
- <span data-ttu-id="2f2be-123">Профессиональные сетевые сайты, такие как LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="2f2be-123">Professional network sites such as LinkedIn.</span></span>
    
- <span data-ttu-id="2f2be-124">Другие бизнес-приложения или корпоративные внутренние веб-сайты, используемые для работы в сети.</span><span class="sxs-lookup"><span data-stu-id="2f2be-124">Other line-of-business applications or corporate internal websites used for networking.</span></span>
    
<span data-ttu-id="2f2be-125">Термин "друг" обычно используется для подключения друзей, семьи, коллег, подключений и других пользователей Office, с кем связан пользователь Office в контексте совместной работы, например SharePoint, или добавленный в учетную запись пользователя в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="2f2be-125">The term friend is used generally to include friends, family, colleagues, connections, and anyone else an Office user is associated with in a collaborative context like SharePoint, or has added to the user's social network account.</span></span> <span data-ttu-id="2f2be-126">Пользователи, которые не являются друзьями, ссылаются на обновления активности друзей, но не являются друзьями, которые были добавлены в учетную запись социальной сети пользователя Office.</span><span class="sxs-lookup"><span data-stu-id="2f2be-126">Non-friends are people referenced in friends' activity updates but are not friends who have been added to the Office user's social network account.</span></span> <span data-ttu-id="2f2be-127">Контакты — это люди из папки контактов Outlook.</span><span class="sxs-lookup"><span data-stu-id="2f2be-127">Contacts are people in an Outlook contact folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2f2be-128">См. также</span><span class="sxs-lookup"><span data-stu-id="2f2be-128">See also</span></span>

- [<span data-ttu-id="2f2be-129">Начало разработки поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="2f2be-129">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

