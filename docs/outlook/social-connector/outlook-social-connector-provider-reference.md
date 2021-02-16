---
title: Справочник по поставщикам Outlook Social Connector
manager: soliver
ms.date: 04/04/2016
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13661393-adf6-4870-86c4-303262317675
description: Outlook Social Connector 2013 предоставляет центр связи для личных и профессиональных коммуникаций.
ms.openlocfilehash: e570fe69cbbe0e8d472e712fb3b8592c97fe43c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359838"
---
# <a name="outlook-social-connector-provider-reference"></a><span data-ttu-id="3b17a-103">Справочник по поставщикам Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="3b17a-103">Outlook Social Connector provider reference</span></span>

<span data-ttu-id="3b17a-104">Outlook Social Connector 2013 предоставляет центр связи для личных и профессиональных коммуникаций.</span><span class="sxs-lookup"><span data-stu-id="3b17a-104">The Outlook Social Connector 2013 provides a communication hub for personal and professional communications.</span></span> <span data-ttu-id="3b17a-105">Outlook Social Connector (OSC) работает с SharePoint Server, SharePoint Workspace, клиентом Lync и всеми клиентские приложения Office, которые поддерживают сведения о присутствии и карточку контакта, поддерживают OSC.</span><span class="sxs-lookup"><span data-stu-id="3b17a-105">The Outlook Social Connector (OSC) works with SharePoint Server, SharePoint Workspace, Lync client, and all Office client applications that support presence information and the Contact Card support the OSC.</span></span> 

<span data-ttu-id="3b17a-106">В outlook, в частности, просто выбрав элемент Outlook, например сообщение электронной почты или запрос на собрание, и щелкнув отправитель или получателя в этом элементе, не выходя из Outlook, пользователи могут видеть в действиях области людей, фотографии и обновлениях состояния этого пользователя в избранных социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="3b17a-106">In Outlook in particular, just by selecting an Outlook item such as an email or meeting request and clicking the sender or a recipient in that item, without leaving Outlook, users can see in the People Pane activities, photos, and status updates of this person on their favorite social networks.</span></span> <span data-ttu-id="3b17a-107">Пользователи могут легко видеть все сообщения электронной почты, вложения и собрания Outlook, полученные от этого человека.</span><span class="sxs-lookup"><span data-stu-id="3b17a-107">Users can conveniently see all the Outlook emails, attachments, and meetings received from this person.</span></span> <span data-ttu-id="3b17a-108">В среде организации пользователи сайта SharePoint также могут видеть обновления документов области людей и другие действия этого пользователя на сайте SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3b17a-108">In an organizational environment, users on a SharePoint site can also see in the People Pane document updates and other site activities of this person on the SharePoint site.</span></span>
  
<span data-ttu-id="3b17a-109">Социальная сеть может разработать поставщика для OSC для синхронизации и создания обновлений социальных сетей на вспомогательных серверах и в приложениях.</span><span class="sxs-lookup"><span data-stu-id="3b17a-109">A social network can develop a provider for the OSC to synchronize and surface social network updates in supporting servers and applications.</span></span> <span data-ttu-id="3b17a-110">Популярные социальные сети, такие как LinkedIn, Facebook и Windows Live, предлагают поставщиков для OSC.</span><span class="sxs-lookup"><span data-stu-id="3b17a-110">Popular social networks such as LinkedIn, Facebook, and Windows Live are offering providers for the OSC.</span></span> 
  
<span data-ttu-id="3b17a-111">В справочнике по поставщикам Outlook Social Connector 2013 описывается разработка поставщика OSC с использованием возможности extensibility поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="3b17a-111">The Outlook Social Connector 2013 Provider Reference describes how to develop an OSC provider using OSC provider extensibility.</span></span> 
  
<span data-ttu-id="3b17a-112">Если у вас нет опыта разработки решений для Outlook, см. статью [Выбор API или технологии разработки решений для Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md), чтобы выбрать API-интерфейсы и технологии, наиболее соответствующие вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="3b17a-112">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="3b17a-113">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="3b17a-113">In this section</span></span>

- <span data-ttu-id="3b17a-114">Начало работы с разработкой поставщика [Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md): обзор OSC, в том числе: как поставщик OSC может быть полезным, быстрые шаги для изучения разработки поставщика, технические требования, советы и новые возможности в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="3b17a-114">[Getting Started with Developing an Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md): Provides an overview of the OSC, including the following: how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span>
    
