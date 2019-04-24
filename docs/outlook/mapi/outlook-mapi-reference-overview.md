---
title: Обзор справочника по MAPI для Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: 'Дата последнего изменения: 1 февраля 2013 г.'
localization_priority: Priority
ms.openlocfilehash: dc743824cf96800c32d4b4006ae86fbff0bd48a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348498"
---
# <a name="outlook-mapi-reference-overview"></a><span data-ttu-id="6d09e-103">Обзор справочника по MAPI для Outlook</span><span class="sxs-lookup"><span data-stu-id="6d09e-103">Outlook MAPI Reference Overview</span></span>

<span data-ttu-id="6d09e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d09e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d09e-105">В этой статье представлены общие сведения о справочных документах по MAPI для Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="6d09e-105">This topic provides overview information about the Outlook 2013 MAPI Reference documentation.</span></span>
  
## <a name="about-this-documentation"></a><span data-ttu-id="6d09e-106">О документации</span><span class="sxs-lookup"><span data-stu-id="6d09e-106">About this documentation</span></span>

<span data-ttu-id="6d09e-107">Эта документация применяется для реализации MAPI (Messaging API) в Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="6d09e-107">This documentation applies to the implementation of the Messaging API (MAPI) in Microsoft Outlook 2013.</span></span> 
  
<span data-ttu-id="6d09e-108">До Microsoft Office Outlook 2007 справочник программиста MAPI входил в состав документации по Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="6d09e-108">Previous to Microsoft Office Outlook 2007, the MAPI Programmer's Reference was part of the Microsoft Exchange documentation.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6d09e-109">Так как, начиная с Microsoft Exchange Server 2007, в Exchange уменьшено применение MAPI, поддержка реализации для Exchange ограничена.</span><span class="sxs-lookup"><span data-stu-id="6d09e-109">Because Exchange has deemphasized the use of MAPI since Microsoft Exchange Server 2007, support for the Exchange implementation is limited.</span></span> 
  
<span data-ttu-id="6d09e-110">Реализация MAPI для Outlook отличается от реализации для Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="6d09e-110">The Outlook implementation of MAPI differs from the Microsoft Exchange implementation.</span></span> <span data-ttu-id="6d09e-111">Реализация в Outlook оптимизирована для работы на клиентских компьютерах с особым вниманием к уменьшению задержек.</span><span class="sxs-lookup"><span data-stu-id="6d09e-111">The Outlook implementation is optimized for running on client computers and emphasizes low latency.</span></span> <span data-ttu-id="6d09e-112">Реализация в Exchange предназначена для серверов, где важна высокая доступность и улучшенная многопоточность.</span><span class="sxs-lookup"><span data-stu-id="6d09e-112">The Exchange implementation is intended for servers where high availability and better multithreading are important.</span></span>
  
