---
title: Связывание OSC с Outlook и социальными сетями
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Outlook Social Connector (OSC) может отображаться в карточке контакта Office и в области "Пользователи" в области "Пользователи", состояния или обновлений фотографий для коллег, друга или любого человека, с которым вы связаны.
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428013"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a><span data-ttu-id="b45d0-103">Связывание OSC с Outlook и социальными сетями</span><span class="sxs-lookup"><span data-stu-id="b45d0-103">Relating the OSC with Outlook and social networks</span></span>

<span data-ttu-id="b45d0-104">Outlook Social Connector (OSC) может отображаться в карточке контакта Office и в области "Пользователи" в области "Пользователи", состояния или обновлений фотографий для коллег, друга или любого человека, с которым вы связаны.</span><span class="sxs-lookup"><span data-stu-id="b45d0-104">The Outlook Social Connector (OSC) can display in the Office Contact Card and Outlook People Pane activities, status, or photo updates for a coworker, friend, or any person you are associated with.</span></span> <span data-ttu-id="b45d0-105">По умолчанию OSC отображает сообщения электронной почты Outlook, вложения и приглашения на собрания, полученные от выбранного пользователя.</span><span class="sxs-lookup"><span data-stu-id="b45d0-105">By default, the OSC displays the Outlook emails, attachments, and meeting requests received from a selected person.</span></span> <span data-ttu-id="b45d0-106">Если выбранный пользователь и пользователь Office работают на сайте SharePoint, OSC также отображает обновления документов и другие действия сайта на этом сайте SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b45d0-106">If the selected person and the Office user collaborate on a SharePoint site, the OSC also displays document updates and other site activities from that SharePoint site.</span></span> <span data-ttu-id="b45d0-107">В зависимости от контекстов связи, в которых заинтересован пользователь Office, пользователь Office может устанавливать поставщиков OSC для бизнес-приложений, внутренних корпоративных веб-сайтов или разнообразных профессиональных и социальных сайтов, таких как LinkedIn Facebook и Windows Live.</span><span class="sxs-lookup"><span data-stu-id="b45d0-107">Depending on the contexts of association that the Office user is interested in, the Office user can install OSC providers for line-of-business applications, internal corporate websites, or a variety of professional and social network sites, such as LinkedIn, Facebook, and Windows Live.</span></span>
  
<span data-ttu-id="b45d0-108">Для поддержки общего доступа к функциям в клиентских приложениях Office ядро компонента OSC реализовано как часть общего компонента Office, а область пользователей реализована как надстройка Outlook.</span><span class="sxs-lookup"><span data-stu-id="b45d0-108">To support sharing of functionality across Office client applications, the OSC core engine is implemented as part of an Office shared component, and the People Pane is implemented as an Outlook add-in.</span></span> <span data-ttu-id="b45d0-109">Чтобы использовать OSC, пользователь Office должен установить Outlook на этом клиентском компьютере и настроить Outlook с использованием профиля, чтобы OSC мог кэшировать контакты в папке "Контакты".</span><span class="sxs-lookup"><span data-stu-id="b45d0-109">To use the OSC, an Office user must have installed Outlook on that client computer and configured Outlook with a profile, so that the OSC can cache contacts in a Contacts folder.</span></span> 
  
<span data-ttu-id="b45d0-110">Поставщик OSC — это DLL-библиотека COM, которая позволяет OSC получать доступ к данным социальных сетей так, как это не зависит от API каждой социальной сети.</span><span class="sxs-lookup"><span data-stu-id="b45d0-110">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="b45d0-111">Библиотека DLL поставщика OSC должна быть установлена локально на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="b45d0-111">An OSC provider DLL must be installed locally on a client computer.</span></span> <span data-ttu-id="b45d0-112">Поставщик OSC в социальной сети подключается к OSC, который входит в состав Outlook, с социальными сетями в Интернете.</span><span class="sxs-lookup"><span data-stu-id="b45d0-112">A social network's OSC provider connects the OSC, which is part of Outlook, with the social network on the Internet.</span></span>
  
