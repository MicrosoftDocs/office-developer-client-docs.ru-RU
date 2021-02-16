---
title: Общие сведения об объектах и интерфейсах MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fcd85bf518f4e6466bf15a09e417767bc34df78d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345789"
---
# <a name="mapi-object-and-interface-overview"></a><span data-ttu-id="e1d95-103">Общие сведения об объектах и интерфейсах MAPI</span><span class="sxs-lookup"><span data-stu-id="e1d95-103">MAPI Object and Interface Overview</span></span>

  
  
<span data-ttu-id="e1d95-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1d95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1d95-105">Объект MAPI — это объектный класс C++ или структура данных C, наследуемая от одного или более интерфейсов MAPI или коллекций связанных функций.</span><span class="sxs-lookup"><span data-stu-id="e1d95-105">A MAPI object is a C++ object class or C data structure inherited from one or more MAPI interfaces, or collections of related functions.</span></span> <span data-ttu-id="e1d95-106">Эти коллекции связанных функций известны разработчикам C++ как чисто виртуальные функции.</span><span class="sxs-lookup"><span data-stu-id="e1d95-106">These collections of related functions are known to C++ developers as pure virtual functions.</span></span> <span data-ttu-id="e1d95-107">Для чисто виртуальной функции MAPI обеспечивает только прототип функции, а не реализацию.</span><span class="sxs-lookup"><span data-stu-id="e1d95-107">For a pure virtual function, MAPI supplies only the function prototype, not an implementation.</span></span> <span data-ttu-id="e1d95-108">Ожидается, что клиентские приложения, поставщик службы или MAPI будут предоставлять эту реализацию, создав объектный класс, наследующий от интерфейса и соответствующий описаниям функций API обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="e1d95-108">It is expected that a client application, a service provider, or MAPI will provide this implementation by creating an object class that inherits from the interface and conforms to the function descriptions of the Messaging API.</span></span> <span data-ttu-id="e1d95-109">Интерфейс MAPI можно использовать только с помощью унаследованных классов.</span><span class="sxs-lookup"><span data-stu-id="e1d95-109">A MAPI interface can be instantiated only through an inherited class.</span></span>
  
<span data-ttu-id="e1d95-110">Существует множество различных объектов MAPI, каждый из которых наследуется от интерфейса, который в конечном итоге наследуется от [интерфейса IUnknown.](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1d95-110">There are many different MAPI objects, each object inheriting from an interface that is ultimately inherited from the [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="e1d95-111">**IUnknown —** это базовый интерфейс объектной модели компонентов OLE (COM).</span><span class="sxs-lookup"><span data-stu-id="e1d95-111">**IUnknown** is the OLE Component Object Model (COM) base interface.</span></span> <span data-ttu-id="e1d95-112">Он предоставляет объекты MAPI со стандартным механизмом для связи и управления.</span><span class="sxs-lookup"><span data-stu-id="e1d95-112">It provides MAPI objects with a standard mechanism for communication and control.</span></span> <span data-ttu-id="e1d95-113">COM определяет, как реализующие объекты обрабатывают такие проблемы, как управление памятью, управление параметрами и многопрочитание.</span><span class="sxs-lookup"><span data-stu-id="e1d95-113">COM dictates how object implementers handle issues such as memory management, parameter management, and multithreading.</span></span> <span data-ttu-id="e1d95-114">В соответствии с этой моделью, реализующий объект соответствует контракту, указанному интерфейсами, включенными в объект.</span><span class="sxs-lookup"><span data-stu-id="e1d95-114">By conforming to this model, an object implementer adheres to a contract as specified by the interfaces included in the object.</span></span> 
  
<span data-ttu-id="e1d95-115">Многие интерфейсы MAPI наследуются непосредственно от **IUnknown,** а другие наследуются косвенно через один из двух других базовых интерфейсов: [IMAPIProp : IUnknown](imapipropiunknown.md) для управления свойствами и [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) для доступа к папок и адресной книге.</span><span class="sxs-lookup"><span data-stu-id="e1d95-115">Many MAPI interfaces are inherited directly from **IUnknown**, while others are inherited indirectly through one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) for property management and [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) for folder and address book access.</span></span> <span data-ttu-id="e1d95-116">Базовые интерфейсы никогда не реализуются как отдельные автономные объекты; они всегда реализуются как часть других объектов, объектов, реализуя производные интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="e1d95-116">Base interfaces are never implemented as separate, standalone objects; they are always implemented as part of other objects, objects that implement derived interfaces.</span></span> 
  
<span data-ttu-id="e1d95-117">MAPI определяет множество типов объектов, каждый из которых реализован одним или более компонентами MAPI.</span><span class="sxs-lookup"><span data-stu-id="e1d95-117">MAPI defines many types of objects, each implemented by one or more MAPI components.</span></span> <span data-ttu-id="e1d95-118">Объекты, реализованные клиентами, используются MAPI, поставщиками услуг и настраиваемые компоненты форм.</span><span class="sxs-lookup"><span data-stu-id="e1d95-118">Objects implemented by clients are used by MAPI, by service providers, and by custom form components.</span></span> <span data-ttu-id="e1d95-119">Объекты, реализованные поставщиками услуг, обычно используются MAPI и клиентами.</span><span class="sxs-lookup"><span data-stu-id="e1d95-119">Objects implemented by service providers are typically used by MAPI and by clients.</span></span> <span data-ttu-id="e1d95-120">Объекты, реализованные поставщиками библиотеки форм и серверами форм, используются другими компонентами форм и клиентами.</span><span class="sxs-lookup"><span data-stu-id="e1d95-120">Objects implemented by form library providers and form servers are used by other form components and by clients.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e1d95-121">См. также</span><span class="sxs-lookup"><span data-stu-id="e1d95-121">See also</span></span>



[<span data-ttu-id="e1d95-122">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e1d95-122">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="e1d95-123">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e1d95-123">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="e1d95-124">Понятия MAPI</span><span class="sxs-lookup"><span data-stu-id="e1d95-124">MAPI Concepts</span></span>](mapi-concepts.md)

