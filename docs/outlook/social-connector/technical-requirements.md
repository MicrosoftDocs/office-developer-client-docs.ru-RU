---
title: Технические требования
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: В этом разделе описываются поддерживаемые языки программирования, видимость COM и метод возвращает тип требования и сведения о расширений поставщика Outlook Social Connector (OSC) DLL.
ms.openlocfilehash: 94b57e20957f3d8d779c4d3324ecbb8ccd37f60a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812837"
---
# <a name="technical-requirements"></a><span data-ttu-id="9f232-103">Технические требования</span><span class="sxs-lookup"><span data-stu-id="9f232-103">Technical requirements</span></span>

<span data-ttu-id="9f232-104">В этом разделе описываются поддерживаемые языки программирования, видимость COM и метод возвращает тип требования и сведения о расширений поставщика Outlook Social Connector (OSC) DLL.</span><span class="sxs-lookup"><span data-stu-id="9f232-104">This topic describes the supported programming languages, COM visibility and method return type requirements, and details of the Outlook Social Connector (OSC) provider extensibility DLL.</span></span> 
  
## <a name="programming-language-and-com-requirements"></a><span data-ttu-id="9f232-105">Требования к COM и языка программирования</span><span class="sxs-lookup"><span data-stu-id="9f232-105">Programming language and COM requirements</span></span>

<span data-ttu-id="9f232-106">Можно создать поставщика OSC с помощью управляемых языков, например Visual C# или Visual Basic или неуправляемые языков, например Visual C++.</span><span class="sxs-lookup"><span data-stu-id="9f232-106">You can create an OSC provider by using managed languages such as Visual C# or Visual Basic, or unmanaged languages such as Visual C++.</span></span> <span data-ttu-id="9f232-107">Можно использовать любое средство, которое можно создать компонент библиотеки DLL COM-видимым для разработки поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="9f232-107">You can use any tool that can create a COM-visible DLL component to develop an OSC provider.</span></span> <span data-ttu-id="9f232-108">Решение об использовании управляемом и неуправляемом языка для разработки поставщика следует принять во учетной записи размер загружаемого файла и зависимости пакета установки поставщика.</span><span class="sxs-lookup"><span data-stu-id="9f232-108">The decision to use a managed or unmanaged language to develop a provider should take into account the download size and dependencies of the provider installation package.</span></span>
  
<span data-ttu-id="9f232-109">Поставщика OSC должны быть отображены COM, как указано далее.</span><span class="sxs-lookup"><span data-stu-id="9f232-109">An OSC provider must be COM-visible as defined by the following:</span></span>
  
- <span data-ttu-id="9f232-110">После установки поставщика OSC должна быть зарегистрирована с помощью COM самостоятельной регистрации или regsvr32.</span><span class="sxs-lookup"><span data-stu-id="9f232-110">After installation, an OSC provider must be registered by using COM self-registration or regsvr32.</span></span>
    
- <span data-ttu-id="9f232-111">Регистрация поставщика OSC DLL COM регистрируется поставщик в разделе HKCU или HKLM.</span><span class="sxs-lookup"><span data-stu-id="9f232-111">COM registration of an OSC provider DLL registers the provider under HKCU or HKLM.</span></span> 
    
