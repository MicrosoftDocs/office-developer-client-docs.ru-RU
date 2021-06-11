---
title: Технические требования
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: В этом разделе описываются поддерживаемые языки программирования, требования к типам возврата com и возвращаемого метода, а также сведения о Outlook поставщике Outlook поставщике extensibility DLL.
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329157"
---
# <a name="technical-requirements"></a><span data-ttu-id="3a4c7-103">Технические требования</span><span class="sxs-lookup"><span data-stu-id="3a4c7-103">Technical requirements</span></span>

<span data-ttu-id="3a4c7-104">В этом разделе описываются поддерживаемые языки программирования, требования к типам возврата com и возвращаемого метода, а также сведения о Outlook поставщике Outlook поставщике extensibility DLL.</span><span class="sxs-lookup"><span data-stu-id="3a4c7-104">This topic describes the supported programming languages, COM visibility and method return type requirements, and details of the Outlook Social Connector (OSC) provider extensibility DLL.</span></span> 
  
## <a name="programming-language-and-com-requirements"></a><span data-ttu-id="3a4c7-105">Язык программирования и требования com</span><span class="sxs-lookup"><span data-stu-id="3a4c7-105">Programming language and COM requirements</span></span>

<span data-ttu-id="3a4c7-106">Вы можете создать поставщика OSC с помощью управляемых языков, таких как Visual C# или Visual Basic, или неугодных языков, таких как Visual C++.</span><span class="sxs-lookup"><span data-stu-id="3a4c7-106">You can create an OSC provider by using managed languages such as Visual C# or Visual Basic, or unmanaged languages such as Visual C++.</span></span> <span data-ttu-id="3a4c7-107">Для разработки поставщика OSC можно использовать любой инструмент, который может создать компонент DLL, видимый в COM.</span><span class="sxs-lookup"><span data-stu-id="3a4c7-107">You can use any tool that can create a COM-visible DLL component to develop an OSC provider.</span></span> <span data-ttu-id="3a4c7-108">При решении использовать управляемый или неустановимый язык для разработки поставщика следует учитывать размер загрузки и зависимости пакета установки поставщика.</span><span class="sxs-lookup"><span data-stu-id="3a4c7-108">The decision to use a managed or unmanaged language to develop a provider should take into account the download size and dependencies of the provider installation package.</span></span>
  
<span data-ttu-id="3a4c7-109">Поставщик OSC должен быть com-видимым в соответствии со следующими следующими словами:</span><span class="sxs-lookup"><span data-stu-id="3a4c7-109">An OSC provider must be COM-visible as defined by the following:</span></span>
  
- <span data-ttu-id="3a4c7-110">После установки поставщик OSC должен быть зарегистрирован с помощью самостоятельной регистрации COM или regsvr32.</span><span class="sxs-lookup"><span data-stu-id="3a4c7-110">After installation, an OSC provider must be registered by using COM self-registration or regsvr32.</span></span>
    
- <span data-ttu-id="3a4c7-111">Регистрация поставщика поставщиков OSC DLL регистрирует поставщика в HKCU или HKLM.</span><span class="sxs-lookup"><span data-stu-id="3a4c7-111">COM registration of an OSC provider DLL registers the provider under HKCU or HKLM.</span></span> 
    
