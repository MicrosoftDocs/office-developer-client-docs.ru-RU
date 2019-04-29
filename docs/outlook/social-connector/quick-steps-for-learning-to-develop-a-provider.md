---
title: Краткое руководство по разработке поставщика
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: В этом разделе предлагается несколько шагов, которые необходимо изучить при разработке поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 581997ab257d59062761d97bfef49a88b90bb1e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424219"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a><span data-ttu-id="14e46-103">Краткое руководство по разработке поставщика</span><span class="sxs-lookup"><span data-stu-id="14e46-103">Quick steps for learning to develop a provider</span></span>

<span data-ttu-id="14e46-104">Для разработки поставщика OSC необходимо выполнить следующие общие действия:</span><span class="sxs-lookup"><span data-stu-id="14e46-104">To develop an OSC provider, you need to complete the following general steps:</span></span>
  
- <span data-ttu-id="14e46-105">Реализуйте четыре обязательных интерфейса: [исоЦиалпровидер](isocialprovideriunknown.md), [настроенный ISocialSession](isocialsessioniunknown.md), [исоЦиалпрофиле](isocialprofileisocialperson.md)и [исоЦиалперсон](isocialpersoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="14e46-105">Implement the four mandatory interfaces: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), and [ISocialPerson](isocialpersoniunknown.md).</span></span> <span data-ttu-id="14e46-106">В зависимости от поддержки кэширования учетных данных для входа в социальной сети, когда пользователь в социальной сети или динамически синхронизирует друзей и их действий, может потребоваться реализация интерфейса [ISocialSession2](isocialsession2iunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="14e46-106">Depending on your social network's support for caching logon credentials, following a person on the social network, or dynamically synchronizing friends and their activities, you might want to implement the [ISocialSession2](isocialsession2iunknown.md) interface.</span></span> 
    
- <span data-ttu-id="14e46-107">Параллельно с реализация интерфейсов — тестирование и Отладка поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="14e46-107">In parallel with implementing interfaces, test and debug the OSC provider.</span></span> 

- <span data-ttu-id="14e46-108">Разверните поставщик OSC.</span><span class="sxs-lookup"><span data-stu-id="14e46-108">Deploy the OSC provider.</span></span>  

- <span data-ttu-id="14e46-109">Выполните окончательную проверку перед выпуском.</span><span class="sxs-lookup"><span data-stu-id="14e46-109">Do final testing before release.</span></span>
    
## <a name="step-a-implementing-interfaces"></a><span data-ttu-id="14e46-110">Этап A: реализация интерфейсов</span><span class="sxs-lookup"><span data-stu-id="14e46-110">Step A: Implementing interfaces</span></span>

<span data-ttu-id="14e46-111">Поставщик OSC реализует интерфейсы, чтобы OSC мог использовать эти интерфейсы для получения необходимой информации или из социальных сетей через поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="14e46-111">An OSC provider implements interfaces so that the OSC can use these interfaces to obtain necessary information about or from the social network, through the OSC provider.</span></span> <span data-ttu-id="14e46-112">Такие сведения включают следующее:</span><span class="sxs-lookup"><span data-stu-id="14e46-112">Such information includes the following:</span></span>
  
- <span data-ttu-id="14e46-113">Отображение диалогового окна входа для учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="14e46-113">How to present the account logon dialog to a user.</span></span>    
- <span data-ttu-id="14e46-114">Поддерживает ли поставщик отображение друзей и действий, отображаемых в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="14e46-114">Whether the provider supports showing friends or activities as displayed on the social network.</span></span>    
- <span data-ttu-id="14e46-115">Отображение друзей и действий в карточке контакта или в области Outlook "люди".</span><span class="sxs-lookup"><span data-stu-id="14e46-115">How to display friends and activities in the Contact Card or Outlook People Pane.</span></span>     
- <span data-ttu-id="14e46-116">Время обновления сведений о друзьях или действиях в карточке контакта или области пользователей.</span><span class="sxs-lookup"><span data-stu-id="14e46-116">When to refresh friends or activities information on the Contact Card or People Pane.</span></span>
    
<span data-ttu-id="14e46-117">Сведения обычно передаются от поставщика к OSC в виде строк XML в качестве выходных параметров методов интерфейса.</span><span class="sxs-lookup"><span data-stu-id="14e46-117">The information is typically passed from the provider to the OSC, in the form of XML strings as output parameters of interface methods.</span></span> <span data-ttu-id="14e46-118">И OSC, и поставщик OSC совместимы с XML-схемой поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="14e46-118">Both the OSC and an OSC provider comply with the OSC provider XML schema.</span></span> <span data-ttu-id="14e46-119">Таким образом, в рамках реализации интерфейсов необходимо хорошо понимать, как схема XML позволяет указать сведения, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="14e46-119">Therefore, in the course of implementing the interfaces, you need a good understanding of how the XML schema allows you to specify information as listed above.</span></span> 

<span data-ttu-id="14e46-120">В следующих ресурсах объясняется, как задать XML для возможностей поставщика, друзей и действий:</span><span class="sxs-lookup"><span data-stu-id="14e46-120">The following resources explain how to specify XML for provider capabilities, friends, and activities:</span></span>
  
- [<span data-ttu-id="14e46-121">ПереOSC типичные последовательности вызовов</span><span class="sxs-lookup"><span data-stu-id="14e46-121">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)    
- [<span data-ttu-id="14e46-122">Синхронизация друзей и действий</span><span class="sxs-lookup"><span data-stu-id="14e46-122">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)    
- [<span data-ttu-id="14e46-123">Пример XML-кода возможностей</span><span class="sxs-lookup"><span data-stu-id="14e46-123">Capabilities XML Example</span></span>](capabilities-xml-example.md)   
- [<span data-ttu-id="14e46-124">XML для возможностей</span><span class="sxs-lookup"><span data-stu-id="14e46-124">XML for Capabilities</span></span>](xml-for-capabilities.md)    
- [<span data-ttu-id="14e46-125">Пример XML-кода друзей</span><span class="sxs-lookup"><span data-stu-id="14e46-125">Friends XML Example</span></span>](friends-xml-example.md)    
- [<span data-ttu-id="14e46-126">XML для друзей</span><span class="sxs-lookup"><span data-stu-id="14e46-126">XML for Friends</span></span>](xml-for-friends.md)   
- [<span data-ttu-id="14e46-127">Пример XML-канала активности</span><span class="sxs-lookup"><span data-stu-id="14e46-127">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)   
- [<span data-ttu-id="14e46-128">XML для действий</span><span class="sxs-lookup"><span data-stu-id="14e46-128">XML for Activities</span></span>](xml-for-activities.md)
    
<span data-ttu-id="14e46-129">Прежде чем приступать к реализации, ознакомьтесь со следующими статьями, чтобы сэкономить время позже в процессе отладки:</span><span class="sxs-lookup"><span data-stu-id="14e46-129">Before you start implementation, also consult the following topics to save you time later in the debugging process:</span></span>
  
- [<span data-ttu-id="14e46-130">Технические требования</span><span class="sxs-lookup"><span data-stu-id="14e46-130">Technical Requirements</span></span>](technical-requirements.md)    
- [<span data-ttu-id="14e46-131">Рекомендации по разработке поставщика</span><span class="sxs-lookup"><span data-stu-id="14e46-131">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)    
- [<span data-ttu-id="14e46-132">Примеры шаблонов OSC</span><span class="sxs-lookup"><span data-stu-id="14e46-132">OSC Sample Templates</span></span>](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a><span data-ttu-id="14e46-133">Шаг B: Отладка</span><span class="sxs-lookup"><span data-stu-id="14e46-133">Step B: Debugging</span></span>

<span data-ttu-id="14e46-134">Раздел [Отладка поставщика](debugging-a-provider.md) предлагает процедуры отладки, которые можно использовать при разработке поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="14e46-134">The topic [Debugging a Provider](debugging-a-provider.md) suggests debugging procedures you can use while developing an OSC provider.</span></span> 
  
<span data-ttu-id="14e46-135">При разработке Вы также можете обратиться к разделу [Подготовка к выпуску поставщика OSC](getting-ready-to-release-an-osc-provider.md) для получения лучшего понимания ожидаемого поведения в определенных сценариях (например, для обычной проверки подлинности на основе форм).</span><span class="sxs-lookup"><span data-stu-id="14e46-135">While you are developing, you can also refer to [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md) to gain a better understanding of the expected behavior in certain scenarios (for example, basic and forms-based authentication).</span></span> 
  
## <a name="step-c-deploying"></a><span data-ttu-id="14e46-136">Шаг C: развертывание</span><span class="sxs-lookup"><span data-stu-id="14e46-136">Step C: Deploying</span></span>

<span data-ttu-id="14e46-137">В следующих разделах приВодятся сведения о требованиях к развертыванию:</span><span class="sxs-lookup"><span data-stu-id="14e46-137">See the following topics to learn about deployment requirements:</span></span>
  
- [<span data-ttu-id="14e46-138">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="14e46-138">Deploying a Provider</span></span>](deploying-a-provider.md)    
- [<span data-ttu-id="14e46-139">Регистрация поставщика</span><span class="sxs-lookup"><span data-stu-id="14e46-139">Registering a Provider</span></span>](registering-a-provider.md)   
- [<span data-ttu-id="14e46-140">Контрольный список установки</span><span class="sxs-lookup"><span data-stu-id="14e46-140">Installation Checklist</span></span>](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a><span data-ttu-id="14e46-141">Шаг D: окончательная проверка перед выпуском</span><span class="sxs-lookup"><span data-stu-id="14e46-141">Step D: Final testing before release</span></span>

<span data-ttu-id="14e46-142">В зависимости от вашей социальной сети и поставщика OSC существуют тесты, которые следует выполнить до выпуска поставщика.</span><span class="sxs-lookup"><span data-stu-id="14e46-142">Depending on your social network and the OSC provider, there are usually provider-specific tests you should carry out before you release your provider.</span></span> <span data-ttu-id="14e46-143">Предлагаемый список тестов приведен [в разделе Подготовка к запуску поставщика OSC](getting-ready-to-release-an-osc-provider.md).</span><span class="sxs-lookup"><span data-stu-id="14e46-143">For a suggested list of tests, see [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="14e46-144">См. также</span><span class="sxs-lookup"><span data-stu-id="14e46-144">See also</span></span>

- [<span data-ttu-id="14e46-145">Начало разработки поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="14e46-145">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