- <span data-ttu-id="9f232-112">Поставщик программный идентификатор зарегистрирован в разделе `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span><span class="sxs-lookup"><span data-stu-id="9f232-112">A provider's ProgID is registered under  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
- <span data-ttu-id="9f232-113">Поставщика OSC, разработанных в управляемом языке виден COM.</span><span class="sxs-lookup"><span data-stu-id="9f232-113">An OSC provider developed in a managed language is COM-visible.</span></span>
    
- <span data-ttu-id="9f232-114">Поставщика OSC следует добавить значения реестра Windows, которые указывают, что поставщик DLL-Библиотека поддерживает одним потоком (STA) и многопоточных подразделения потоковые модели.</span><span class="sxs-lookup"><span data-stu-id="9f232-114">An OSC provider should add values to the Windows registry that indicate that the provider DLL supports both single-threaded apartment (STA) and multithreaded apartment (MTA) threading models.</span></span> <span data-ttu-id="9f232-115">Дополнительные сведения о потоковые модели COM можно [описания и работы OLE Threading моделей](http://support.microsoft.com/kb/150777).</span><span class="sxs-lookup"><span data-stu-id="9f232-115">For more information about COM threading models, see [Descriptions and Workings of OLE Threading Models](http://support.microsoft.com/kb/150777).</span></span>
    
<span data-ttu-id="9f232-116">Методы в возможности расширения поставщика OSC должен возвращать простые типы, такие как **строка** или **bool**.</span><span class="sxs-lookup"><span data-stu-id="9f232-116">Methods in OSC provider extensibility must return primitive types such as **string** or **bool**.</span></span> <span data-ttu-id="9f232-117">Определенные **строки** возвращает следующие значения должны соответствовать схеме определения для расширений поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="9f232-117">Certain **string** return values must comply with the schema definition for OSC provider extensibility.</span></span> <span data-ttu-id="9f232-118">Поддерживается только XML как возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="9f232-118">Only XML is supported as a return value.</span></span> 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a><span data-ttu-id="9f232-119">Сведения о возможности расширения поставщика OSC DLL</span><span class="sxs-lookup"><span data-stu-id="9f232-119">Details of the OSC provider extensibility DLL</span></span>

<span data-ttu-id="9f232-120">Компонент, который поддерживает возможности расширения поставщика OSC является возможности расширения поставщика OSC DLL-Библиотеку.</span><span class="sxs-lookup"><span data-stu-id="9f232-120">The component that supports OSC provider extensibility is the OSC provider extensibility DLL.</span></span> <span data-ttu-id="9f232-121">Сторонние разработчики может создавать библиотеки DLL поставщика OSC с помощью этих интерфейсов расширяемости.</span><span class="sxs-lookup"><span data-stu-id="9f232-121">Third-party developers can build OSC provider DLLs by using these extensibility interfaces.</span></span> <span data-ttu-id="9f232-122">В следующем списке приведены сведения о возможности расширения поставщика OSC DLL:</span><span class="sxs-lookup"><span data-stu-id="9f232-122">The following list shows the details of the OSC provider extensibility DLL:</span></span>
  
- <span data-ttu-id="9f232-123">Имя файла DLL-Библиотека расширяемости: socialprovider.dll</span><span class="sxs-lookup"><span data-stu-id="9f232-123">Extensibility DLL file name: socialprovider.dll</span></span>
    
- <span data-ttu-id="9f232-124">Понятное имя DLL-Библиотека расширяемости: социальные поставщика расширений Microsoft Outlook</span><span class="sxs-lookup"><span data-stu-id="9f232-124">Extensibility DLL friendly name: Microsoft Outlook Social Provider Extensibility</span></span>
    
- <span data-ttu-id="9f232-125">Основная версия DLL-Библиотека расширяемости: 15.0</span><span class="sxs-lookup"><span data-stu-id="9f232-125">Extensibility DLL major version: 15.0</span></span>
    
- <span data-ttu-id="9f232-126">Версия библиотеки типов библиотеки DLL Extensibiilty: 1.1</span><span class="sxs-lookup"><span data-stu-id="9f232-126">Extensibiilty DLL TypeLib version: 1.1</span></span>
    
## <a name="miscellaneous-technical-information"></a><span data-ttu-id="9f232-127">Прочие технические сведения</span><span class="sxs-lookup"><span data-stu-id="9f232-127">Miscellaneous technical information</span></span>

<span data-ttu-id="9f232-128">В модели расширения поставщика OSC JavaScript Object Notation (JSON) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9f232-128">JavaScript Object Notation (JSON) is not supported in the OSC provider extensibility model.</span></span>
  
<span data-ttu-id="9f232-129">Нет отсутствуют зависимости на синтаксического анализа XML.</span><span class="sxs-lookup"><span data-stu-id="9f232-129">There are no dependencies on an XML parser.</span></span> <span data-ttu-id="9f232-130">Поставщика OSC можно использовать анализатор XML, который входит в состав Office, таких как Microsoft XML Core Services (MSXML), используйте XML, синтаксический анализ возможности, встроенные в Microsoft .NET Framework или средство синтаксического анализа XML сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="9f232-130">The OSC provider can use an XML parser that is included with Office, such as Microsoft XML Core Services (MSXML), use the XML parsing capabilities built into the Microsoft .NET Framework, or use a third-party XML parser.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9f232-131">См. также</span><span class="sxs-lookup"><span data-stu-id="9f232-131">See also</span></span>

- [<span data-ttu-id="9f232-132">Рекомендации по разработке поставщика</span><span class="sxs-lookup"><span data-stu-id="9f232-132">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)  
- [<span data-ttu-id="9f232-133">Быстрый шаги, необходимые для разработки поставщика</span><span class="sxs-lookup"><span data-stu-id="9f232-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="9f232-134">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="9f232-134">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="9f232-135">Начало разработки поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="9f232-135">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

