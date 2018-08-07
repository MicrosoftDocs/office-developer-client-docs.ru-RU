---
title: Краткое руководство по разработке поставщика
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: В данном разделе приводятся некоторые действия, чтобы узнать о разработки поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 345e8600c704504be091ee23c66b7f85575cde90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812835"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a><span data-ttu-id="720ca-103">Краткое руководство по разработке поставщика</span><span class="sxs-lookup"><span data-stu-id="720ca-103">Quick steps for learning to develop a provider</span></span>

<span data-ttu-id="720ca-104">Разработка поставщика OSC, необходимо выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="720ca-104">To develop an OSC provider, you need to complete the following general steps:</span></span>
  
- <span data-ttu-id="720ca-105">Реализация четыре обязательные интерфейсы: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)и [ISocialPerson](isocialpersoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="720ca-105">Implement the four mandatory interfaces: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), and [ISocialPerson](isocialpersoniunknown.md).</span></span> <span data-ttu-id="720ca-106">В зависимости от поддержки социальной сети для кэширования учетные данные для входа, отслеживание человека на социальные сети, или динамически синхронизации друзей и их действий требуется реализовать интерфейс [ISocialSession2](isocialsession2iunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="720ca-106">Depending on your social network's support for caching logon credentials, following a person on the social network, or dynamically synchronizing friends and their activities, you might want to implement the [ISocialSession2](isocialsession2iunknown.md) interface.</span></span> 
    
- <span data-ttu-id="720ca-107">В рамках реализации интерфейсов тестирование и отладка поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="720ca-107">In parallel with implementing interfaces, test and debug the OSC provider.</span></span> 

- <span data-ttu-id="720ca-108">Развертывание поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="720ca-108">Deploy the OSC provider.</span></span>  

- <span data-ttu-id="720ca-109">Выполните окончательный тестирование перед выпуском.</span><span class="sxs-lookup"><span data-stu-id="720ca-109">Do final testing before release.</span></span>
    
## <a name="step-a-implementing-interfaces"></a><span data-ttu-id="720ca-110">Шаг а: реализация интерфейсов</span><span class="sxs-lookup"><span data-stu-id="720ca-110">Step A: Implementing interfaces</span></span>

<span data-ttu-id="720ca-111">Поставщика OSC реализует интерфейсы, чтобы OSC могут использовать эти интерфейсы для получения необходимых сведений о или из социальных сетей через поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="720ca-111">An OSC provider implements interfaces so that the OSC can use these interfaces to obtain necessary information about or from the social network, through the OSC provider.</span></span> <span data-ttu-id="720ca-112">Такая информация включает в себя следующее:</span><span class="sxs-lookup"><span data-stu-id="720ca-112">Such information includes the following:</span></span>
  
- <span data-ttu-id="720ca-113">Как представить диалоговое окно входа в систему учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="720ca-113">How to present the account logon dialog to a user.</span></span>    
- <span data-ttu-id="720ca-114">Поставщик поддерживает ли отображение друзей или действия, которые отображаются в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="720ca-114">Whether the provider supports showing friends or activities as displayed on the social network.</span></span>    
- <span data-ttu-id="720ca-115">Способ отображения друзей и действий в карточке контакта или области пользователей Outlook.</span><span class="sxs-lookup"><span data-stu-id="720ca-115">How to display friends and activities in the Contact Card or Outlook People Pane.</span></span>     
- <span data-ttu-id="720ca-116">Когда следует обновить данные о друзьях или действия в карточке контакта или в области пользователей.</span><span class="sxs-lookup"><span data-stu-id="720ca-116">When to refresh friends or activities information on the Contact Card or People Pane.</span></span>
    
<span data-ttu-id="720ca-117">Сведения о обычно передается от поставщика OSC в виде строки XML как выходные параметры методов интерфейса.</span><span class="sxs-lookup"><span data-stu-id="720ca-117">The information is typically passed from the provider to the OSC, in the form of XML strings as output parameters of interface methods.</span></span> <span data-ttu-id="720ca-118">OSC и поставщика OSC соответствует схеме XML поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="720ca-118">Both the OSC and an OSC provider comply with the OSC provider XML schema.</span></span> <span data-ttu-id="720ca-119">Таким образом в реализации интерфейсов, необходимо понять, как XML-схему позволяет указать сведения, как указано выше.</span><span class="sxs-lookup"><span data-stu-id="720ca-119">Therefore, in the course of implementing the interfaces, you need a good understanding of how the XML schema allows you to specify information as listed above.</span></span> 

<span data-ttu-id="720ca-120">Ознакомьтесь со следующими ресурсами объясняется, как указать XML для возможности поставщика, друзей и действий:</span><span class="sxs-lookup"><span data-stu-id="720ca-120">The following resources explain how to specify XML for provider capabilities, friends, and activities:</span></span>
  
- [<span data-ttu-id="720ca-121">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="720ca-121">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)    
- [<span data-ttu-id="720ca-122">Синхронизация друзей и действия</span><span class="sxs-lookup"><span data-stu-id="720ca-122">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)    
- [<span data-ttu-id="720ca-123">Пример возможности XML</span><span class="sxs-lookup"><span data-stu-id="720ca-123">Capabilities XML Example</span></span>](capabilities-xml-example.md)   
- [<span data-ttu-id="720ca-124">XML-код для возможности</span><span class="sxs-lookup"><span data-stu-id="720ca-124">XML for Capabilities</span></span>](xml-for-capabilities.md)    
- [<span data-ttu-id="720ca-125">Пример XML друзей</span><span class="sxs-lookup"><span data-stu-id="720ca-125">Friends XML Example</span></span>](friends-xml-example.md)    
- [<span data-ttu-id="720ca-126">XML-код для друзей</span><span class="sxs-lookup"><span data-stu-id="720ca-126">XML for Friends</span></span>](xml-for-friends.md)   
- [<span data-ttu-id="720ca-127">Пример XML веб-канала активности</span><span class="sxs-lookup"><span data-stu-id="720ca-127">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)   
- [<span data-ttu-id="720ca-128">XML-код для действия</span><span class="sxs-lookup"><span data-stu-id="720ca-128">XML for Activities</span></span>](xml-for-activities.md)
    
<span data-ttu-id="720ca-129">Прежде чем начать реализации, также можно найти следующие разделы для экономии времени в процесс отладки.</span><span class="sxs-lookup"><span data-stu-id="720ca-129">Before you start implementation, also consult the following topics to save you time later in the debugging process:</span></span>
  
- [<span data-ttu-id="720ca-130">Технические требования</span><span class="sxs-lookup"><span data-stu-id="720ca-130">Technical Requirements</span></span>](technical-requirements.md)    
- [<span data-ttu-id="720ca-131">Рекомендации по разработке поставщика</span><span class="sxs-lookup"><span data-stu-id="720ca-131">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)    
- [<span data-ttu-id="720ca-132">Шаблоны OSC примера</span><span class="sxs-lookup"><span data-stu-id="720ca-132">OSC Sample Templates</span></span>](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a><span data-ttu-id="720ca-133">Отладка Шаг б.</span><span class="sxs-lookup"><span data-stu-id="720ca-133">Step B: Debugging</span></span>

<span data-ttu-id="720ca-134">Раздел [Отладка поставщика](debugging-a-provider.md) предлагает отладку процедур, которые можно использовать при разработке поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="720ca-134">The topic [Debugging a Provider](debugging-a-provider.md) suggests debugging procedures you can use while developing an OSC provider.</span></span> 
  
<span data-ttu-id="720ca-135">При разработке, также можно обратиться к и [Подготовка к выпуску поставщика OSC](getting-ready-to-release-an-osc-provider.md) лучше понимать поведение характерно для некоторых сценариях (например, основной и на основе форм проверки подлинности).</span><span class="sxs-lookup"><span data-stu-id="720ca-135">While you are developing, you can also refer to [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md) to gain a better understanding of the expected behavior in certain scenarios (for example, basic and forms-based authentication).</span></span> 
  
## <a name="step-c-deploying"></a><span data-ttu-id="720ca-136">Развертывание шаг C:</span><span class="sxs-lookup"><span data-stu-id="720ca-136">Step C: Deploying</span></span>

<span data-ttu-id="720ca-137">Содержатся в следующих разделах, чтобы узнать о требованиях к развертыванию:</span><span class="sxs-lookup"><span data-stu-id="720ca-137">See the following topics to learn about deployment requirements:</span></span>
  
- [<span data-ttu-id="720ca-138">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="720ca-138">Deploying a Provider</span></span>](deploying-a-provider.md)    
- [<span data-ttu-id="720ca-139">Регистрация поставщика</span><span class="sxs-lookup"><span data-stu-id="720ca-139">Registering a Provider</span></span>](registering-a-provider.md)   
- [<span data-ttu-id="720ca-140">Контрольный список установки</span><span class="sxs-lookup"><span data-stu-id="720ca-140">Installation Checklist</span></span>](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a><span data-ttu-id="720ca-141">Шаг D: тестирование перед выпуском последний</span><span class="sxs-lookup"><span data-stu-id="720ca-141">Step D: Final testing before release</span></span>

<span data-ttu-id="720ca-142">В зависимости от социальной сети и поставщика OSC существует обычно поставщика тестов, необходимо выполнить перед выпуском ваш поставщик.</span><span class="sxs-lookup"><span data-stu-id="720ca-142">Depending on your social network and the OSC provider, there are usually provider-specific tests you should carry out before you release your provider.</span></span> <span data-ttu-id="720ca-143">Предлагаемые список тестов в разделе [Подготовка к выпуску поставщика OSC](getting-ready-to-release-an-osc-provider.md).</span><span class="sxs-lookup"><span data-stu-id="720ca-143">For a suggested list of tests, see [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="720ca-144">См. также</span><span class="sxs-lookup"><span data-stu-id="720ca-144">See also</span></span>

- [<span data-ttu-id="720ca-145">Начало разработки поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="720ca-145">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

