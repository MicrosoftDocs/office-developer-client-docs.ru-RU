---
title: Getting ready to release an OSC provider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: В этом разделе предлагаются тесты, которые можно сделать перед выпуском поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414664"
---
# <a name="getting-ready-to-release-an-osc-provider"></a><span data-ttu-id="08838-103">Getting ready to release an OSC provider</span><span class="sxs-lookup"><span data-stu-id="08838-103">Getting ready to release an OSC provider</span></span>

<span data-ttu-id="08838-104">В этом разделе предлагаются тесты, которые можно сделать перед выпуском поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="08838-104">This section suggests tests you can do before you release your Outlook Social Connector (OSC) provider.</span></span> <span data-ttu-id="08838-105">Вы можете начать со ссылками на разделы этого раздела и выполнить некоторые из этих тестов на этапах разработки и тестирования, но эти тесты должны быть выполнены к моменту выпуска.</span><span class="sxs-lookup"><span data-stu-id="08838-105">You can start referring to the topics in this section and carry out some of these tests during your development and testing phases, but you should have completed these tests by the time you release.</span></span> 

<span data-ttu-id="08838-106">Эти тесты проверяют базовую функциональность реализации интерфейсов поставщика OSC в отношении возможностей, указанных для поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="08838-106">These tests verify the basic functionality of your implementation of the OSC provider interfaces with respect to the capabilities you specify for the OSC provider.</span></span> <span data-ttu-id="08838-107">Кроме того, несмотря на то что OSC является функцией, совместно используемой несколькими клиентские приложения Office, в этих тестах используется Outlook в качестве клиента для тестирования основных функций.</span><span class="sxs-lookup"><span data-stu-id="08838-107">Also, even though the OSC is a feature shared by multiple Office client applications, these tests use Outlook as the client to test the fundamental functionality.</span></span> <span data-ttu-id="08838-108">Необходимо определить, необходимы ли другие тесты для функций, характерных для вашего поставщика.</span><span class="sxs-lookup"><span data-stu-id="08838-108">You should determine whether other tests are necessary for features specific to your provider.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="08838-109">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="08838-109">In this section</span></span>

- <span data-ttu-id="08838-110">[Тестирование развертывания](testing-deployment.md): описываются сценарии, на которые следует проверить установку и установку поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="08838-110">[Testing Deployment](testing-deployment.md): Describes scenarios you should test for around installing and uninstalling an OSC provider.</span></span>
    
- <span data-ttu-id="08838-111">[Тестирование возможностей, проверки](testing-capabilities-authentication-and-configuration.md)подлинности и конфигурации : описывает тесты для получения возможностей и сценарии настройки учетной записи и проверки подлинности пользователя в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="08838-111">[Testing Capabilities, Authentication, and Configuration](testing-capabilities-authentication-and-configuration.md): Describes tests for getting capabilities, and scenarios around configuring an account and authenticating a user for a social network.</span></span>
    
- <span data-ttu-id="08838-112">[Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network.</span><span class="sxs-lookup"><span data-stu-id="08838-112">[Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network.</span></span> 
    
- <span data-ttu-id="08838-113">[Тестирование друзей](testing-friends.md): описывает тесты и сценарии, чтобы убедиться, что поставщик OSC правильно возвращает данные друзей и других пользователей, где это применимо, в зависимости от режима синхронизации, поддерживаемого поставщиком.</span><span class="sxs-lookup"><span data-stu-id="08838-113">[Testing Friends](testing-friends.md): Describes tests and scenarios to verify that the OSC provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
- <span data-ttu-id="08838-114">[Действия](testing-activities.md)по тестированию : описываются тесты и сценарии для проверки того, что поставщик OSC правильно возвращает действия друзей и других, если применимо, в зависимости от режима синхронизации, поддерживаемого поставщиком.</span><span class="sxs-lookup"><span data-stu-id="08838-114">[Testing Activities](testing-activities.md): Describes tests and scenarios to verify that the OSC provider appropriately returns activities of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
## <a name="reference"></a><span data-ttu-id="08838-115">Справка</span><span class="sxs-lookup"><span data-stu-id="08838-115">Reference</span></span>

- [<span data-ttu-id="08838-116">Outlook Social Connector Provider Reference</span><span class="sxs-lookup"><span data-stu-id="08838-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="08838-117">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="08838-117">Related sections</span></span>

- [<span data-ttu-id="08838-118">Примеры шаблонов OSC</span><span class="sxs-lookup"><span data-stu-id="08838-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="08838-119">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="08838-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="08838-120">Разработка поставщика с помощью схемы OSC XML</span><span class="sxs-lookup"><span data-stu-id="08838-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="08838-121">Отладка поставщика</span><span class="sxs-lookup"><span data-stu-id="08838-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="08838-122">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="08838-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  