<span data-ttu-id="b45d0-113">Поставщик OSC должен реализовать набор интерфейсов, определенных как часть расширяемости поставщика OSC, для подключения к OSC.</span><span class="sxs-lookup"><span data-stu-id="b45d0-113">An OSC provider must implement a set of interfaces, defined as part of the OSC provider extensibility, to communicate with the OSC.</span></span> <span data-ttu-id="b45d0-114">Расширяемость поставщика OSC доступна в виде открытой платформы.</span><span class="sxs-lookup"><span data-stu-id="b45d0-114">OSC provider extensibility is available as an open platform.</span></span>
  
<span data-ttu-id="b45d0-115">Архитектура поставщика OSC позволяет нескольким поставщикам работать с ядром компонента OSC и собирать социальные сведения, такие как друзья и действия.</span><span class="sxs-lookup"><span data-stu-id="b45d0-115">The provider architecture of the OSC enables multiple providers to work with the OSC core engine and aggregate social information such as friends and activities.</span></span> <span data-ttu-id="b45d0-116">На рисунке 1 показана архитектура поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="b45d0-116">Figure 1 illustrates the OSC provider architecture.</span></span>
  
<span data-ttu-id="b45d0-117">**Рис. 1. Архитектура поставщика социальных соединителей Outlook**</span><span class="sxs-lookup"><span data-stu-id="b45d0-117">**Figure 1. Outlook Social Connector provider architecture**</span></span>

![Социальные сети, поставщики OSC, OSC и Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a><span data-ttu-id="b45d0-119">Терминология</span><span class="sxs-lookup"><span data-stu-id="b45d0-119">Terminology</span></span>

<span data-ttu-id="b45d0-120">В этом справочнике по поставщику Outlook Social Connector для ссылки на сайты следующих типов используются социальные сети:</span><span class="sxs-lookup"><span data-stu-id="b45d0-120">In this Outlook Social Connector Provider Reference, a social network is used to refer to the following types of sites:</span></span> 
  
- <span data-ttu-id="b45d0-121">Сайты для сотрудничества, такие как SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b45d0-121">Collaborative sites such as SharePoint.</span></span>
    
- <span data-ttu-id="b45d0-122">Сайты социальных сетей, такие как Facebook и Windows Live.</span><span class="sxs-lookup"><span data-stu-id="b45d0-122">Social network sites such as Facebook and Windows Live.</span></span>
    
- <span data-ttu-id="b45d0-123">Профессиональные сетевые сайты, например LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="b45d0-123">Professional network sites such as LinkedIn.</span></span>
    
- <span data-ttu-id="b45d0-124">Другие бизнес-приложения или корпоративные внутренние веб-сайты, используемые для работы с сетью.</span><span class="sxs-lookup"><span data-stu-id="b45d0-124">Other line-of-business applications or corporate internal websites used for networking.</span></span>
    
<span data-ttu-id="b45d0-125">Термин Friend используется, как правило, для включения друзей, семьи, коллег, подключений и всех остальных пользователей Office, с которыми связан пользователь Office в контексте совместной работы, например SharePoint, или добавлен в учетную запись социальных сетей пользователя.</span><span class="sxs-lookup"><span data-stu-id="b45d0-125">The term friend is used generally to include friends, family, colleagues, connections, and anyone else an Office user is associated with in a collaborative context like SharePoint, or has added to the user's social network account.</span></span> <span data-ttu-id="b45d0-126">Пользователи, не являющиеся друзьями, ссылаются на обновления действий друзей, но не будут иметь друзей, добавленных в учетную запись социальных сетей пользователя Office.</span><span class="sxs-lookup"><span data-stu-id="b45d0-126">Non-friends are people referenced in friends' activity updates but are not friends who have been added to the Office user's social network account.</span></span> <span data-ttu-id="b45d0-127">Контакты — это пользователи, которые находятся в папке контактов Outlook.</span><span class="sxs-lookup"><span data-stu-id="b45d0-127">Contacts are people in an Outlook contact folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b45d0-128">См. также</span><span class="sxs-lookup"><span data-stu-id="b45d0-128">See also</span></span>

- [<span data-ttu-id="b45d0-129">Начало разработки поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="b45d0-129">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