- <span data-ttu-id="3a4c7-112">ProgID поставщика регистрируется под  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` .</span><span class="sxs-lookup"><span data-stu-id="3a4c7-112">A provider's ProgID is registered under  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
- <span data-ttu-id="3a4c7-113">Поставщик OSC, разработанный на управляемом языке, является com-видимым.</span><span class="sxs-lookup"><span data-stu-id="3a4c7-113">An OSC provider developed in a managed language is COM-visible.</span></span>
    
- <span data-ttu-id="3a4c7-114">Поставщик OSC должен добавить значения в реестр Windows, которые указывают на то, что поставщик DLL поддерживает как однопотовые модели потоков квартиры (STA) так и многопотоковые модели потоков квартиры (MTA).</span><span class="sxs-lookup"><span data-stu-id="3a4c7-114">An OSC provider should add values to the Windows registry that indicate that the provider DLL supports both single-threaded apartment (STA) and multithreaded apartment (MTA) threading models.</span></span> <span data-ttu-id="3a4c7-115">Дополнительные сведения о моделях потоков com см. в описании и [работе моделей потоков OLE.](https://support.microsoft.com/kb/150777)</span><span class="sxs-lookup"><span data-stu-id="3a4c7-115">For more information about COM threading models, see [Descriptions and Workings of OLE Threading Models](https://support.microsoft.com/kb/150777).</span></span>
    
<span data-ttu-id="3a4c7-116">Методы в extensibility поставщика OSC должны возвращать примитивные типы, такие как **строка** **или бол.**</span><span class="sxs-lookup"><span data-stu-id="3a4c7-116">Methods in OSC provider extensibility must return primitive types such as **string** or **bool**.</span></span> <span data-ttu-id="3a4c7-117">Некоторые **значения возврата** строки должны соответствовать определению схемы для extensibility поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="3a4c7-117">Certain **string** return values must comply with the schema definition for OSC provider extensibility.</span></span> <span data-ttu-id="3a4c7-118">Только XML поддерживается как возвращаемая величина.</span><span class="sxs-lookup"><span data-stu-id="3a4c7-118">Only XML is supported as a return value.</span></span> 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a><span data-ttu-id="3a4c7-119">Сведения о поставщике extensibility DLL поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="3a4c7-119">Details of the OSC provider extensibility DLL</span></span>

<span data-ttu-id="3a4c7-120">Компонент, который поддерживает удлиняемость поставщика OSC, — это DLL поставщика extensibility OSC.</span><span class="sxs-lookup"><span data-stu-id="3a4c7-120">The component that supports OSC provider extensibility is the OSC provider extensibility DLL.</span></span> <span data-ttu-id="3a4c7-121">Сторонние разработчики могут создавать DLL-интерфейсы поставщика OSC с помощью этих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="3a4c7-121">Third-party developers can build OSC provider DLLs by using these extensibility interfaces.</span></span> <span data-ttu-id="3a4c7-122">В следующем списке показаны сведения о DLL поставщика extensibility osC:</span><span class="sxs-lookup"><span data-stu-id="3a4c7-122">The following list shows the details of the OSC provider extensibility DLL:</span></span>
  
- <span data-ttu-id="3a4c7-123">Имя файла DLL: socialprovider.dll</span><span class="sxs-lookup"><span data-stu-id="3a4c7-123">Extensibility DLL file name: socialprovider.dll</span></span>
    
- <span data-ttu-id="3a4c7-124">Удобное имя DLL: Microsoft Outlook для социальных поставщиков</span><span class="sxs-lookup"><span data-stu-id="3a4c7-124">Extensibility DLL friendly name: Microsoft Outlook Social Provider Extensibility</span></span>
    
- <span data-ttu-id="3a4c7-125">Основная версия DLL: 15.0</span><span class="sxs-lookup"><span data-stu-id="3a4c7-125">Extensibility DLL major version: 15.0</span></span>
    
- <span data-ttu-id="3a4c7-126">Extensibiilty DLL TypeLib версии: 1.1</span><span class="sxs-lookup"><span data-stu-id="3a4c7-126">Extensibiilty DLL TypeLib version: 1.1</span></span>
    
## <a name="miscellaneous-technical-information"></a><span data-ttu-id="3a4c7-127">Различные технические сведения</span><span class="sxs-lookup"><span data-stu-id="3a4c7-127">Miscellaneous technical information</span></span>

<span data-ttu-id="3a4c7-128">Нотация объектов JavaScript (JSON) не поддерживается в модели extensibility поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="3a4c7-128">JavaScript Object Notation (JSON) is not supported in the OSC provider extensibility model.</span></span>
  
<span data-ttu-id="3a4c7-129">Нет зависимостей от XML-parser.</span><span class="sxs-lookup"><span data-stu-id="3a4c7-129">There are no dependencies on an XML parser.</span></span> <span data-ttu-id="3a4c7-130">Поставщик OSC может использовать XML-parser, включенный в Office, например MSXML (MSXML), использовать возможности XML-разреза, встроенные в microsoft платформа .NET Framework, или использовать сторонний синтаксик XML.</span><span class="sxs-lookup"><span data-stu-id="3a4c7-130">The OSC provider can use an XML parser that is included with Office, such as Microsoft XML Core Services (MSXML), use the XML parsing capabilities built into the Microsoft .NET Framework, or use a third-party XML parser.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3a4c7-131">См. также</span><span class="sxs-lookup"><span data-stu-id="3a4c7-131">See also</span></span>

- [<span data-ttu-id="3a4c7-132">Лучшие практики для разработки поставщика</span><span class="sxs-lookup"><span data-stu-id="3a4c7-132">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)  
- [<span data-ttu-id="3a4c7-133">Быстрые шаги для обучения разработке поставщика</span><span class="sxs-lookup"><span data-stu-id="3a4c7-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="3a4c7-134">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="3a4c7-134">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="3a4c7-135">Начало работы с разработкой Outlook поставщика социальных соединители</span><span class="sxs-lookup"><span data-stu-id="3a4c7-135">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

