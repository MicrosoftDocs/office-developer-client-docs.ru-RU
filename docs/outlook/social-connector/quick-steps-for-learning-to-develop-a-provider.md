---
title: Краткое руководство по разработке поставщика
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: В этом разделе предлагается несколько действий, чтобы узнать о разработке поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 581997ab257d59062761d97bfef49a88b90bb1e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424219"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a><span data-ttu-id="99caa-103">Краткое руководство по разработке поставщика</span><span class="sxs-lookup"><span data-stu-id="99caa-103">Quick steps for learning to develop a provider</span></span>

<span data-ttu-id="99caa-104">Чтобы разработать поставщика OSC, необходимо выполнить следующие общие действия:</span><span class="sxs-lookup"><span data-stu-id="99caa-104">To develop an OSC provider, you need to complete the following general steps:</span></span>
  
- <span data-ttu-id="99caa-105">Реализуют четыре обязательных интерфейса: [ISocialProvider,](isocialprovideriunknown.md) [ISocialSession,](isocialsessioniunknown.md) [ISocialProfile](isocialprofileisocialperson.md)и [ISocialPerson.](isocialpersoniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="99caa-105">Implement the four mandatory interfaces: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), and [ISocialPerson](isocialpersoniunknown.md).</span></span> <span data-ttu-id="99caa-106">В зависимости от поддержки вашей социальной сети для кэшации учетных данных для входа, после пользователя в социальной сети или динамической синхронизации друзей и их действий, может потребоваться реализовать [интерфейс ISocialSession2.](isocialsession2iunknown.md)</span><span class="sxs-lookup"><span data-stu-id="99caa-106">Depending on your social network's support for caching logon credentials, following a person on the social network, or dynamically synchronizing friends and their activities, you might want to implement the [ISocialSession2](isocialsession2iunknown.md) interface.</span></span> 
    
- <span data-ttu-id="99caa-107">Параллельно с реализацией интерфейсов протестировать и отлалать поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="99caa-107">In parallel with implementing interfaces, test and debug the OSC provider.</span></span> 

- <span data-ttu-id="99caa-108">Развертывание поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="99caa-108">Deploy the OSC provider.</span></span>  

- <span data-ttu-id="99caa-109">Завершите тестирование перед выпуском.</span><span class="sxs-lookup"><span data-stu-id="99caa-109">Do final testing before release.</span></span>
    
## <a name="step-a-implementing-interfaces"></a><span data-ttu-id="99caa-110">Шаг А. Реализация интерфейсов</span><span class="sxs-lookup"><span data-stu-id="99caa-110">Step A: Implementing interfaces</span></span>

<span data-ttu-id="99caa-111">Поставщик OSC реализует интерфейсы, чтобы osC могли использовать эти интерфейсы для получения необходимой информации о социальных сетях или из нее через поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="99caa-111">An OSC provider implements interfaces so that the OSC can use these interfaces to obtain necessary information about or from the social network, through the OSC provider.</span></span> <span data-ttu-id="99caa-112">К таким сведениям относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="99caa-112">Such information includes the following:</span></span>
  
- <span data-ttu-id="99caa-113">Как представить пользователю диалоговое окно для учетной записи для пользователя.</span><span class="sxs-lookup"><span data-stu-id="99caa-113">How to present the account logon dialog to a user.</span></span>    
- <span data-ttu-id="99caa-114">Поддерживает ли поставщик отображение друзей или действий в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="99caa-114">Whether the provider supports showing friends or activities as displayed on the social network.</span></span>    
- <span data-ttu-id="99caa-115">Отображение друзей и действий в карточке контакта или области людей Outlook.</span><span class="sxs-lookup"><span data-stu-id="99caa-115">How to display friends and activities in the Contact Card or Outlook People Pane.</span></span>     
- <span data-ttu-id="99caa-116">Когда обновлять сведения о друзьях или действиях на карточке контакта или в области "Люди".</span><span class="sxs-lookup"><span data-stu-id="99caa-116">When to refresh friends or activities information on the Contact Card or People Pane.</span></span>
    
<span data-ttu-id="99caa-117">Как правило, сведения передаются от поставщика в OSC в виде строк XML в качестве выходных параметров методов интерфейса.</span><span class="sxs-lookup"><span data-stu-id="99caa-117">The information is typically passed from the provider to the OSC, in the form of XML strings as output parameters of interface methods.</span></span> <span data-ttu-id="99caa-118">OsC и поставщик OSC соответствуют XML-схеме поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="99caa-118">Both the OSC and an OSC provider comply with the OSC provider XML schema.</span></span> <span data-ttu-id="99caa-119">Поэтому в процессе реализации интерфейсов необходимо хорошо понимать, как схема XML позволяет указать сведения, указанные выше.</span><span class="sxs-lookup"><span data-stu-id="99caa-119">Therefore, in the course of implementing the interfaces, you need a good understanding of how the XML schema allows you to specify information as listed above.</span></span> 

<span data-ttu-id="99caa-120">В следующих ресурсах объясняется, как указать XML для возможностей поставщика, друзей и действий:</span><span class="sxs-lookup"><span data-stu-id="99caa-120">The following resources explain how to specify XML for provider capabilities, friends, and activities:</span></span>
  
