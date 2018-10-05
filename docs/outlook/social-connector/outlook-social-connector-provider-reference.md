---
title: Справочник по поставщикам Outlook Social Connector
manager: soliver
ms.date: 04/04/2016
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13661393-adf6-4870-86c4-303262317675
description: Outlook Social Connector 2013 предоставляется обмена данными для персональных и корпоративных коммуникаций.
ms.openlocfilehash: e570fe69cbbe0e8d472e712fb3b8592c97fe43c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396704"
---
# <a name="outlook-social-connector-provider-reference"></a><span data-ttu-id="9a7a2-103">Справочник по поставщикам Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="9a7a2-103">Outlook Social Connector provider reference</span></span>

<span data-ttu-id="9a7a2-104">Outlook Social Connector 2013 предоставляется обмена данными для персональных и корпоративных коммуникаций.</span><span class="sxs-lookup"><span data-stu-id="9a7a2-104">The Outlook Social Connector 2013 provides a communication hub for personal and professional communications.</span></span> <span data-ttu-id="9a7a2-105">Outlook Social Connector (OSC) для работы с SharePoint Server, SharePoint Workspace клиента Lync и все клиентские приложения Office, которые поддерживают сведения о присутствии и карточки контакта поддерживают OSC.</span><span class="sxs-lookup"><span data-stu-id="9a7a2-105">The Outlook Social Connector (OSC) works with SharePoint Server, SharePoint Workspace, Lync client, and all Office client applications that support presence information and the Contact Card support the OSC.</span></span> 

<span data-ttu-id="9a7a2-106">В программе Outlook, в частности, просто, выбрав элемент Outlook, такие как сообщения электронной почты или приглашения на собрание и щелкнув отправителя или получателя в данного элемента, не выходя из Outlook, пользователи могут видеть в области пользователей действий, фотографии и обновлениями состояния пользователя на их Избранные социальными сетями.</span><span class="sxs-lookup"><span data-stu-id="9a7a2-106">In Outlook in particular, just by selecting an Outlook item such as an email or meeting request and clicking the sender or a recipient in that item, without leaving Outlook, users can see in the People Pane activities, photos, and status updates of this person on their favorite social networks.</span></span> <span data-ttu-id="9a7a2-107">Пользователи могут легко создавать видеть все Outlook по электронной почте, вложения и собраний, полученных от этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="9a7a2-107">Users can conveniently see all the Outlook emails, attachments, and meetings received from this person.</span></span> <span data-ttu-id="9a7a2-108">В среде организации на сайте SharePoint можно также, отображаемых в области пользователей обновления документов или действий сайта этого пользователя на сайте SharePoint.</span><span class="sxs-lookup"><span data-stu-id="9a7a2-108">In an organizational environment, users on a SharePoint site can also see in the People Pane document updates and other site activities of this person on the SharePoint site.</span></span>
  
<span data-ttu-id="9a7a2-109">Социальные сети можно разработать поставщик для OSC для синхронизации и отображения обновления социальной сети в вспомогательных серверов и приложений.</span><span class="sxs-lookup"><span data-stu-id="9a7a2-109">A social network can develop a provider for the OSC to synchronize and surface social network updates in supporting servers and applications.</span></span> <span data-ttu-id="9a7a2-110">Популярные социальных сетей, например, Facebook, LinkedIn а Windows Live предлагают поставщиков для OSC.</span><span class="sxs-lookup"><span data-stu-id="9a7a2-110">Popular social networks such as LinkedIn, Facebook, and Windows Live are offering providers for the OSC.</span></span> 
  
<span data-ttu-id="9a7a2-111">Outlook Social Connector 2013 Справочник поставщика по описываются способы разработки поставщика OSC с помощью возможности расширения поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="9a7a2-111">The Outlook Social Connector 2013 Provider Reference describes how to develop an OSC provider using OSC provider extensibility.</span></span> 
  
<span data-ttu-id="9a7a2-112">Если у вас нет опыта разработки решений для Outlook, см. статью [Выбор API или технологии разработки решений для Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md), чтобы выбрать API-интерфейсы и технологии, наиболее соответствующие вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="9a7a2-112">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="9a7a2-113">В этой статье</span><span class="sxs-lookup"><span data-stu-id="9a7a2-113">In this section</span></span>

- <span data-ttu-id="9a7a2-114">[Начало разработки поставщика Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md): Обзор OSC, включая следующие: как поставщика OSC могут быть полезны, быстрого шаги, необходимые для разработки поставщика, технические требования советы и рекомендации для Разработка поставщика, а также новые возможности этой версии.</span><span class="sxs-lookup"><span data-stu-id="9a7a2-114">[Getting Started with Developing an Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md): Provides an overview of the OSC, including the following: how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span>
    
