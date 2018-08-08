---
title: Обзор справочника по MAPI для Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: 'Последнее изменение: 01 февраля 2013 г.'
ms.openlocfilehash: c0d7faaa957167977606cd93800a085d62b214f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810077"
---
# <a name="outlook-mapi-reference-overview"></a><span data-ttu-id="cebd6-103">Обзор справочника по MAPI для Outlook</span><span class="sxs-lookup"><span data-stu-id="cebd6-103">Outlook MAPI Reference Overview</span></span>

<span data-ttu-id="cebd6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cebd6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cebd6-105">В этом разделе изложены общие сведения о документации по Справочник по интерфейсу MAPI приложения Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="cebd6-105">This topic provides overview information about the Outlook 2013 MAPI Reference documentation.</span></span>
  
## <a name="about-this-documentation"></a><span data-ttu-id="cebd6-106">Об этой документации</span><span class="sxs-lookup"><span data-stu-id="cebd6-106">About this documentation</span></span>

<span data-ttu-id="cebd6-107">В этой документации применяется к реализации системы обмена сообщениями API (MAPI) в Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="cebd6-107">This documentation applies to the implementation of the Messaging API (MAPI) in Microsoft Outlook 2013.</span></span> 
  
<span data-ttu-id="cebd6-108">До Microsoft Office Outlook 2007 Справочник программиста MAPI являлся частью документации по Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="cebd6-108">Previous to Microsoft Office Outlook 2007, the MAPI Programmer's Reference was part of the Microsoft Exchange documentation.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cebd6-109">Так как Exchange deemphasized использование интерфейса MAPI, начиная с Microsoft Exchange Server 2007, поддержка реализации Exchange ограничен.</span><span class="sxs-lookup"><span data-stu-id="cebd6-109">Because Exchange has deemphasized the use of MAPI since Microsoft Exchange Server 2007, support for the Exchange implementation is limited.</span></span> 
  
<span data-ttu-id="cebd6-110">Реализация Outlook MAPI отличается от реализации Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="cebd6-110">The Outlook implementation of MAPI differs from the Microsoft Exchange implementation.</span></span> <span data-ttu-id="cebd6-111">Реализация Outlook оптимизирован для запуска на клиентских компьютерах с акцентом минимизировать задержки.</span><span class="sxs-lookup"><span data-stu-id="cebd6-111">The Outlook implementation is optimized for running on client computers and emphasizes low latency.</span></span> <span data-ttu-id="cebd6-112">Реализация Exchange предназначена для серверов, где высокого уровня доступности и лучше многопоточность являются важными.</span><span class="sxs-lookup"><span data-stu-id="cebd6-112">The Exchange implementation is intended for servers where high availability and better multithreading are important.</span></span>
  