<span data-ttu-id="6d09e-113">Используйте эту документацию для приложений, работающих в системах конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="6d09e-113">Use this documentation for applications running on end-user systems.</span></span> <span data-ttu-id="6d09e-114">Для серверных приложений используйте реализацию MAPI для Exchange, если применимо, или используйте текущие API Exchange, например веб-службы Exchange.</span><span class="sxs-lookup"><span data-stu-id="6d09e-114">For server applications, use the Exchange implementation of MAPI if appropriate, or use current Exchange APIs such as Exchange Web Services.</span></span> <span data-ttu-id="6d09e-115">Дополнительные сведения о веб-службах Exchange см. в статье [Справочник по веб-службам Exchange](https://msdn.microsoft.com/library/bb204119.aspx).</span><span class="sxs-lookup"><span data-stu-id="6d09e-115">For more information on Exchange Web Services, see the [Exchange Web Services Reference](https://msdn.microsoft.com/library/bb204119.aspx).</span></span>
  
<span data-ttu-id="6d09e-116">Можно создавать приложения, работающие с реализациями MAPI либо для Outlook, либо для Exchange.</span><span class="sxs-lookup"><span data-stu-id="6d09e-116">It may be possible to write applications that work with either the Outlook or Exchange implementations of MAPI.</span></span> <span data-ttu-id="6d09e-117">Например, MFCMAPI хорошо работает на обеих платформах.</span><span class="sxs-lookup"><span data-stu-id="6d09e-117">For example, MFCMAPI works well on either platform.</span></span> <span data-ttu-id="6d09e-118">Реализации обладают большим количеством общих функций, но есть очевидные и неявные различия.</span><span class="sxs-lookup"><span data-stu-id="6d09e-118">The implementations have many common features, but there are differences both obvious and subtle.</span></span> <span data-ttu-id="6d09e-119">Необходимо тщательно выполнять тестирование на обеих платформах, если приложение предназначено для работы во всех средах.</span><span class="sxs-lookup"><span data-stu-id="6d09e-119">You will have to test carefully on both platforms if you intend for your application to work in all environments.</span></span> <span data-ttu-id="6d09e-120">Для тестирования потребуются две системы, так как запуск обеих реализаций в одной операционной системе не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6d09e-120">This testing will require two systems because running both implementations on the same operating system installation is not supported.</span></span>
  
<span data-ttu-id="6d09e-121">Следует помнить, что MAPI подходит для доступа низкого уровня к данным в хранилище MAPI или для создания поставщика транспорта, хранилища сообщений или адресной книги.</span><span class="sxs-lookup"><span data-stu-id="6d09e-121">Be aware that MAPI is appropriate for low-level access to data in a MAPI store or for building a transport, message store, or address book provider.</span></span> <span data-ttu-id="6d09e-122">Так как MAPI обходит бизнес-логику Outlook, необходимо также рассмотреть использование объектной модели Outlook при оценке API-интерфейсов для создания решения.</span><span class="sxs-lookup"><span data-stu-id="6d09e-122">Because MAPI bypasses Outlook's business logic, you should also consider the use of the Outlook object model when you evaluate APIs for building your solution.</span></span> <span data-ttu-id="6d09e-123">Объектная модель Outlook включает бизнес-логику Outlook, но не подходит для многопоточного кода, поставщиков синхронизации или приложений-служб Windows.</span><span class="sxs-lookup"><span data-stu-id="6d09e-123">The Outlook object model does encapsulate Outlook business logic but is not suitable for multithreaded code, sync providers, or Windows Service applications.</span></span>
  
<span data-ttu-id="6d09e-124">Дополнительные сведения о новых возможностях этого выпуска см. в указанных ниже статьях.</span><span class="sxs-lookup"><span data-stu-id="6d09e-124">For information about what is new in this edition, see the following topics:</span></span>
  
- [<span data-ttu-id="6d09e-125">Новые возможности этого выпуска</span><span class="sxs-lookup"><span data-stu-id="6d09e-125">What's New in This Edition</span></span>](what-s-new-in-this-edition.md)
    
- [<span data-ttu-id="6d09e-126">Элементы API, объявленные устаревшими в этом выпуске</span><span class="sxs-lookup"><span data-stu-id="6d09e-126">API Elements Deprecated in This Edition</span></span>](api-elements-deprecated-in-this-edition.md)
    
<span data-ttu-id="6d09e-127">Если вы не знакомы с разработкой приложений MAPI для Outlook, см. указанные ниже статьи.</span><span class="sxs-lookup"><span data-stu-id="6d09e-127">If you are new to developing MAPI applications for Outlook, see the following topics:</span></span>
  
- [<span data-ttu-id="6d09e-128">Выбор API или технологии для разработки решений для Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="6d09e-128">Selecting an API or technology for developing solutions for Outlook 2013</span></span>](https://msdn.microsoft.com/library/jj900714.aspx)
    
- [<span data-ttu-id="6d09e-129">Часто используемые файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6d09e-129">Commonly Used Header Files</span></span>](commonly-used-header-files.md)
    
- [<span data-ttu-id="6d09e-130">Часто используемые свойства</span><span class="sxs-lookup"><span data-stu-id="6d09e-130">Commonly Used Properties</span></span>](commonly-used-properties.md)
    
- [<span data-ttu-id="6d09e-131">Часто используемые объекты</span><span class="sxs-lookup"><span data-stu-id="6d09e-131">Commonly Used Objects</span></span>](commonly-used-objects.md)
    
<span data-ttu-id="6d09e-132">Остальная часть этого справочника разделена на три типа сведений, указанных ниже.</span><span class="sxs-lookup"><span data-stu-id="6d09e-132">The rest of this reference is categorized into the following three types of information:</span></span>
  
- <span data-ttu-id="6d09e-133">[Примеры MAPI.](mapi-samples.md) Направляют к разным примерам кода, демонстрирующим использования различных элементов API, способ внедрения основных поставщиков MAPI и создание элементов Outlook.</span><span class="sxs-lookup"><span data-stu-id="6d09e-133">[MAPI Samples](mapi-samples.md) - Directs you to many code samples that show the use of various API elements and how to implement basic MAPI providers and create Outlook items.</span></span> 
    
- <span data-ttu-id="6d09e-134">[Понятия MAPI.](mapi-concepts.md) Объясняются основные понятия и архитектура MAPI.</span><span class="sxs-lookup"><span data-stu-id="6d09e-134">[MAPI Concepts](mapi-concepts.md) - Explains the concepts and architecture of MAPI.</span></span> 
    
- <span data-ttu-id="6d09e-135">[Справочник по интерфейсу MAPI.](mapi-reference.md) Предоставляет подробные сведения о функциях, интерфейсах, структурах и свойствах в MAPI.</span><span class="sxs-lookup"><span data-stu-id="6d09e-135">[MAPI Reference](mapi-reference.md) - Provides detailed information about the functions, interfaces, structures, and properties in MAPI.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6d09e-136">См. также</span><span class="sxs-lookup"><span data-stu-id="6d09e-136">See also</span></span>

- [<span data-ttu-id="6d09e-137">Начало работы со справочником по MAPI для Outlook</span><span class="sxs-lookup"><span data-stu-id="6d09e-137">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)
- [<span data-ttu-id="6d09e-138">Примеры MAPI</span><span class="sxs-lookup"><span data-stu-id="6d09e-138">MAPI Samples</span></span>](mapi-samples.md)
- [<span data-ttu-id="6d09e-139">Понятия MAPI</span><span class="sxs-lookup"><span data-stu-id="6d09e-139">MAPI Concepts</span></span>](mapi-concepts.md)

