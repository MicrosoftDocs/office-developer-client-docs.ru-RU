---
title: Применение образца шаблона поставщика
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Шаблоны поставщика приложения Outlook Social Connector (OSC) предоставляют платформу для реализации поставщика OSC. '
ms.openlocfilehash: 10fb21ab640e298bc655b8cad554fae789e2ad47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425913"
---
# <a name="applying-a-sample-provider-template"></a><span data-ttu-id="d93ae-103">Применение образца шаблона поставщика</span><span class="sxs-lookup"><span data-stu-id="d93ae-103">Applying a Sample Provider Template</span></span>

<span data-ttu-id="d93ae-104">Шаблоны поставщика приложения Outlook Social Connector (OSC) предоставляют платформу для реализации поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="d93ae-104">The sample Outlook Social Connector (OSC) provider templates give you a framework for implementing an OSC provider.</span></span> <span data-ttu-id="d93ae-105">Шаблоны поставщика доступны в C++, C# и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d93ae-105">The provider templates are available in C++, C#, and Visual Basic.</span></span> <span data-ttu-id="d93ae-106">Эти шаблоны представляют собой только отправную точку для разработки поставщика; шаблоны не разписывают код реализации поставщика и создает пакет установки для поставщика.</span><span class="sxs-lookup"><span data-stu-id="d93ae-106">These templates are just a starting point for your provider development; the templates do not address writing the implementation code for the provider and creating a setup package for the provider.</span></span> <span data-ttu-id="d93ae-107">В следующей процедуре показано, как применять шаблон поставщика OSC при начале разработки поставщика.</span><span class="sxs-lookup"><span data-stu-id="d93ae-107">The following procedure shows how to apply an OSC provider template when you begin to develop a provider.</span></span>
  
### <a name="to-apply-an-osc-provider-template"></a><span data-ttu-id="d93ae-108">Применение шаблона поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="d93ae-108">To apply an OSC provider template</span></span>

1. <span data-ttu-id="d93ae-109">В меню " **Пуск** " щелкните правой кнопкой мыши элемент **Microsoft Visual Studio 2010** и выберите команду **Запуск от имени администратора** .</span><span class="sxs-lookup"><span data-stu-id="d93ae-109">On the **Start** menu, right-click **Microsoft Visual Studio 2010** and click the **Run as administrator** command.</span></span> <span data-ttu-id="d93ae-110">При появлении соответствующего запроса нажмите кнопку **Да** , чтобы запустить Visual Studio от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="d93ae-110">When prompted, click **Yes** to run Visual Studio as an administrator.</span></span> 
    
2. <span data-ttu-id="d93ae-111">Измените имя проекта и пространство имен в шаблоне на имя проекта и идентификаторы пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d93ae-111">Change the project name and namespace in the template to your project name and namespace identifiers.</span></span>
    
3. <span data-ttu-id="d93ae-112">Измените класс **AssemblyInfo** , указав соответствующие сведения о сборке.</span><span class="sxs-lookup"><span data-stu-id="d93ae-112">Modify the **AssemblyInfo** class to specify the appropriate assembly information.</span></span> 
    
4. <span data-ttu-id="d93ae-113">Реализуйте элементы интерфейса, помеченные как **задачи** , и добавляйте дополнительные зависимости и ссылки, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="d93ae-113">Implement the interface members marked as **To-Do** and add more dependencies and references, as required.</span></span> 
    
5. <span data-ttu-id="d93ae-114">Выполните построение проекта.</span><span class="sxs-lookup"><span data-stu-id="d93ae-114">Build the project.</span></span>
    
6. <span data-ttu-id="d93ae-115">Убедитесь, что идентификатор ProgID сборки поставщика указан как ключ `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span><span class="sxs-lookup"><span data-stu-id="d93ae-115">Ensure that the provider assembly ProgID is listed as a key under  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
7. <span data-ttu-id="d93ae-116">Чтобы распространить проект установки, создайте проект установки в Visual Studio или средство установки.</span><span class="sxs-lookup"><span data-stu-id="d93ae-116">To distribute the setup project, create a setup project in Visual Studio or a setup tool of your choice.</span></span>
    
8. <span data-ttu-id="d93ae-117">Проект установки должен завершить регистрацию COM для сборки, а также создать ключ ProgID, как указано в шаге 5.</span><span class="sxs-lookup"><span data-stu-id="d93ae-117">Your setup project should complete COM registration for your assembly and also create the ProgID key as listed in step 5.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d93ae-118">См. также</span><span class="sxs-lookup"><span data-stu-id="d93ae-118">See also</span></span>

- [<span data-ttu-id="d93ae-119">Загрузка примеров</span><span class="sxs-lookup"><span data-stu-id="d93ae-119">Downloading the Samples</span></span>](downloading-the-samples.md)
- [<span data-ttu-id="d93ae-120">Примеры шаблонов OSC</span><span class="sxs-lookup"><span data-stu-id="d93ae-120">OSC Sample Templates</span></span>](osc-sample-templates.md)

