---
title: Справочник по основной сборке взаимодействия Outlook
TOCTitle: '@NoTitle'
ms:assetid: 54bdde85-8dc9-4498-a1ac-f72eaf8f0cd3
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb652780(v=office.15)
ms:contentKeyID: 55119771
ms.date: 09/15/2015
mtps_version: v=office.15
f1_keywords:
- Outlook 2010, programming
- Outlook 2010, object model
- Outlook 2010, PIA
- Outlook code samples
- Outlook 2010, primary interop assembly
- primary interop assembly [Outlook 2010]
- PIA [Outlook 2010]
- reference [Outlook 2010], primary interop assembly
localization_priority: Normal
ms.openlocfilehash: 53c50c447c6f132c562a1a22934df646347a51bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335751"
---
# <a name="outlook-primary-interop-assembly-reference"></a><span data-ttu-id="db00a-102">Справочник по основной сборке взаимодействия Outlook</span><span class="sxs-lookup"><span data-stu-id="db00a-102">Outlook Primary Interop Assembly reference</span></span>

<span data-ttu-id="db00a-103">В справочном руководстве по основной сборке взаимодействия (PIA) Outlook 2013 содержатся справочные сведения для разработки управляемых приложений, предназначенных для Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="db00a-103">The Outlook 2013 Primary Interop Assembly (PIA) reference provides help for developing managed applications for Outlook 2013.</span></span> <span data-ttu-id="db00a-104">Оно расширяет [справочное руководство разработчика Outlook 2013](https://docs.microsoft.com/office/vba/api/overview/outlook) от среды COM до управляемой среды и уделяет особое внимание использованию основной сборки взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="db00a-104">It extends the [Outlook 2013 Developer Reference](https://docs.microsoft.com/office/vba/api/overview/outlook) from the COM environment to the managed environment and focuses on how to use the PIA.</span></span> <span data-ttu-id="db00a-105">В это руководство также включены все дополнения и изменения объектной модели в Outlook 2013, а также множество примеров кода на C\# и Visual Basic, иллюстрирующих выполнение наиболее распространенных задач в Outlook.</span><span class="sxs-lookup"><span data-stu-id="db00a-105">It includes all the additions and changes to the object model in Outlook 2013, and provides many code samples in C\# and Visual Basic to show how to perform common tasks in Outlook.</span></span>

<span data-ttu-id="db00a-106">Если у вас нет опыта разработки решений для Outlook, см. статью [Выбор API или технологии разработки решений для Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md), чтобы выбрать API-интерфейсы и технологии, наиболее соответствующие вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="db00a-106">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span>

## <a name="purpose-of-the-outlook-pia-reference"></a><span data-ttu-id="db00a-107">Назначение справочника Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="db00a-107">Purpose of the Outlook PIA reference</span></span>

<span data-ttu-id="db00a-108">Если вы только начинаете создание надстроек для Outlook, вам следует сначала ознакомиться с концептуальным содержимым справочного руководства разработчика Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="db00a-108">If you are just beginning to write add-ins for Outlook, you should first refer to the conceptual content in the Outlook 2013 Developer Reference.</span></span> <span data-ttu-id="db00a-109">Хотя среда программирования, доступ к некоторым методам и подключение к событиям отличаются в среде COM и управляемой среде разработки, функции в объектной модели Outlook работают аналогично в среде COM и управляемой среде разработки.</span><span class="sxs-lookup"><span data-stu-id="db00a-109">Even though the programming environment and accessing certain methods and connecting to events are different in COM and in managed development, features in the Outlook object model behave the same way in both COM and managed development.</span></span> <span data-ttu-id="db00a-110">С общими сведениями об использовании разных функций объектной модели можно ознакомиться в концептуальном содержимом справочного руководства разработчика Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="db00a-110">You can refer to the conceptual content in the Outlook 2013 Developer Reference to understand how to use the different features of the object model.</span></span>

<span data-ttu-id="db00a-111">Если вы понимаете основы объектной модели Outlook и учитесь разрабатывать управляемые надстройки Outlook, см. статью [Подготовка к использованию Outlook PIA](setting-up-to-use-the-outlook-pia.md).</span><span class="sxs-lookup"><span data-stu-id="db00a-111">If you have a basic understanding of the Outlook object model and are learning to develop managed Outlook add-ins, see [Setting up to use the Outlook PIA](setting-up-to-use-the-outlook-pia.md).</span></span> 

<span data-ttu-id="db00a-112">Сведения о разработке управляемых решений Office с помощью инструментов разработчика Office для Visual Studio 2013 см. в статье [Разработка решений Office в Visual Studio](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017).</span><span class="sxs-lookup"><span data-stu-id="db00a-112">For information about developing managed Office solutions by using Office Developer Tools for Visual Studio 2013, see [Office Development in Visual Studio](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017).</span></span> 

<span data-ttu-id="db00a-113">Сведения о программировании некоторых основных задач Outlook на Visual Basic и C\# см. в статье [Решения Outlook](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017).</span><span class="sxs-lookup"><span data-stu-id="db00a-113">For information about how to program some basic Outlook tasks in both Visual Basic and C\#, see [Outlook solutions](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017).</span></span> 

<span data-ttu-id="db00a-114">Более сложные примеры кода см. в разделе [Инструкции (справочник по основной сборке взаимодействия для Outlook 2013)](how-do-i-outlook-2013-pia-reference.md) этого справочника.</span><span class="sxs-lookup"><span data-stu-id="db00a-114">For more advanced code examples, see [How do I... (Outlook 2013 PIA Reference)](how-do-i-outlook-2013-pia-reference.md) in this reference.</span></span>

<span data-ttu-id="db00a-115">Если объектная модель Outlook уже знакома, есть определенный опыт в написании управляемых приложений, но Outlook PIA используется впервые, следует начать с разделов [Установка и создание ссылок на Outlook PIA](installing-and-referencing-the-outlook-pia.md) и [Архитектура Outlook PIA](architecture-of-the-outlook-pia.md).</span><span class="sxs-lookup"><span data-stu-id="db00a-115">If you are already familiar with the Outlook object model, you have some experience writing managed applications, and you are using the Outlook PIA for the first time, start with [Installing and referencing the Outlook PIA](installing-and-referencing-the-outlook-pia.md) and [Architecture of the Outlook PIA](architecture-of-the-outlook-pia.md).</span></span>

## <a name="accessing-the-outlook-pia-reference-in-design-time"></a><span data-ttu-id="db00a-116">Доступ к справочнику Outlook PIA во время разработки</span><span class="sxs-lookup"><span data-stu-id="db00a-116">Accessing the Outlook PIA reference in design time</span></span>

<span data-ttu-id="db00a-117">При использовании инструментов разработчика Office для Visual Studio 2013 и наличии подключения к Интернету можно обратиться к контекстной справке, нажав клавишу F1 в интегрированной среде разработки Visual Studio (IDE).</span><span class="sxs-lookup"><span data-stu-id="db00a-117">If you use Office Developer Tools for Visual Studio 2013 and you are connected to the Internet, you can access context-sensitive Help when you press F1 in the Visual Studio integrated development environment (IDE).</span></span> <span data-ttu-id="db00a-118">Содержимое этой справки является справочником по PIA для Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="db00a-118">This Help content is the Outlook 2013 PIA reference.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="db00a-119">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="db00a-119">In this section</span></span>

- [<span data-ttu-id="db00a-120">Что нового в справочнике Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="db00a-120">What's new in the Outlook PIA reference</span></span>](what-s-new-in-the-outlook-pia-reference.md)
- [<span data-ttu-id="db00a-121">Подготовка к использованию Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="db00a-121">Setting up to use the Outlook PIA</span></span>](setting-up-to-use-the-outlook-pia.md)
- [<span data-ttu-id="db00a-122">Архитектура Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="db00a-122">Architecture of the Outlook PIA</span></span>](architecture-of-the-outlook-pia.md)
- [<span data-ttu-id="db00a-123">Разработка управляемых надстроек для Outlook с помощью Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="db00a-123">Developing managed Outlook add-ins using the Outlook PIA</span></span>](developing-managed-outlook-add-ins-using-the-outlook-pia.md)
- [<span data-ttu-id="db00a-124">Инструкции (справочник по основной сборке взаимодействия для Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="db00a-124">How do I... (Outlook 2013 PIA Reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)
- [<span data-ttu-id="db00a-125">Библиотека классов</span><span class="sxs-lookup"><span data-stu-id="db00a-125">Class library</span></span>](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook?view=outlook-pia)

## <a name="see-also"></a><span data-ttu-id="db00a-126">См. также</span><span class="sxs-lookup"><span data-stu-id="db00a-126">See also</span></span>

- [<span data-ttu-id="db00a-127">Центр разработчика Outlook</span><span class="sxs-lookup"><span data-stu-id="db00a-127">Outlook Developer Center</span></span>](../outlook-home.md)
- [<span data-ttu-id="db00a-128">Взаимодействие COM и .NET</span><span class="sxs-lookup"><span data-stu-id="db00a-128">COM and .NET Interoperability</span></span>](https://www.apress.com/us/book/9781590590119)
- [<span data-ttu-id="db00a-129">Разработка решений Office в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="db00a-129">Office Development in Visual Studio</span></span>](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017)
- [<span data-ttu-id="db00a-130">Специальные возможности в продуктах Майкрософт</span><span class="sxs-lookup"><span data-stu-id="db00a-130">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/en-us/accessibility/)