<span data-ttu-id="cebd6-113">Использование этой документации для приложений, работающих на компьютерах конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="cebd6-113">Use this documentation for applications running on end-user systems.</span></span> <span data-ttu-id="cebd6-114">Для серверных приложений Описание использования реализации Exchange MAPI при необходимости или использовать текущих API Exchange, таких как веб-служб Exchange.</span><span class="sxs-lookup"><span data-stu-id="cebd6-114">For server applications, use the Exchange implementation of MAPI if appropriate, or use current Exchange APIs such as Exchange Web Services.</span></span> <span data-ttu-id="cebd6-115">Дополнительные сведения о веб-служб Exchange содержатся в разделе [Веб-служб Exchange ссылки](http://msdn.microsoft.com/en-us/library/bb204119.aspx).</span><span class="sxs-lookup"><span data-stu-id="cebd6-115">For more information on Exchange Web Services, see the [Exchange Web Services Reference](http://msdn.microsoft.com/en-us/library/bb204119.aspx).</span></span>
  
<span data-ttu-id="cebd6-116">Можно создавать приложения, которые работают с Outlook или Exchange реализациями MAPI.</span><span class="sxs-lookup"><span data-stu-id="cebd6-116">It may be possible to write applications that work with either the Outlook or Exchange implementations of MAPI.</span></span> <span data-ttu-id="cebd6-117">Например mfcmapi (en) работает на любой из платформ.</span><span class="sxs-lookup"><span data-stu-id="cebd6-117">For example, MFCMAPI works well on either platform.</span></span> <span data-ttu-id="cebd6-118">Реализации иметь множество общие функции, но существуют некоторые отличия очевидны и тонкой.</span><span class="sxs-lookup"><span data-stu-id="cebd6-118">The implementations have many common features, but there are differences both obvious and subtle.</span></span> <span data-ttu-id="cebd6-119">Необходимо тщательно проверьте для обеих платформ, если вы намереваетесь приложения для работы во всех средах.</span><span class="sxs-lookup"><span data-stu-id="cebd6-119">You will have to test carefully on both platforms if you intend for your application to work in all environments.</span></span> <span data-ttu-id="cebd6-120">Тестирования потребуется две системы из-за выполнение обоих реализации на одном установки операционной системы не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cebd6-120">This testing will require two systems because running both implementations on the same operating system installation is not supported.</span></span>
  
<span data-ttu-id="cebd6-121">Обратите внимание, что MAPI подходит для низкого уровня доступа к данным в хранилище MAPI и построение транспорта, хранение сообщений или поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="cebd6-121">Be aware that MAPI is appropriate for low-level access to data in a MAPI store or for building a transport, message store, or address book provider.</span></span> <span data-ttu-id="cebd6-122">Поскольку MAPI обходит Outlook бизнес-логики, необходимо учитывать использование объектной модели Outlook при оценке API-интерфейсы для построения решения.</span><span class="sxs-lookup"><span data-stu-id="cebd6-122">Because MAPI bypasses Outlook's business logic, you should also consider the use of the Outlook object model when you evaluate APIs for building your solution.</span></span> <span data-ttu-id="cebd6-123">Объектная модель Outlook инкапсулирует бизнес-логику Outlook, но не подходит для многопоточных кода, поставщики синхронизации или приложений-служб Windows.</span><span class="sxs-lookup"><span data-stu-id="cebd6-123">The Outlook object model does encapsulate Outlook business logic but is not suitable for multithreaded code, sync providers, or Windows Service applications.</span></span>
  
<span data-ttu-id="cebd6-124">Сведения о том, что новые возможности этой версии в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="cebd6-124">For information about what is new in this edition, see the following topics:</span></span>
  
- [<span data-ttu-id="cebd6-125">Новые возможности этого выпуска</span><span class="sxs-lookup"><span data-stu-id="cebd6-125">What's New in This Edition</span></span>](what-s-new-in-this-edition.md)
    
- [<span data-ttu-id="cebd6-126">Элементы API, объявленные устаревшими в этом выпуске</span><span class="sxs-lookup"><span data-stu-id="cebd6-126">API Elements Deprecated in This Edition</span></span>](api-elements-deprecated-in-this-edition.md)
    
<span data-ttu-id="cebd6-127">Если вы не знакомы с разработкой приложений MAPI в Outlook, в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="cebd6-127">If you are new to developing MAPI applications for Outlook, see the following topics:</span></span>
  
- [<span data-ttu-id="cebd6-128">Выбор API или технологий для разработки решений для Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="cebd6-128">Selecting an API or technology for developing solutions for Outlook 2013</span></span>](http://msdn.microsoft.com/en-us/library/jj900714.aspx)
    
- [<span data-ttu-id="cebd6-129">Часто используемые файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="cebd6-129">Commonly Used Header Files</span></span>](commonly-used-header-files.md)
    
- [<span data-ttu-id="cebd6-130">Часто используемые свойства</span><span class="sxs-lookup"><span data-stu-id="cebd6-130">Commonly Used Properties</span></span>](commonly-used-properties.md)
    
- [<span data-ttu-id="cebd6-131">Часто используемые объекты</span><span class="sxs-lookup"><span data-stu-id="cebd6-131">Commonly Used Objects</span></span>](commonly-used-objects.md)
    
<span data-ttu-id="cebd6-132">Остальная часть данной справки разделить на следующие три типа данных:</span><span class="sxs-lookup"><span data-stu-id="cebd6-132">The rest of this reference is categorized into the following three types of information:</span></span>
  
- <span data-ttu-id="cebd6-133">[Примеры MAPI](mapi-samples.md) - содержит много примеров кода, которые демонстрируют использование различных элементов API и как реализовать основные поставщики MAPI и создания элементов Outlook.</span><span class="sxs-lookup"><span data-stu-id="cebd6-133">[MAPI Samples](mapi-samples.md) - Directs you to many code samples that show the use of various API elements and how to implement basic MAPI providers and create Outlook items.</span></span> 
    
- <span data-ttu-id="cebd6-134">[Концепции MAPI](mapi-concepts.md) - объясняет принципы и архитектура MAPI.</span><span class="sxs-lookup"><span data-stu-id="cebd6-134">[MAPI Concepts](mapi-concepts.md) - Explains the concepts and architecture of MAPI.</span></span> 
    
- <span data-ttu-id="cebd6-135">[Справочник по интерфейсу MAPI](mapi-reference.md) - предоставляет подробные сведения о функции, интерфейсы, структуры и свойств в MAPI.</span><span class="sxs-lookup"><span data-stu-id="cebd6-135">[MAPI Reference](mapi-reference.md) - Provides detailed information about the functions, interfaces, structures, and properties in MAPI.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="cebd6-136">См. также</span><span class="sxs-lookup"><span data-stu-id="cebd6-136">See also</span></span>

- [<span data-ttu-id="cebd6-137">Начало работы со справочником по MAPI для Outlook</span><span class="sxs-lookup"><span data-stu-id="cebd6-137">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)
- [<span data-ttu-id="cebd6-138">Примеры MAPI</span><span class="sxs-lookup"><span data-stu-id="cebd6-138">MAPI Samples</span></span>](mapi-samples.md)
- [<span data-ttu-id="cebd6-139">Понятия MAPI</span><span class="sxs-lookup"><span data-stu-id="cebd6-139">MAPI Concepts</span></span>](mapi-concepts.md)

