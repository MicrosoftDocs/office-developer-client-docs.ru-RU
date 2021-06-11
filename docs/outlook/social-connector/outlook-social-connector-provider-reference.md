---
title: Справочник по поставщикам Outlook Social Connector
manager: soliver
ms.date: 04/04/2016
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13661393-adf6-4870-86c4-303262317675
description: Центр Outlook Social Connector 2013 предоставляет центр связи для личных и профессиональных коммуникаций.
ms.openlocfilehash: e570fe69cbbe0e8d472e712fb3b8592c97fe43c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359838"
---
# <a name="outlook-social-connector-provider-reference"></a><span data-ttu-id="8dc97-103">Справочник по поставщикам Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="8dc97-103">Outlook Social Connector provider reference</span></span>

<span data-ttu-id="8dc97-104">Центр Outlook Social Connector 2013 предоставляет центр связи для личных и профессиональных коммуникаций.</span><span class="sxs-lookup"><span data-stu-id="8dc97-104">The Outlook Social Connector 2013 provides a communication hub for personal and professional communications.</span></span> <span data-ttu-id="8dc97-105">Социальный соединитатель Outlook (OSC) работает с SharePoint Server, SharePoint Workspace, клиентом Lync и всеми Office-приложениями, которые поддерживают сведения о присутствии и поддерживают контактную карту OSC.</span><span class="sxs-lookup"><span data-stu-id="8dc97-105">The Outlook Social Connector (OSC) works with SharePoint Server, SharePoint Workspace, Lync client, and all Office client applications that support presence information and the Contact Card support the OSC.</span></span> 

<span data-ttu-id="8dc97-106">В Outlook частности, просто выбрав элемент Outlook, например запрос электронной почты или собрания и щелкнув отправитель или получатель в этом элементе, не покидая Outlook, пользователи могут видеть в действиях, фотографиях и обновлениях состояния этого человека в своих любимых социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="8dc97-106">In Outlook in particular, just by selecting an Outlook item such as an email or meeting request and clicking the sender or a recipient in that item, without leaving Outlook, users can see in the People Pane activities, photos, and status updates of this person on their favorite social networks.</span></span> <span data-ttu-id="8dc97-107">Пользователи могут удобно видеть все электронные Outlook, вложения и собрания, полученные от этого человека.</span><span class="sxs-lookup"><span data-stu-id="8dc97-107">Users can conveniently see all the Outlook emails, attachments, and meetings received from this person.</span></span> <span data-ttu-id="8dc97-108">В организационной среде пользователи SharePoint сайта также могут видеть обновления документов в области людей и другие действия этого пользователя на SharePoint сайте.</span><span class="sxs-lookup"><span data-stu-id="8dc97-108">In an organizational environment, users on a SharePoint site can also see in the People Pane document updates and other site activities of this person on the SharePoint site.</span></span>
  
<span data-ttu-id="8dc97-109">Социальная сеть может разработать поставщика для osC для синхронизации и поверхностных обновлений социальных сетей в поддержке серверов и приложений.</span><span class="sxs-lookup"><span data-stu-id="8dc97-109">A social network can develop a provider for the OSC to synchronize and surface social network updates in supporting servers and applications.</span></span> <span data-ttu-id="8dc97-110">Популярные социальные сети, такие как LinkedIn, Facebook и Windows Live, предлагают поставщиков для OSC.</span><span class="sxs-lookup"><span data-stu-id="8dc97-110">Popular social networks such as LinkedIn, Facebook, and Windows Live are offering providers for the OSC.</span></span> 
  
<span data-ttu-id="8dc97-111">В Outlook Social Connector 2013 Provider Reference описывается, как разработать поставщика OSC с помощью extensibility поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="8dc97-111">The Outlook Social Connector 2013 Provider Reference describes how to develop an OSC provider using OSC provider extensibility.</span></span> 
  
<span data-ttu-id="8dc97-112">Если у вас нет опыта разработки решений для Outlook, см. статью [Выбор API или технологии разработки решений для Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md), чтобы выбрать API-интерфейсы и технологии, наиболее соответствующие вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="8dc97-112">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="8dc97-113">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="8dc97-113">In this section</span></span>

- <span data-ttu-id="8dc97-114">Начало работы с разработкой [Outlook](getting-started-with-developing-an-outlook-social-connector-provider.md)поставщика социальных соединители: предоставляет обзор OSC, в том числе следующие: как поставщик OSC может быть полезным, быстрые шаги для обучения разработке поставщика, технические требования, лучшие практики для разработки поставщика, и что нового в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="8dc97-114">[Getting Started with Developing an Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md): Provides an overview of the OSC, including the following: how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span>
    
