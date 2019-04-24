---
title: Справочник по поставщикам Outlook Social Connector
manager: soliver
ms.date: 04/04/2016
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13661393-adf6-4870-86c4-303262317675
description: Outlook Social Connector 2013 предоставляет концентратор для общения персональных и профессиональных коммуникаций.
ms.openlocfilehash: e570fe69cbbe0e8d472e712fb3b8592c97fe43c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359838"
---
# <a name="outlook-social-connector-provider-reference"></a><span data-ttu-id="0ef89-103">Справочник по поставщикам Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="0ef89-103">Outlook Social Connector provider reference</span></span>

<span data-ttu-id="0ef89-104">Outlook Social Connector 2013 предоставляет концентратор для общения персональных и профессиональных коммуникаций.</span><span class="sxs-lookup"><span data-stu-id="0ef89-104">The Outlook Social Connector 2013 provides a communication hub for personal and professional communications.</span></span> <span data-ttu-id="0ef89-105">Outlook Social Connector (OSC) работает с SharePoint Server, SharePoint Workspace, Lync Client и всеми клиентскими приложениями Office, которые поддерживают сведения о присутствии и карточке контакта, поддерживающие OSC.</span><span class="sxs-lookup"><span data-stu-id="0ef89-105">The Outlook Social Connector (OSC) works with SharePoint Server, SharePoint Workspace, Lync client, and all Office client applications that support presence information and the Contact Card support the OSC.</span></span> 

<span data-ttu-id="0ef89-106">В Outlook в частности, выбрав элемент Outlook (например, приглашение на собрание или приглашение на собрание) и щелкнув отправителя или получателя в этом элементе, не выходя из Outlook, пользователи могут видеть в области людей действия, фотографии и обновления состояния этого пользователя Избранные социальные сети.</span><span class="sxs-lookup"><span data-stu-id="0ef89-106">In Outlook in particular, just by selecting an Outlook item such as an email or meeting request and clicking the sender or a recipient in that item, without leaving Outlook, users can see in the People Pane activities, photos, and status updates of this person on their favorite social networks.</span></span> <span data-ttu-id="0ef89-107">Пользователи могут удобно видеть все сообщения электронной почты, вложения и собрания Outlook, полученные от этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="0ef89-107">Users can conveniently see all the Outlook emails, attachments, and meetings received from this person.</span></span> <span data-ttu-id="0ef89-108">В организационной среде пользователи на сайте SharePoint также могут отображаться в области Пользователи, а другие действия этого пользователя — на сайте SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0ef89-108">In an organizational environment, users on a SharePoint site can also see in the People Pane document updates and other site activities of this person on the SharePoint site.</span></span>
  
<span data-ttu-id="0ef89-109">Социальные сети могут разрабатывать поставщик OSC для синхронизации и поповерхностных обновлений социальных сетей в поддерживающих серверах и приложениях.</span><span class="sxs-lookup"><span data-stu-id="0ef89-109">A social network can develop a provider for the OSC to synchronize and surface social network updates in supporting servers and applications.</span></span> <span data-ttu-id="0ef89-110">Популярные социальные сети, такие как LinkedIn, Facebook и Windows Live, предлагают поставщиков для OSC.</span><span class="sxs-lookup"><span data-stu-id="0ef89-110">Popular social networks such as LinkedIn, Facebook, and Windows Live are offering providers for the OSC.</span></span> 
  
<span data-ttu-id="0ef89-111">В справочнике по поставщику Outlook Social Connector 2013 описывается разработка поставщика OSC с помощью расширяемости поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="0ef89-111">The Outlook Social Connector 2013 Provider Reference describes how to develop an OSC provider using OSC provider extensibility.</span></span> 
  
<span data-ttu-id="0ef89-112">Если у вас нет опыта разработки решений для Outlook, см. статью [Выбор API или технологии разработки решений для Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md), чтобы выбрать API-интерфейсы и технологии, наиболее соответствующие вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="0ef89-112">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="0ef89-113">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="0ef89-113">In this section</span></span>

- <span data-ttu-id="0ef89-114">[Приступая к разработке поставщика Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md): предоставляет обзор OSC, включая следующие материалы: как поставщик OSC может быть полезен, краткие инструкции по разработке поставщика, технические требования, рекомендации по Разработка поставщика и новые возможности этого выпуска.</span><span class="sxs-lookup"><span data-stu-id="0ef89-114">[Getting Started with Developing an Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md): Provides an overview of the OSC, including the following: how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span>
    
