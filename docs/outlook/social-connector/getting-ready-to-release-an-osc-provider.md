---
title: Подготовка к выпуску поставщика OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: В этом разделе приводятся тесты, которые можно выполнить перед выпуском поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 5caf4144a8daed31d30c9ecbcf9cf21c2300ed8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812715"
---
# <a name="getting-ready-to-release-an-osc-provider"></a><span data-ttu-id="c6bca-103">Подготовка к выпуску поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="c6bca-103">Getting ready to release an OSC provider</span></span>

<span data-ttu-id="c6bca-104">В этом разделе приводятся тесты, которые можно выполнить перед выпуском поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="c6bca-104">This section suggests tests you can do before you release your Outlook Social Connector (OSC) provider.</span></span> <span data-ttu-id="c6bca-105">Можно начать ссылки на разделы в этом разделе и выполнить некоторые из этих тестов во время разработки и тестировании, но также выполнить эти тесты, время, когда будет отпущена.</span><span class="sxs-lookup"><span data-stu-id="c6bca-105">You can start referring to the topics in this section and carry out some of these tests during your development and testing phases, but you should have completed these tests by the time you release.</span></span> 

<span data-ttu-id="c6bca-106">Эти тесты проверяют основные функциональные возможности реализации интерфейсов поставщика OSC по отношению к функциональные возможности, которые можно указать для поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="c6bca-106">These tests verify the basic functionality of your implementation of the OSC provider interfaces with respect to the capabilities you specify for the OSC provider.</span></span> <span data-ttu-id="c6bca-107">Кроме того несмотря на то, что OSC является компонентом, общий для нескольких клиентских приложениях Office, эти тесты использовать Outlook как клиент для тестирования основных функций.</span><span class="sxs-lookup"><span data-stu-id="c6bca-107">Also, even though the OSC is a feature shared by multiple Office client applications, these tests use Outlook as the client to test the fundamental functionality.</span></span> <span data-ttu-id="c6bca-108">Следует определить, ли другие тесты, необходимые для конкретных компонентов для вашего поставщика.</span><span class="sxs-lookup"><span data-stu-id="c6bca-108">You should determine whether other tests are necessary for features specific to your provider.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="c6bca-109">В этой статье</span><span class="sxs-lookup"><span data-stu-id="c6bca-109">In this section</span></span>

- <span data-ttu-id="c6bca-110">[Тестирование развертывания](testing-deployment.md): описаны сценарии, следует проверить, применимую к установке и удалении поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="c6bca-110">[Testing Deployment](testing-deployment.md): Describes scenarios you should test for around installing and uninstalling an OSC provider.</span></span>
    
- <span data-ttu-id="c6bca-111">[Тестирование возможностей, проверки подлинности и конфигурация](testing-capabilities-authentication-and-configuration.md): описание тестов для получения возможности и сценарии Настройка учетной записи и проверка подлинности пользователя для социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="c6bca-111">[Testing Capabilities, Authentication, and Configuration](testing-capabilities-authentication-and-configuration.md): Describes tests for getting capabilities, and scenarios around configuring an account and authenticating a user for a social network.</span></span>
    
- <span data-ttu-id="c6bca-112">[Тестирование следующих и Stop-следующих лиц](testing-following-and-stop-following-persons.md): описание сценариев для тестирования поставщика OSC возможность добавления пользователя как friend или удаление друга из социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="c6bca-112">[Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network.</span></span> 
    
- <span data-ttu-id="c6bca-113">[Тестирование друзья](testing-friends.md): описание тестов и сценариев, чтобы убедиться, что поставщика OSC надлежащим образом возвращает данные из друзья и не-, где это применимо в зависимости от того, поставщик поддерживает режим синхронизации.</span><span class="sxs-lookup"><span data-stu-id="c6bca-113">[Testing Friends](testing-friends.md): Describes tests and scenarios to verify that the OSC provider appropriately returns data of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
- <span data-ttu-id="c6bca-114">[Тестирование действий](testing-activities.md): описание тестов и сценариев, чтобы убедиться, что поставщика OSC надлежащим образом возвращает действий друзья и не-, где это применимо в зависимости от того, поставщик поддерживает режим синхронизации.</span><span class="sxs-lookup"><span data-stu-id="c6bca-114">[Testing Activities](testing-activities.md): Describes tests and scenarios to verify that the OSC provider appropriately returns activities of friends and non-friends, where applicable, depending on the synchronization mode that the provider supports.</span></span>
    
## <a name="reference"></a><span data-ttu-id="c6bca-115">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="c6bca-115">Reference</span></span>

- [<span data-ttu-id="c6bca-116">Справочник поставщика по Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="c6bca-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="c6bca-117">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="c6bca-117">Related sections</span></span>

- [<span data-ttu-id="c6bca-118">Шаблоны OSC примера</span><span class="sxs-lookup"><span data-stu-id="c6bca-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="c6bca-119">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="c6bca-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="c6bca-120">Разработка поставщика с использованием схемы XML для OSC</span><span class="sxs-lookup"><span data-stu-id="c6bca-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="c6bca-121">Отладка поставщика</span><span class="sxs-lookup"><span data-stu-id="c6bca-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="c6bca-122">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="c6bca-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  

