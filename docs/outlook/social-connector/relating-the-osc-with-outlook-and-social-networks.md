---
title: Связывание OSC с Outlook и социальными сетями
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Коллеги, friend или любого контакта, с которым связаны с в Office карточки контакта и области пользователей Outlook действия, состояние или обновления фотографий можно отобразить Outlook Social Connector (OSC).
ms.openlocfilehash: 6dc6221b89eca5303e7cf6a201927659d4ac9107
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812839"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a><span data-ttu-id="61354-103">Связывание OSC с Outlook и социальными сетями</span><span class="sxs-lookup"><span data-stu-id="61354-103">Relating the OSC with Outlook and social networks</span></span>

<span data-ttu-id="61354-104">Коллеги, friend или любого контакта, с которым связаны с в Office карточки контакта и области пользователей Outlook действия, состояние или обновления фотографий можно отобразить Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="61354-104">The Outlook Social Connector (OSC) can display in the Office Contact Card and Outlook People Pane activities, status, or photo updates for a coworker, friend, or any person you are associated with.</span></span> <span data-ttu-id="61354-105">По умолчанию OSC отображает сообщениях Outlook, вложения, и приглашений на собрания полученных от выбранного пользователя.</span><span class="sxs-lookup"><span data-stu-id="61354-105">By default, the OSC displays the Outlook emails, attachments, and meeting requests received from a selected person.</span></span> <span data-ttu-id="61354-106">Если выбранного пользователя и пользователь Office совместно работать на сайте SharePoint, OSC также отображает обновления документов и других действий сайта для этого сайта SharePoint.</span><span class="sxs-lookup"><span data-stu-id="61354-106">If the selected person and the Office user collaborate on a SharePoint site, the OSC also displays document updates and other site activities from that SharePoint site.</span></span> <span data-ttu-id="61354-107">В зависимости от контекстах связь, которая является интерес для пользователей Office Office пользователь может установить поставщиков OSC для бизнес приложений, внутренний корпоративный веб-сайтов или различных сайтов профессиональный и социальные сети, например, LinkedIn, Facebook (en) и Windows Live.</span><span class="sxs-lookup"><span data-stu-id="61354-107">Depending on the contexts of association that the Office user is interested in, the Office user can install OSC providers for line-of-business applications, internal corporate websites, or a variety of professional and social network sites, such as LinkedIn, Facebook, and Windows Live.</span></span>
  
<span data-ttu-id="61354-108">Чтобы обеспечить поддержку для совместного использования функциональных возможностей нескольких клиентских приложениях Office, ядра OSC реализован как часть общего компонента Office и области пользователей реализован в виде надстройки Outlook.</span><span class="sxs-lookup"><span data-stu-id="61354-108">To support sharing of functionality across Office client applications, the OSC core engine is implemented as part of an Office shared component, and the People Pane is implemented as an Outlook add-in.</span></span> <span data-ttu-id="61354-109">Чтобы использовать OSC, пользователя с Office необходимо установки Outlook на этом компьютере клиента и настроить Outlook с использованием профиля так, чтобы OSC можно кэшировать контактов в папке контактов.</span><span class="sxs-lookup"><span data-stu-id="61354-109">To use the OSC, an Office user must have installed Outlook on that client computer and configured Outlook with a profile, so that the OSC can cache contacts in a Contacts folder.</span></span> 
  
<span data-ttu-id="61354-110">Поставщика OSC — модели компонентных объектов (COM) библиотеки DLL, которая позволяет OSC для доступа к данным социальных сетей, чтобы не зависит от API-интерфейсы каждого социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="61354-110">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="61354-111">Библиотека поставщика OSC устанавливается локально на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="61354-111">An OSC provider DLL must be installed locally on a client computer.</span></span> <span data-ttu-id="61354-112">Поставщика OSC социальной сети подключается OSC, которая является частью Outlook с помощью социальных сетей в Интернете.</span><span class="sxs-lookup"><span data-stu-id="61354-112">A social network's OSC provider connects the OSC, which is part of Outlook, with the social network on the Internet.</span></span>
  