- <span data-ttu-id="9a7a2-115">[Шаблоны OSC примера](osc-sample-templates.md): описаны несколько шаблонов Visual Studio для разработки поставщика.</span><span class="sxs-lookup"><span data-stu-id="9a7a2-115">[OSC Sample Templates](osc-sample-templates.md): Describes several Visual Studio templates for developing a provider.</span></span>
    
- <span data-ttu-id="9a7a2-116">[Типичные последовательности OSC вызов](osc-typical-calling-sequences.md): описываются некоторые типичные последовательности вызова с OSC члены в интерфейсы расширяемости поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="9a7a2-116">[OSC Typical Calling Sequences](osc-typical-calling-sequences.md): Describes a few typical calling sequences by the OSC of members in the OSC provider extensibility interfaces.</span></span> <span data-ttu-id="9a7a2-117">Это позволит вам лучше понять, как реализовать эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="9a7a2-117">This should enable you to better understand how to implement these interfaces.</span></span>
    
- <span data-ttu-id="9a7a2-118">[Разработка поставщика с использованием схемы XML OSC](developing-a-provider-with-the-osc-xml-schema.md): описывает, как интерфейсов расширения поставщика OSC и схемы XML для OSC предназначены для поддержки поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="9a7a2-118">[Developing a Provider with the OSC XML Schema](developing-a-provider-with-the-osc-xml-schema.md): Describes how the OSC provider extensibility interfaces and OSC XML schema are designed to support an OSC provider.</span></span>
    
- <span data-ttu-id="9a7a2-119">[Отладка поставщика](debugging-a-provider.md): предлагает несколько способов отладки поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="9a7a2-119">[Debugging a Provider](debugging-a-provider.md): Suggests a few ways to help debug an OSC provider.</span></span>
    
- <span data-ttu-id="9a7a2-120">[Развертывание поставщика](deploying-a-provider.md): описываются требования к регистрации для поставщика OSC и содержит контрольный список для установки поставщика.</span><span class="sxs-lookup"><span data-stu-id="9a7a2-120">[Deploying a Provider](deploying-a-provider.md): Describes registration requirements for an OSC provider, and provides a checklist for installing a provider.</span></span>
    
- <span data-ttu-id="9a7a2-121">[Подготовка к выпуску поставщика OSC](getting-ready-to-release-an-osc-provider.md): предлагаются тесты, можно выполнить перед выпуском поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="9a7a2-121">[Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md): Suggests tests you can do before releasing an OSC provider.</span></span>
    
- <span data-ttu-id="9a7a2-122">[Справочник по поставщика Outlook Social Connector](outlook-social-connector-provider-reference-0.md): Справочник сведения для интерфейсов расширения поставщика OSC и схемы XML для OSC и списки кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="9a7a2-122">[Outlook Social Connector Provider Reference](outlook-social-connector-provider-reference-0.md): Provides reference information for the OSC provider extensibility interfaces and OSC XML schema, and lists possible error codes.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9a7a2-123">См. также</span><span class="sxs-lookup"><span data-stu-id="9a7a2-123">See also</span></span>

- [<span data-ttu-id="9a7a2-124">Уведомление об авторских правах характеристики Справочник по Outlook Social Connector 2013 поставщика</span><span class="sxs-lookup"><span data-stu-id="9a7a2-124">Outlook Social Connector 2013 provider reference copyright notice</span></span>](outlook-social-connector-2013-provider-reference-copyright-notice.md) 
- [<span data-ttu-id="9a7a2-125">Условные обозначения в документах (Возможно, на английском языке)</span><span class="sxs-lookup"><span data-stu-id="9a7a2-125">Document Conventions</span></span>](https://msdn.microsoft.com/office/aa905365.aspx)   
- [<span data-ttu-id="9a7a2-126">Специальные возможности в продуктах Майкрософт (Возможно, на английском языке)</span><span class="sxs-lookup"><span data-stu-id="9a7a2-126">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/enable/products/default.aspx)  
- [<span data-ttu-id="9a7a2-127">Уведомление о конфиденциальности (Майкрософт), доступное в Интернете</span><span class="sxs-lookup"><span data-stu-id="9a7a2-127">Microsoft Online Privacy Notice</span></span>](https://privacy.microsoft.com/en-us/privacystatement)
    