- <span data-ttu-id="3b17a-115">[Примеры шаблонов OSC](osc-sample-templates.md): описание Visual Studio шаблонов для разработки поставщика.</span><span class="sxs-lookup"><span data-stu-id="3b17a-115">[OSC Sample Templates](osc-sample-templates.md): Describes several Visual Studio templates for developing a provider.</span></span>
    
- <span data-ttu-id="3b17a-116">Типичные последовательности [вызовов OSC](osc-typical-calling-sequences.md): описывает несколько типичных последовательностей вызовов osC членов в интерфейсах extensibility поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="3b17a-116">[OSC Typical Calling Sequences](osc-typical-calling-sequences.md): Describes a few typical calling sequences by the OSC of members in the OSC provider extensibility interfaces.</span></span> <span data-ttu-id="3b17a-117">Это позволит лучше понять, как реализовать эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="3b17a-117">This should enable you to better understand how to implement these interfaces.</span></span>
    
- <span data-ttu-id="3b17a-118">Разработка поставщика с помощью схемы [OSC XML](developing-a-provider-with-the-osc-xml-schema.md): описывает, как интерфейсы extensibility поставщика OSC и схема OSC XML предназначены для поддержки поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="3b17a-118">[Developing a Provider with the OSC XML Schema](developing-a-provider-with-the-osc-xml-schema.md): Describes how the OSC provider extensibility interfaces and OSC XML schema are designed to support an OSC provider.</span></span>
    
- <span data-ttu-id="3b17a-119">[Отладка поставщика:](debugging-a-provider.md)предлагает несколько способов отладки поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="3b17a-119">[Debugging a Provider](debugging-a-provider.md): Suggests a few ways to help debug an OSC provider.</span></span>
    
- <span data-ttu-id="3b17a-120">[Развертывание поставщика](deploying-a-provider.md): описывает требования к регистрации для поставщика OSC и предоставляет контрольный список для установки поставщика.</span><span class="sxs-lookup"><span data-stu-id="3b17a-120">[Deploying a Provider](deploying-a-provider.md): Describes registration requirements for an OSC provider, and provides a checklist for installing a provider.</span></span>
    
- <span data-ttu-id="3b17a-121">[Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md): Suggests tests you can do before releaseing an OSC provider.</span><span class="sxs-lookup"><span data-stu-id="3b17a-121">[Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md): Suggests tests you can do before releasing an OSC provider.</span></span>
    
- <span data-ttu-id="3b17a-122">[Outlook Social Connector Provider Reference](outlook-social-connector-provider-reference-0.md): Provides reference information for the OSC provider extensibility interfaces and OSC XML schema, and lists possible error codes.</span><span class="sxs-lookup"><span data-stu-id="3b17a-122">[Outlook Social Connector Provider Reference](outlook-social-connector-provider-reference-0.md): Provides reference information for the OSC provider extensibility interfaces and OSC XML schema, and lists possible error codes.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3b17a-123">См. также</span><span class="sxs-lookup"><span data-stu-id="3b17a-123">See also</span></span>

- [<span data-ttu-id="3b17a-124">Уведомление об авторских правах для поставщика Outlook Social Connector 2013</span><span class="sxs-lookup"><span data-stu-id="3b17a-124">Outlook Social Connector 2013 provider reference copyright notice</span></span>](outlook-social-connector-2013-provider-reference-copyright-notice.md) 
- [<span data-ttu-id="3b17a-125">Условные обозначения в документах (Возможно, на английском языке)</span><span class="sxs-lookup"><span data-stu-id="3b17a-125">Document Conventions</span></span>](https://msdn.microsoft.com/office/aa905365.aspx)   
- [<span data-ttu-id="3b17a-126">Специальные возможности в продуктах Майкрософт (Возможно, на английском языке)</span><span class="sxs-lookup"><span data-stu-id="3b17a-126">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/enable/products/default.aspx)  
- [<span data-ttu-id="3b17a-127">Уведомление о конфиденциальности (Майкрософт), доступное в Интернете</span><span class="sxs-lookup"><span data-stu-id="3b17a-127">Microsoft Online Privacy Notice</span></span>](https://privacy.microsoft.com/en-us/privacystatement)
    