<span data-ttu-id="61354-113">Поставщика OSC необходимо реализовать набор интерфейсов, определенные как часть возможности расширения поставщика OSC для взаимодействия с OSC.</span><span class="sxs-lookup"><span data-stu-id="61354-113">An OSC provider must implement a set of interfaces, defined as part of the OSC provider extensibility, to communicate with the OSC.</span></span> <span data-ttu-id="61354-114">Возможности расширения поставщика OSC доступна как open платформы.</span><span class="sxs-lookup"><span data-stu-id="61354-114">OSC provider extensibility is available as an open platform.</span></span>
  
<span data-ttu-id="61354-115">Архитектура поставщика OSC включает несколько поставщиков для работы с OSC ядра и статистической обработки социальных сведения, такие как друзей и действия.</span><span class="sxs-lookup"><span data-stu-id="61354-115">The provider architecture of the OSC enables multiple providers to work with the OSC core engine and aggregate social information such as friends and activities.</span></span> <span data-ttu-id="61354-116">На рисунке 1 показана архитектура поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="61354-116">Figure 1 illustrates the OSC provider architecture.</span></span>
  
<span data-ttu-id="61354-117">**На рисунке 1. Архитектура поставщика Outlook Social Connector**</span><span class="sxs-lookup"><span data-stu-id="61354-117">**Figure 1. Outlook Social Connector provider architecture**</span></span>

![Социальные сети, поставщики OSC, OSC и Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a><span data-ttu-id="61354-119">Терминология</span><span class="sxs-lookup"><span data-stu-id="61354-119">Terminology</span></span>

<span data-ttu-id="61354-120">В Outlook Social Connector поставщика ссылку социальные сети используется для ссылки на следующие типы сайтов:</span><span class="sxs-lookup"><span data-stu-id="61354-120">In this Outlook Social Connector Provider Reference, a social network is used to refer to the following types of sites:</span></span> 
  
- <span data-ttu-id="61354-121">Сайты совместной работы, таких как SharePoint.</span><span class="sxs-lookup"><span data-stu-id="61354-121">Collaborative sites such as SharePoint.</span></span>
    
- <span data-ttu-id="61354-122">Сайты социальных сетей, такие как Facebook и Windows Live.</span><span class="sxs-lookup"><span data-stu-id="61354-122">Social network sites such as Facebook and Windows Live.</span></span>
    
- <span data-ttu-id="61354-123">Профессиональный сетевых узлов, таких как LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="61354-123">Professional network sites such as LinkedIn.</span></span>
    
- <span data-ttu-id="61354-124">Другие бизнес приложения или корпоративной внутренней веб-сайтов, используемые для работы в сети.</span><span class="sxs-lookup"><span data-stu-id="61354-124">Other line-of-business applications or corporate internal websites used for networking.</span></span>
    
<span data-ttu-id="61354-125">Friend термин обычно используется для включения друзья, семейства, коллеги, подключений и кому-либо Office user связан с в контексте совместной работы, как SharePoint или добавлен учетная запись социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="61354-125">The term friend is used generally to include friends, family, colleagues, connections, and anyone else an Office user is associated with in a collaborative context like SharePoint, or has added to the user's social network account.</span></span> <span data-ttu-id="61354-126">Не друзья сотрудники по ссылке в друзей действия обновления, но не друзья, добавленные в учетной записи пользователя Office социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="61354-126">Non-friends are people referenced in friends' activity updates but are not friends who have been added to the Office user's social network account.</span></span> <span data-ttu-id="61354-127">Контакты, людей в папке контактов Outlook.</span><span class="sxs-lookup"><span data-stu-id="61354-127">Contacts are people in an Outlook contact folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="61354-128">См. также</span><span class="sxs-lookup"><span data-stu-id="61354-128">See also</span></span>

- [<span data-ttu-id="61354-129">Начало разработки поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="61354-129">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

