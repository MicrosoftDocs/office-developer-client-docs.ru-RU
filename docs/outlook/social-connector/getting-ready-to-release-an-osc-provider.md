---
title: Готовимся к выпуску поставщика OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: В этом разделе предлагаются тесты, которые можно сделать перед выпуском поставщика Outlook social Connector (OSC).
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414664"
---
# <a name="getting-ready-to-release-an-osc-provider"></a><span data-ttu-id="a1f28-103">Готовимся к выпуску поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="a1f28-103">Getting ready to release an OSC provider</span></span>

<span data-ttu-id="a1f28-104">В этом разделе предлагаются тесты, которые можно сделать перед выпуском поставщика Outlook social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="a1f28-104">This section suggests tests you can do before you release your Outlook Social Connector (OSC) provider.</span></span> <span data-ttu-id="a1f28-105">Вы можете начать ссылаться на разделы в этом разделе и выполнять некоторые из этих тестов на этапах разработки и тестирования, но к моменту выпуска эти тесты должны быть завершены.</span><span class="sxs-lookup"><span data-stu-id="a1f28-105">You can start referring to the topics in this section and carry out some of these tests during your development and testing phases, but you should have completed these tests by the time you release.</span></span> 

<span data-ttu-id="a1f28-106">Эти тесты проверяют основные функциональные возможности реализации интерфейсов поставщика OSC в отношении возможностей, указанных для поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="a1f28-106">These tests verify the basic functionality of your implementation of the OSC provider interfaces with respect to the capabilities you specify for the OSC provider.</span></span> <span data-ttu-id="a1f28-107">Кроме того, несмотря на то, что OSC является функцией, совместно используемой несколькими Office клиентских приложений, эти тесты Outlook в качестве клиента для проверки основных функций.</span><span class="sxs-lookup"><span data-stu-id="a1f28-107">Also, even though the OSC is a feature shared by multiple Office client applications, these tests use Outlook as the client to test the fundamental functionality.</span></span> <span data-ttu-id="a1f28-108">Необходимо определить, необходимы ли другие тесты для функций, определенных вашему поставщику.</span><span class="sxs-lookup"><span data-stu-id="a1f28-108">You should determine whether other tests are necessary for features specific to your provider.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="a1f28-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="a1f28-109">In this section</span></span>

- <span data-ttu-id="a1f28-110">[Тестирование развертывания](testing-deployment.md). Описывает сценарии, которые необходимо протестировать для установки и стирки поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="a1f28-110">[Testing Deployment](testing-deployment.md): Describes scenarios you should test for around installing and uninstalling an OSC provider.</span></span>
    
- <span data-ttu-id="a1f28-111">[Тестирование возможностей, проверки](testing-capabilities-authentication-and-configuration.md)подлинности и конфигурации. Описывает тесты для получения возможностей и сценарии настройки учетной записи и проверки подлинности пользователя для социальной сети.</span><span class="sxs-lookup"><span data-stu-id="a1f28-111">[Testing Capabilities, Authentication, and Configuration](testing-capabilities-authentication-and-configuration.md): Describes tests for getting capabilities, and scenarios around configuring an account and authenticating a user for a social network.</span></span>
    
- <span data-ttu-id="a1f28-112">[Тестирование следующих](testing-following-and-stop-following-persons.md)и Stop-Following: Описывает сценарии проверки способности поставщика OSC добавить человека в качестве друга или удалить друга из социальной сети.</span><span class="sxs-lookup"><span data-stu-id="a1f28-112">[Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network.</span></span> 
    
- <span data-ttu-id="a1f28-113">[Тестирование друзей.](testing-friends.md)Описывает тесты и сценарии, чтобы убедиться, что поставщик OSC надлежащим образом возвращает данные друзей и не-друзей, если это применимо, в зависимости от режима синхронизации, который поддерживает поставщик.</span><span class="sxs-lookup"><span data-stu-id="a1f28-113">[Testing Friends](testing-friends.md): Describes tests and scenarios to verify that the OSC provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
- <span data-ttu-id="a1f28-114">[Тестирование](testing-activities.md)действий . Описывает тесты и сценарии, чтобы убедиться, что поставщик OSC надлежащим образом возвращает действия друзей и не-друзей, где это применимо, в зависимости от режима синхронизации, который поддерживает поставщик.</span><span class="sxs-lookup"><span data-stu-id="a1f28-114">[Testing Activities](testing-activities.md): Describes tests and scenarios to verify that the OSC provider appropriately returns activities of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
## <a name="reference"></a><span data-ttu-id="a1f28-115">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="a1f28-115">Reference</span></span>

- [<span data-ttu-id="a1f28-116">Outlook Справка о поставщике социальных соединители</span><span class="sxs-lookup"><span data-stu-id="a1f28-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="a1f28-117">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="a1f28-117">Related sections</span></span>

- [<span data-ttu-id="a1f28-118">Шаблоны образцов OSC</span><span class="sxs-lookup"><span data-stu-id="a1f28-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="a1f28-119">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="a1f28-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="a1f28-120">Разработка поставщика с помощью схемы XML OSC</span><span class="sxs-lookup"><span data-stu-id="a1f28-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="a1f28-121">Отладка поставщика</span><span class="sxs-lookup"><span data-stu-id="a1f28-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="a1f28-122">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="a1f28-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  

