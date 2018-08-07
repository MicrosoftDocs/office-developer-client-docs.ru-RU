---
title: Обзор интерфейса и объект MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8882457ff99f4150f2c9b086b92af32de29d60a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809772"
---
# <a name="mapi-object-and-interface-overview"></a><span data-ttu-id="46284-103">Обзор интерфейса и объект MAPI</span><span class="sxs-lookup"><span data-stu-id="46284-103">MAPI Object and Interface Overview</span></span>

  
  
<span data-ttu-id="46284-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="46284-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="46284-105">Объект MAPI — класс объекта C++ или C структура данных, наследуется от одного или нескольких интерфейсов MAPI или коллекции связанных функций.</span><span class="sxs-lookup"><span data-stu-id="46284-105">A MAPI object is a C++ object class or C data structure inherited from one or more MAPI interfaces, or collections of related functions.</span></span> <span data-ttu-id="46284-106">Эти коллекции связанных функций называются чисто виртуальные функции для разработчиков на C++.</span><span class="sxs-lookup"><span data-stu-id="46284-106">These collections of related functions are known to C++ developers as pure virtual functions.</span></span> <span data-ttu-id="46284-107">Для чистой виртуальной функции MAPI предоставляет только прототипа функции, но не реализации.</span><span class="sxs-lookup"><span data-stu-id="46284-107">For a pure virtual function, MAPI supplies only the function prototype, not an implementation.</span></span> <span data-ttu-id="46284-108">Предполагается, что клиентское приложение, поставщика услуг или MAPI будет предоставлять этой реализации, создав класс объекта, который наследует от интерфейса и соответствует описания функции API системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="46284-108">It is expected that a client application, a service provider, or MAPI will provide this implementation by creating an object class that inherits from the interface and conforms to the function descriptions of the Messaging API.</span></span> <span data-ttu-id="46284-109">Интерфейс MAPI могут быть созданы только с помощью унаследованного класса.</span><span class="sxs-lookup"><span data-stu-id="46284-109">A MAPI interface can be instantiated only through an inherited class.</span></span>
  
<span data-ttu-id="46284-110">Существует множество различных объектов MAPI, каждый объект, наследуемый от интерфейс, который в конечном счете наследуется от интерфейс [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="46284-110">There are many different MAPI objects, each object inheriting from an interface that is ultimately inherited from the [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="46284-111">**Интерфейс IUnknown** — это основной интерфейс OLE модели компонентных объектов (COM).</span><span class="sxs-lookup"><span data-stu-id="46284-111">**IUnknown** is the OLE Component Object Model (COM) base interface.</span></span> <span data-ttu-id="46284-112">Содержит объектов MAPI с помощью стандартного механизма для обмена данными и элемента управления.</span><span class="sxs-lookup"><span data-stu-id="46284-112">It provides MAPI objects with a standard mechanism for communication and control.</span></span> <span data-ttu-id="46284-113">Определяет COM как объект специалистов по внедрению обрабатывать проблемы, такие как управление памятью, параметр управления и многопоточность.</span><span class="sxs-lookup"><span data-stu-id="46284-113">COM dictates how object implementers handle issues such as memory management, parameter management, and multithreading.</span></span> <span data-ttu-id="46284-114">Соответствующее эту модель, разработчик объект соответствующий контракт, указанный с интерфейсов, включенные в объекте.</span><span class="sxs-lookup"><span data-stu-id="46284-114">By conforming to this model, an object implementer adheres to a contract as specified by the interfaces included in the object.</span></span> 
  
<span data-ttu-id="46284-115">Многие интерфейсы MAPI наследуются непосредственно из **IUnknown**, в то время как другие пользователи косвенно наследуется через один из двух базовых интерфейсов: [IMAPIProp: IUnknown](imapipropiunknown.md) для управления свойствами и [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) для папки и доступа к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="46284-115">Many MAPI interfaces are inherited directly from **IUnknown**, while others are inherited indirectly through one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) for property management and [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) for folder and address book access.</span></span> <span data-ttu-id="46284-116">Базовые интерфейсы никогда не реализованы в виде отдельной, отдельных объектов; всегда реализованы в составе другие объекты, объекты, которые реализуют производные интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="46284-116">Base interfaces are never implemented as separate, standalone objects; they are always implemented as part of other objects, objects that implement derived interfaces.</span></span> 
  
<span data-ttu-id="46284-117">MAPI определяет множество типов объектов, реализованы с одного или нескольких компонентов интерфейса MAPI.</span><span class="sxs-lookup"><span data-stu-id="46284-117">MAPI defines many types of objects, each implemented by one or more MAPI components.</span></span> <span data-ttu-id="46284-118">Объекты, реализуемый клиентами используются MAPI, поставщиков услуг и настраиваемые компоненты формы.</span><span class="sxs-lookup"><span data-stu-id="46284-118">Objects implemented by clients are used by MAPI, by service providers, and by custom form components.</span></span> <span data-ttu-id="46284-119">Объектов, реализованных поставщиков услуг обычно используются для MAPI и клиентами.</span><span class="sxs-lookup"><span data-stu-id="46284-119">Objects implemented by service providers are typically used by MAPI and by clients.</span></span> <span data-ttu-id="46284-120">Объекты реализации поставщиками библиотеки форм и форм серверы используются другими компонентами формы и клиентами.</span><span class="sxs-lookup"><span data-stu-id="46284-120">Objects implemented by form library providers and form servers are used by other form components and by clients.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46284-121">См. также</span><span class="sxs-lookup"><span data-stu-id="46284-121">See also</span></span>



[<span data-ttu-id="46284-122">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="46284-122">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="46284-123">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="46284-123">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="46284-124">Понятия MAPI</span><span class="sxs-lookup"><span data-stu-id="46284-124">MAPI Concepts</span></span>](mapi-concepts.md)