- <span data-ttu-id="8dc97-115">[Шаблоны образцов OSC:](osc-sample-templates.md)описывает несколько Visual Studio шаблонов для разработки поставщика.</span><span class="sxs-lookup"><span data-stu-id="8dc97-115">[OSC Sample Templates](osc-sample-templates.md): Describes several Visual Studio templates for developing a provider.</span></span>
    
- <span data-ttu-id="8dc97-116">[Типичные последовательности](osc-typical-calling-sequences.md)вызовов OSC: Описывает несколько типичных последовательностей вызовов, которые osC членов в интерфейсах extensibility поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="8dc97-116">[OSC Typical Calling Sequences](osc-typical-calling-sequences.md): Describes a few typical calling sequences by the OSC of members in the OSC provider extensibility interfaces.</span></span> <span data-ttu-id="8dc97-117">Это позволит вам лучше понять, как реализовать эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="8dc97-117">This should enable you to better understand how to implement these interfaces.</span></span>
    
- <span data-ttu-id="8dc97-118">Разработка поставщика с помощью [схемы XML OSC](developing-a-provider-with-the-osc-xml-schema.md): Описывает, как интерфейсы extensibility поставщика OSC и схема XML OSC предназначены для поддержки поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="8dc97-118">[Developing a Provider with the OSC XML Schema](developing-a-provider-with-the-osc-xml-schema.md): Describes how the OSC provider extensibility interfaces and OSC XML schema are designed to support an OSC provider.</span></span>
    
- <span data-ttu-id="8dc97-119">[Отладка поставщика:](debugging-a-provider.md)предлагает несколько способов помочь отладке поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="8dc97-119">[Debugging a Provider](debugging-a-provider.md): Suggests a few ways to help debug an OSC provider.</span></span>
    
- <span data-ttu-id="8dc97-120">[Развертывание поставщика:](deploying-a-provider.md)описывает требования к регистрации для поставщика OSC и предоставляет контрольный список для установки поставщика.</span><span class="sxs-lookup"><span data-stu-id="8dc97-120">[Deploying a Provider](deploying-a-provider.md): Describes registration requirements for an OSC provider, and provides a checklist for installing a provider.</span></span>
    
- <span data-ttu-id="8dc97-121">[Получение готовности к выпуску поставщика OSC:](getting-ready-to-release-an-osc-provider.md)предлагает тесты, которые можно сделать перед выпуском поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="8dc97-121">[Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md): Suggests tests you can do before releasing an OSC provider.</span></span>
    
- <span data-ttu-id="8dc97-122">[Outlook](outlook-social-connector-provider-reference-0.md)поставщика социальных соединителем: предоставляет справочные сведения для интерфейсов extensibility поставщика OSC и схемы XML OSC, а также перечисляет возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="8dc97-122">[Outlook Social Connector Provider Reference](outlook-social-connector-provider-reference-0.md): Provides reference information for the OSC provider extensibility interfaces and OSC XML schema, and lists possible error codes.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8dc97-123">См. также</span><span class="sxs-lookup"><span data-stu-id="8dc97-123">See also</span></span>

- [<span data-ttu-id="8dc97-124">Outlook Уведомление об авторском праве поставщика social Connector 2013</span><span class="sxs-lookup"><span data-stu-id="8dc97-124">Outlook Social Connector 2013 provider reference copyright notice</span></span>](outlook-social-connector-2013-provider-reference-copyright-notice.md) 
- [<span data-ttu-id="8dc97-125">Условные обозначения в документах (Возможно, на английском языке)</span><span class="sxs-lookup"><span data-stu-id="8dc97-125">Document Conventions</span></span>](https://msdn.microsoft.com/office/aa905365.aspx)   
- [<span data-ttu-id="8dc97-126">Специальные возможности в продуктах Майкрософт (Возможно, на английском языке)</span><span class="sxs-lookup"><span data-stu-id="8dc97-126">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/enable/products/default.aspx)  
- [<span data-ttu-id="8dc97-127">Уведомление о конфиденциальности (Майкрософт), доступное в Интернете</span><span class="sxs-lookup"><span data-stu-id="8dc97-127">Microsoft Online Privacy Notice</span></span>](https://privacy.microsoft.com/en-us/privacystatement)
    