- [<span data-ttu-id="99caa-121">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="99caa-121">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)    
- [<span data-ttu-id="99caa-122">Синхронизация друзей и действий</span><span class="sxs-lookup"><span data-stu-id="99caa-122">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)    
- [<span data-ttu-id="99caa-123">XML-пример возможностей</span><span class="sxs-lookup"><span data-stu-id="99caa-123">Capabilities XML Example</span></span>](capabilities-xml-example.md)   
- [<span data-ttu-id="99caa-124">XML для возможностей</span><span class="sxs-lookup"><span data-stu-id="99caa-124">XML for Capabilities</span></span>](xml-for-capabilities.md)    
- [<span data-ttu-id="99caa-125">Пример XML-разных друзей</span><span class="sxs-lookup"><span data-stu-id="99caa-125">Friends XML Example</span></span>](friends-xml-example.md)    
- [<span data-ttu-id="99caa-126">XML для друзей</span><span class="sxs-lookup"><span data-stu-id="99caa-126">XML for Friends</span></span>](xml-for-friends.md)   
- [<span data-ttu-id="99caa-127">Пример XML-канала активности</span><span class="sxs-lookup"><span data-stu-id="99caa-127">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)   
- [<span data-ttu-id="99caa-128">XML для действий</span><span class="sxs-lookup"><span data-stu-id="99caa-128">XML for Activities</span></span>](xml-for-activities.md)
    
<span data-ttu-id="99caa-129">Перед началом реализации также проконсультируйтесь со следующими разделами, чтобы сэкономить время в процессе отладки:</span><span class="sxs-lookup"><span data-stu-id="99caa-129">Before you start implementation, also consult the following topics to save you time later in the debugging process:</span></span>
  
- [<span data-ttu-id="99caa-130">Технические требования</span><span class="sxs-lookup"><span data-stu-id="99caa-130">Technical Requirements</span></span>](technical-requirements.md)    
- [<span data-ttu-id="99caa-131">Best Practices for Developing a Provider</span><span class="sxs-lookup"><span data-stu-id="99caa-131">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)    
- [<span data-ttu-id="99caa-132">Примеры шаблонов OSC</span><span class="sxs-lookup"><span data-stu-id="99caa-132">OSC Sample Templates</span></span>](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a><span data-ttu-id="99caa-133">Шаг Б. Отладка</span><span class="sxs-lookup"><span data-stu-id="99caa-133">Step B: Debugging</span></span>

<span data-ttu-id="99caa-134">В разделе ["Отладка поставщика"](debugging-a-provider.md) предложены процедуры отладки, которые можно использовать при разработке поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="99caa-134">The topic [Debugging a Provider](debugging-a-provider.md) suggests debugging procedures you can use while developing an OSC provider.</span></span> 
  
<span data-ttu-id="99caa-135">Во время разработки вы также можете сослаться на статью "Готовность к выпуску поставщика [OSC",](getting-ready-to-release-an-osc-provider.md) чтобы лучше понять ожидаемое поведение в определенных сценариях (например, при базовой и проверке подлинности на основе форм).</span><span class="sxs-lookup"><span data-stu-id="99caa-135">While you are developing, you can also refer to [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md) to gain a better understanding of the expected behavior in certain scenarios (for example, basic and forms-based authentication).</span></span> 
  
## <a name="step-c-deploying"></a><span data-ttu-id="99caa-136">Шаг C. Развертывание</span><span class="sxs-lookup"><span data-stu-id="99caa-136">Step C: Deploying</span></span>

<span data-ttu-id="99caa-137">Чтобы узнать о требованиях к развертыванию, см. следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="99caa-137">See the following topics to learn about deployment requirements:</span></span>
  
- [<span data-ttu-id="99caa-138">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="99caa-138">Deploying a Provider</span></span>](deploying-a-provider.md)    
- [<span data-ttu-id="99caa-139">Регистрация поставщика</span><span class="sxs-lookup"><span data-stu-id="99caa-139">Registering a Provider</span></span>](registering-a-provider.md)   
- [<span data-ttu-id="99caa-140">Контрольный список установки</span><span class="sxs-lookup"><span data-stu-id="99caa-140">Installation Checklist</span></span>](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a><span data-ttu-id="99caa-141">Шаг D. Окончательное тестирование перед выпуском</span><span class="sxs-lookup"><span data-stu-id="99caa-141">Step D: Final testing before release</span></span>

<span data-ttu-id="99caa-142">В зависимости от социальной сети и поставщика OSC обычно существуют специальные тесты, которые необходимо выполнить перед выпуском поставщика.</span><span class="sxs-lookup"><span data-stu-id="99caa-142">Depending on your social network and the OSC provider, there are usually provider-specific tests you should carry out before you release your provider.</span></span> <span data-ttu-id="99caa-143">Рекомендуемый список тестов см. в [подготовии к выпуску поставщика OSC.](getting-ready-to-release-an-osc-provider.md)</span><span class="sxs-lookup"><span data-stu-id="99caa-143">For a suggested list of tests, see [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="99caa-144">См. также</span><span class="sxs-lookup"><span data-stu-id="99caa-144">See also</span></span>

- [<span data-ttu-id="99caa-145">Начало разработки поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="99caa-145">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

