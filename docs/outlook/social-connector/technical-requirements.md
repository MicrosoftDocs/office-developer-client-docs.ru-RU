---
title: Технические требования
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: В этом разделе описываются поддерживаемые языки программирования, возможности отображения и возврата COM-кода, а также подробные сведения о DLL расширяемости поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329157"
---
# <a name="technical-requirements"></a><span data-ttu-id="b89b2-103">Технические требования</span><span class="sxs-lookup"><span data-stu-id="b89b2-103">Technical requirements</span></span>

<span data-ttu-id="b89b2-104">В этом разделе описываются поддерживаемые языки программирования, возможности отображения и возврата COM-кода, а также подробные сведения о DLL расширяемости поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="b89b2-104">This topic describes the supported programming languages, COM visibility and method return type requirements, and details of the Outlook Social Connector (OSC) provider extensibility DLL.</span></span> 
  
## <a name="programming-language-and-com-requirements"></a><span data-ttu-id="b89b2-105">Требования к языку программирования и COM</span><span class="sxs-lookup"><span data-stu-id="b89b2-105">Programming language and COM requirements</span></span>

<span data-ttu-id="b89b2-106">Вы можете создать поставщика OSC, используя управляемые языки, такие как Visual C# или Visual Basic, или неуправляемые языки, такие как Visual C++.</span><span class="sxs-lookup"><span data-stu-id="b89b2-106">You can create an OSC provider by using managed languages such as Visual C# or Visual Basic, or unmanaged languages such as Visual C++.</span></span> <span data-ttu-id="b89b2-107">Вы можете использовать любое средство, с помощью которого можно создать COM-компонент DLL для разработки поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="b89b2-107">You can use any tool that can create a COM-visible DLL component to develop an OSC provider.</span></span> <span data-ttu-id="b89b2-108">Решение использовать управляемый или неуправляемый язык для разработки поставщика должен учитывать размер загружаемого файла и зависимости пакета установки поставщика.</span><span class="sxs-lookup"><span data-stu-id="b89b2-108">The decision to use a managed or unmanaged language to develop a provider should take into account the download size and dependencies of the provider installation package.</span></span>
  
<span data-ttu-id="b89b2-109">Поставщик OSC должен быть видимым для COM, как определено в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="b89b2-109">An OSC provider must be COM-visible as defined by the following:</span></span>
  
- <span data-ttu-id="b89b2-110">После установки поставщик OSC необходимо зарегистрировать с помощью функции самостоятельной регистрации COM или regsvr32.</span><span class="sxs-lookup"><span data-stu-id="b89b2-110">After installation, an OSC provider must be registered by using COM self-registration or regsvr32.</span></span>
    
- <span data-ttu-id="b89b2-111">При регистрации COM для библиотеки DLL поставщика OSC поставщик регистрируется в разделе HKCU или HKLM.</span><span class="sxs-lookup"><span data-stu-id="b89b2-111">COM registration of an OSC provider DLL registers the provider under HKCU or HKLM.</span></span> 
    
