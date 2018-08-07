---
title: Применение образец шаблона поставщика
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Образцы шаблонов поставщика Outlook Social Connector (OSC) предоставить структуру для реализации поставщика OSC. '
ms.openlocfilehash: 2388da58690e1870434c576bfa68649937156c54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812700"
---
# <a name="applying-a-sample-provider-template"></a><span data-ttu-id="81e9d-103">Применение образец шаблона поставщика</span><span class="sxs-lookup"><span data-stu-id="81e9d-103">Applying a Sample Provider Template</span></span>

<span data-ttu-id="81e9d-104">Образцы шаблонов поставщика Outlook Social Connector (OSC) предоставить структуру для реализации поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="81e9d-104">The sample Outlook Social Connector (OSC) provider templates give you a framework for implementing an OSC provider.</span></span> <span data-ttu-id="81e9d-105">Шаблоны поставщика доступны на C++, C# и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="81e9d-105">The provider templates are available in C++, C#, and Visual Basic.</span></span> <span data-ttu-id="81e9d-106">Эти шаблоны, просто отправной точки для разработки поставщика; шаблоны, не относятся к написанию кода реализации поставщика и создание пакета установки для поставщика.</span><span class="sxs-lookup"><span data-stu-id="81e9d-106">These templates are just a starting point for your provider development; the templates do not address writing the implementation code for the provider and creating a setup package for the provider.</span></span> <span data-ttu-id="81e9d-107">Следующей процедуре показано, как применить шаблон поставщика OSC при начале разработки поставщика.</span><span class="sxs-lookup"><span data-stu-id="81e9d-107">The following procedure shows how to apply an OSC provider template when you begin to develop a provider.</span></span>
  
### <a name="to-apply-an-osc-provider-template"></a><span data-ttu-id="81e9d-108">Чтобы применить шаблон поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="81e9d-108">To apply an OSC provider template</span></span>

1. <span data-ttu-id="81e9d-109">В меню **Пуск** щелкните правой кнопкой мыши **Microsoft Visual Studio 2010** и выберите команду **Запуск от имени администратора** .</span><span class="sxs-lookup"><span data-stu-id="81e9d-109">On the **Start** menu, right-click **Microsoft Visual Studio 2010** and click the **Run as administrator** command.</span></span> <span data-ttu-id="81e9d-110">При появлении запроса нажмите кнопку **Да** для запуска Visual Studio с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="81e9d-110">When prompted, click **Yes** to run Visual Studio as an administrator.</span></span> 
    
2. <span data-ttu-id="81e9d-111">Измените имя проекта и пространства имен в шаблоне на идентификаторов и пространства имен проекта.</span><span class="sxs-lookup"><span data-stu-id="81e9d-111">Change the project name and namespace in the template to your project name and namespace identifiers.</span></span>
    
3. <span data-ttu-id="81e9d-112">Измените класс **AssemblyInfo** для определения информации, соответствующей сборки.</span><span class="sxs-lookup"><span data-stu-id="81e9d-112">Modify the **AssemblyInfo** class to specify the appropriate assembly information.</span></span> 
    
4. <span data-ttu-id="81e9d-113">Реализация членов интерфейса, помеченные как **задачи** и добавьте дополнительные справочные материалы и зависимостей при необходимости.</span><span class="sxs-lookup"><span data-stu-id="81e9d-113">Implement the interface members marked as **To-Do** and add more dependencies and references, as required.</span></span> 
    
5. <span data-ttu-id="81e9d-114">Выполните построение проекта.</span><span class="sxs-lookup"><span data-stu-id="81e9d-114">Build the project.</span></span>
    
6. <span data-ttu-id="81e9d-115">Убедитесь, что программный идентификатор сборки поставщика из списка в разделе реестра `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span><span class="sxs-lookup"><span data-stu-id="81e9d-115">Ensure that the provider assembly ProgID is listed as a key under  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
7. <span data-ttu-id="81e9d-116">Чтобы распространить проект программы установки, создайте проект программы установки в Visual Studio или средство установки собственное.</span><span class="sxs-lookup"><span data-stu-id="81e9d-116">To distribute the setup project, create a setup project in Visual Studio or a setup tool of your choice.</span></span>
    
8. <span data-ttu-id="81e9d-117">Проект программы установки следует завершения регистрации COM для сборки и также создать ProgID ключ, указанный в шаге 5.</span><span class="sxs-lookup"><span data-stu-id="81e9d-117">Your setup project should complete COM registration for your assembly and also create the ProgID key as listed in step 5.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81e9d-118">См. также</span><span class="sxs-lookup"><span data-stu-id="81e9d-118">See also</span></span>

- [<span data-ttu-id="81e9d-119">Загрузка примеров</span><span class="sxs-lookup"><span data-stu-id="81e9d-119">Downloading the Samples</span></span>](downloading-the-samples.md)
- [<span data-ttu-id="81e9d-120">Шаблоны OSC примера</span><span class="sxs-lookup"><span data-stu-id="81e9d-120">OSC Sample Templates</span></span>](osc-sample-templates.md)