- <span data-ttu-id="0ef89-115">[Примеры шаблонов OSC](osc-sample-templates.md): описание нескольких шаблонов Visual Studio для разработки поставщика.</span><span class="sxs-lookup"><span data-stu-id="0ef89-115">[OSC Sample Templates](osc-sample-templates.md): Describes several Visual Studio templates for developing a provider.</span></span>
    
- <span data-ttu-id="0ef89-116">[OSC типичНые последовательности вызовов](osc-typical-calling-sequences.md): описывает несколько типичных последовательностей вызовов с помощью OSC элементов в интерфейсах расширения поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="0ef89-116">[OSC Typical Calling Sequences](osc-typical-calling-sequences.md): Describes a few typical calling sequences by the OSC of members in the OSC provider extensibility interfaces.</span></span> <span data-ttu-id="0ef89-117">Это должно помочь вам лучше понять, как реализовать эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="0ef89-117">This should enable you to better understand how to implement these interfaces.</span></span>
    
- <span data-ttu-id="0ef89-118">[Разработка поставщика с помощью XML-схемы OSC](developing-a-provider-with-the-osc-xml-schema.md): в этой статье описано, как интерфейсы и XML-схема OSC для расширения XML-схемы предназначены для поддержки поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="0ef89-118">[Developing a Provider with the OSC XML Schema](developing-a-provider-with-the-osc-xml-schema.md): Describes how the OSC provider extensibility interfaces and OSC XML schema are designed to support an OSC provider.</span></span>
    
- <span data-ttu-id="0ef89-119">[Отладка поставщика](debugging-a-provider.md): предлагается несколько способов отладки поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="0ef89-119">[Debugging a Provider](debugging-a-provider.md): Suggests a few ways to help debug an OSC provider.</span></span>
    
- <span data-ttu-id="0ef89-120">[Развертывание поставщика](deploying-a-provider.md): описывает требования к регистрации для поставщика OSC и предоставляет контрольный список для установки поставщика.</span><span class="sxs-lookup"><span data-stu-id="0ef89-120">[Deploying a Provider](deploying-a-provider.md): Describes registration requirements for an OSC provider, and provides a checklist for installing a provider.</span></span>
    
- <span data-ttu-id="0ef89-121">[Подготовка к выпуску поставщика OSC](getting-ready-to-release-an-osc-provider.md): предлагает тесты, которые можно выполнить перед запуском поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="0ef89-121">[Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md): Suggests tests you can do before releasing an OSC provider.</span></span>
    
- <span data-ttu-id="0ef89-122">[Справочник по поставщику Outlook Social Connector](outlook-social-connector-provider-reference-0.md): содержит справочные сведения о интерфейсах расширяемости поставщиков OSC и XML-схеме OSC, а также список возможных кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="0ef89-122">[Outlook Social Connector Provider Reference](outlook-social-connector-provider-reference-0.md): Provides reference information for the OSC provider extensibility interfaces and OSC XML schema, and lists possible error codes.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ef89-123">См. также</span><span class="sxs-lookup"><span data-stu-id="0ef89-123">See also</span></span>

- [<span data-ttu-id="0ef89-124">Справочник по поставщику Outlook Social Connector 2013 с уведомлением об авторском праве</span><span class="sxs-lookup"><span data-stu-id="0ef89-124">Outlook Social Connector 2013 provider reference copyright notice</span></span>](outlook-social-connector-2013-provider-reference-copyright-notice.md) 
- [<span data-ttu-id="0ef89-125">Условные обозначения в документах (Возможно, на английском языке)</span><span class="sxs-lookup"><span data-stu-id="0ef89-125">Document Conventions</span></span>](https://msdn.microsoft.com/office/aa905365.aspx)   
- [<span data-ttu-id="0ef89-126">Специальные возможности в продуктах Майкрософт (Возможно, на английском языке)</span><span class="sxs-lookup"><span data-stu-id="0ef89-126">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/enable/products/default.aspx)  
- [<span data-ttu-id="0ef89-127">Уведомление о конфиденциальности (Майкрософт), доступное в Интернете</span><span class="sxs-lookup"><span data-stu-id="0ef89-127">Microsoft Online Privacy Notice</span></span>](https://privacy.microsoft.com/en-us/privacystatement)
    

