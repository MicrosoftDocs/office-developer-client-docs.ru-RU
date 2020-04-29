---
title: Реализация объектов MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c0d67d10d54591de926724cbf594a44f17e9ea14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310173"
---
# <a name="implementing-mapi-objects"></a><span data-ttu-id="8aaa3-103">Реализация объектов MAPI</span><span class="sxs-lookup"><span data-stu-id="8aaa3-103">Implementing MAPI Objects</span></span>

  
  
<span data-ttu-id="8aaa3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8aaa3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8aaa3-105">Объекты MAPI можно реализовать с помощью классов C++ или структур данных C в зависимости от языка и набора API, используемого клиентом или поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-105">MAPI objects can be implemented by using C++ classes or C data structures, depending on the language and the API set a client or service provider is using.</span></span> <span data-ttu-id="8aaa3-106">Поставщики услуг можно писать в C или C++ с помощью интерфейса поставщика службы MAPI; клиентские приложения также могут использовать C или C++.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-106">Service providers can be written in C or C++ with the MAPI service provider interface; client applications can also use C or C++.</span></span> <span data-ttu-id="8aaa3-107">Если это возможно, клиенты и поставщики услуг, использующие объектно ориентированный интерфейс программирования, должны использовать C++.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-107">If possible, clients and service providers that use the object-oriented programming interface should use C++.</span></span> 
  
<span data-ttu-id="8aaa3-108">Язык c++ предпочтительнее, так как MAPI является объектно-ориентированной технологией, а C++ в объектно-ориентированной разработке.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-108">C++ is the preferred choice because MAPI is an object-oriented technology, and C++ lends itself more readily to object-oriented development.</span></span> <span data-ttu-id="8aaa3-109">Полученный код проще и упрощает обслуживание.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-109">The resulting code is simpler and more straightforward, making it easier to maintain.</span></span> <span data-ttu-id="8aaa3-110">Документация по MAPI записывается преимущественно разработчикам C++; все описания синтаксиса для методов интерфейса MAPI в этой ссылке представлены в C++.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-110">The MAPI documentation is written primarily for C++ developers; all of the syntax descriptions for the MAPI interface methods in this Reference are in C++.</span></span>
  
<span data-ttu-id="8aaa3-111">Разработчики могут использовать Microsoft Visual Studio и сторонние средства разработки для разработки решений, вызывающих MAPI.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-111">Developers can use Microsoft Visual Studio and third-party development tools to develop solutions that call MAPI.</span></span> <span data-ttu-id="8aaa3-112">Обратите внимание, что разработчики должны использовать C или неуправляемый C++, но не управляемые C++ для написания решений MAPI.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-112">Note that developers should use C or unmanaged C++, but not managed C++ to write MAPI solutions.</span></span>
  
<span data-ttu-id="8aaa3-113">Когда объект MAPI реализован, клиент или поставщик услуг создает код для всех методов интерфейса, кода для всех частных методов, характерных для реализации, и кода для поддержки закрытых элементов данных для поддержания сведений о состоянии.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-113">When a MAPI object is implemented, a client or service provider creates code for all of the interface methods, code for any private methods that are specific to the implementation, and code to support private data members for maintaining state information.</span></span> <span data-ttu-id="8aaa3-114">Код методов интерфейса должен соответствовать спецификациям, опубликованным MAPI, в котором ожидается поведение Document.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-114">The code for the interface methods must follow the specifications published by MAPI that document expected behavior.</span></span> 
  
<span data-ttu-id="8aaa3-115">В файле заголовка MAPIDEFS. h и файлах заголовков OLE существует множество макросов, которые могут использоваться клиентами и поставщиками служб на любом языке, чтобы помочь им в определениях объектов MAPI.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-115">There are many macros in the Mapidefs.h header file and OLE header files that clients and service providers in either language can use to help them with their definitions of MAPI objects.</span></span> <span data-ttu-id="8aaa3-116">Например, существует макрос, определяющий методы каждого интерфейса MAPI.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-116">For example, there is a macro to define the methods of each of the MAPI interfaces.</span></span> <span data-ttu-id="8aaa3-117">Макрос, определяющий методы интерфейса [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) , отображается в MAPIDEFS. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8aaa3-117">The macro to define the methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface appears in Mapidefs.h as follows:</span></span> 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a><span data-ttu-id="8aaa3-118">См. также</span><span class="sxs-lookup"><span data-stu-id="8aaa3-118">See also</span></span>



[<span data-ttu-id="8aaa3-119">Общие сведения об объекте и интерфейсе MAPI</span><span class="sxs-lookup"><span data-stu-id="8aaa3-119">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