- <span data-ttu-id="b89b2-112">Идентификатор ProgID поставщика зарегистрирован в разделе `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span><span class="sxs-lookup"><span data-stu-id="b89b2-112">A provider's ProgID is registered under  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
- <span data-ttu-id="b89b2-113">Поставщик OSC, разработанный на управляемом языке, является видимым для COM.</span><span class="sxs-lookup"><span data-stu-id="b89b2-113">An OSC provider developed in a managed language is COM-visible.</span></span>
    
- <span data-ttu-id="b89b2-114">Поставщик OSC должен добавить в реестр Windows значения, указывающие на то, что библиотека DLL поставщика поддерживает потоковые модели с однопотоковым апартаментом (STA) и многопоточным апартаментом (MTA).</span><span class="sxs-lookup"><span data-stu-id="b89b2-114">An OSC provider should add values to the Windows registry that indicate that the provider DLL supports both single-threaded apartment (STA) and multithreaded apartment (MTA) threading models.</span></span> <span data-ttu-id="b89b2-115">Для получения дополнительных сведений о COM-потоковой модели ознакомьтесь с [описанием и работой моделей потоков OLE](https://support.microsoft.com/kb/150777).</span><span class="sxs-lookup"><span data-stu-id="b89b2-115">For more information about COM threading models, see [Descriptions and Workings of OLE Threading Models](https://support.microsoft.com/kb/150777).</span></span>
    
<span data-ttu-id="b89b2-116">Методы в расширяемости поставщика OSC должны возвращать простые типы, такие как **String** или **bool**.</span><span class="sxs-lookup"><span data-stu-id="b89b2-116">Methods in OSC provider extensibility must return primitive types such as **string** or **bool**.</span></span> <span data-ttu-id="b89b2-117">Определенные **строковые** возвращаемые значения должны соответствовать определению схемы для расширяемости поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="b89b2-117">Certain **string** return values must comply with the schema definition for OSC provider extensibility.</span></span> <span data-ttu-id="b89b2-118">В качестве возвращаемого значения поддерживается только XML.</span><span class="sxs-lookup"><span data-stu-id="b89b2-118">Only XML is supported as a return value.</span></span> 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a><span data-ttu-id="b89b2-119">Подробные сведения о библиотеке DLL расширяемости поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="b89b2-119">Details of the OSC provider extensibility DLL</span></span>

<span data-ttu-id="b89b2-120">Компонент, поддерживающий Расширяемость поставщика OSC, это библиотека DLL расширения поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="b89b2-120">The component that supports OSC provider extensibility is the OSC provider extensibility DLL.</span></span> <span data-ttu-id="b89b2-121">Сторонние разработчики могут создавать библиотеки DLL поставщика OSC с помощью этих интерфейсов расширения.</span><span class="sxs-lookup"><span data-stu-id="b89b2-121">Third-party developers can build OSC provider DLLs by using these extensibility interfaces.</span></span> <span data-ttu-id="b89b2-122">В следующем списке приведены подробные сведения о библиотеке DLL расширяемости поставщика OSC:</span><span class="sxs-lookup"><span data-stu-id="b89b2-122">The following list shows the details of the OSC provider extensibility DLL:</span></span>
  
- <span data-ttu-id="b89b2-123">Имя файла DLL расширяемости: соЦиалпровидер. dll</span><span class="sxs-lookup"><span data-stu-id="b89b2-123">Extensibility DLL file name: socialprovider.dll</span></span>
    
- <span data-ttu-id="b89b2-124">Понятное имя DLL расширения: расширяемость поставщика Microsoft Outlook Social</span><span class="sxs-lookup"><span data-stu-id="b89b2-124">Extensibility DLL friendly name: Microsoft Outlook Social Provider Extensibility</span></span>
    
- <span data-ttu-id="b89b2-125">Основная версия библиотеки DLL расширения: 15,0</span><span class="sxs-lookup"><span data-stu-id="b89b2-125">Extensibility DLL major version: 15.0</span></span>
    
- <span data-ttu-id="b89b2-126">Версия библиотеки типов DLL Екстенсибиилти: 1,1</span><span class="sxs-lookup"><span data-stu-id="b89b2-126">Extensibiilty DLL TypeLib version: 1.1</span></span>
    
## <a name="miscellaneous-technical-information"></a><span data-ttu-id="b89b2-127">Прочие технические сведения</span><span class="sxs-lookup"><span data-stu-id="b89b2-127">Miscellaneous technical information</span></span>

<span data-ttu-id="b89b2-128">Нотация объектов JavaScript (JSON) не поддерживается в модели расширяемости поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="b89b2-128">JavaScript Object Notation (JSON) is not supported in the OSC provider extensibility model.</span></span>
  
<span data-ttu-id="b89b2-129">Средство синтаксического анализа XML не зависит от зависимостей.</span><span class="sxs-lookup"><span data-stu-id="b89b2-129">There are no dependencies on an XML parser.</span></span> <span data-ttu-id="b89b2-130">Поставщик OSC может использовать средство синтаксического анализа XML, включенное в Office, например службы MSXML (Microsoft XML Core Services (MSXML)), использовать возможности синтаксического анализа XML, встроенные в Microsoft .NET Framework, или использовать сторонние средства синтаксического анализа XML.</span><span class="sxs-lookup"><span data-stu-id="b89b2-130">The OSC provider can use an XML parser that is included with Office, such as Microsoft XML Core Services (MSXML), use the XML parsing capabilities built into the Microsoft .NET Framework, or use a third-party XML parser.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b89b2-131">См. также</span><span class="sxs-lookup"><span data-stu-id="b89b2-131">See also</span></span>

- [<span data-ttu-id="b89b2-132">Рекомендации по разработке поставщика</span><span class="sxs-lookup"><span data-stu-id="b89b2-132">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)  
- [<span data-ttu-id="b89b2-133">Быстрые действия для изучения разработки поставщика</span><span class="sxs-lookup"><span data-stu-id="b89b2-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="b89b2-134">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="b89b2-134">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="b89b2-135">Начало разработки поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="b89b2-135">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

