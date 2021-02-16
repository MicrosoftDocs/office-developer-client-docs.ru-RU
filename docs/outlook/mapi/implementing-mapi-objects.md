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
# <a name="implementing-mapi-objects"></a><span data-ttu-id="ab1dd-103">Реализация объектов MAPI</span><span class="sxs-lookup"><span data-stu-id="ab1dd-103">Implementing MAPI Objects</span></span>

  
  
<span data-ttu-id="ab1dd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab1dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab1dd-105">Объекты MAPI можно реализовать с помощью классов C++ или структур данных C в зависимости от языка и набора API, которые использует клиент или поставщик услуг.</span><span class="sxs-lookup"><span data-stu-id="ab1dd-105">MAPI objects can be implemented by using C++ classes or C data structures, depending on the language and the API set a client or service provider is using.</span></span> <span data-ttu-id="ab1dd-106">Поставщики услуг могут быть написаны на C или C++ с помощью интерфейса поставщика служб MAPI; клиентские приложения также могут использовать C или C++.</span><span class="sxs-lookup"><span data-stu-id="ab1dd-106">Service providers can be written in C or C++ with the MAPI service provider interface; client applications can also use C or C++.</span></span> <span data-ttu-id="ab1dd-107">По возможности клиенты и поставщики услуг, которые используют объектно-ориентированный программный интерфейс, должны использовать C++.</span><span class="sxs-lookup"><span data-stu-id="ab1dd-107">If possible, clients and service providers that use the object-oriented programming interface should use C++.</span></span> 
  
<span data-ttu-id="ab1dd-108">C++ является предпочтительным вариантом, так как MAPI является объектно-ориентированной технологией, и C++ предоставляет себя более легко для объектно-ориентированной разработки.</span><span class="sxs-lookup"><span data-stu-id="ab1dd-108">C++ is the preferred choice because MAPI is an object-oriented technology, and C++ lends itself more readily to object-oriented development.</span></span> <span data-ttu-id="ab1dd-109">В результате код становится проще и проще, что упрощает обслуживание.</span><span class="sxs-lookup"><span data-stu-id="ab1dd-109">The resulting code is simpler and more straightforward, making it easier to maintain.</span></span> <span data-ttu-id="ab1dd-110">Документация по MAPI предназначена в основном для разработчиков C++; все описания синтаксиса для методов интерфейса MAPI в этом справочнике находятся на C++.</span><span class="sxs-lookup"><span data-stu-id="ab1dd-110">The MAPI documentation is written primarily for C++ developers; all of the syntax descriptions for the MAPI interface methods in this Reference are in C++.</span></span>
  
<span data-ttu-id="ab1dd-111">Разработчики могут использовать microsoft Visual Studio и сторонние средства разработки для разработки решений, которые называют MAPI.</span><span class="sxs-lookup"><span data-stu-id="ab1dd-111">Developers can use Microsoft Visual Studio and third-party development tools to develop solutions that call MAPI.</span></span> <span data-ttu-id="ab1dd-112">Обратите внимание, что для написания решений MAPI разработчикам следует использовать C или неугодный C++, но не управляемый C++.</span><span class="sxs-lookup"><span data-stu-id="ab1dd-112">Note that developers should use C or unmanaged C++, but not managed C++ to write MAPI solutions.</span></span>
  
<span data-ttu-id="ab1dd-113">При реализации объекта MAPI клиент или поставщик услуг создает код для всех методов интерфейса, код для любых частных методов, которые являются специфическими для реализации, и код для поддержки частных членов данных для поддержки сведений о состоянии.</span><span class="sxs-lookup"><span data-stu-id="ab1dd-113">When a MAPI object is implemented, a client or service provider creates code for all of the interface methods, code for any private methods that are specific to the implementation, and code to support private data members for maintaining state information.</span></span> <span data-ttu-id="ab1dd-114">Код методов интерфейса должен следовать спецификациям, опубликованным MAPI, в соответствии с ожидаемым поведением документа.</span><span class="sxs-lookup"><span data-stu-id="ab1dd-114">The code for the interface methods must follow the specifications published by MAPI that document expected behavior.</span></span> 
  
<span data-ttu-id="ab1dd-115">В файле заголовок Mapidefs.h и файлах заголовок OLE имеется много макроов, которые клиенты и поставщики служб на любом языке могут использовать для определения объектов MAPI.</span><span class="sxs-lookup"><span data-stu-id="ab1dd-115">There are many macros in the Mapidefs.h header file and OLE header files that clients and service providers in either language can use to help them with their definitions of MAPI objects.</span></span> <span data-ttu-id="ab1dd-116">Например, существует макрос для определения методов каждого интерфейса MAPI.</span><span class="sxs-lookup"><span data-stu-id="ab1dd-116">For example, there is a macro to define the methods of each of the MAPI interfaces.</span></span> <span data-ttu-id="ab1dd-117">Макрос для определения методов интерфейса [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) отображается в mapidefs.h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ab1dd-117">The macro to define the methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface appears in Mapidefs.h as follows:</span></span> 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a><span data-ttu-id="ab1dd-118">См. также</span><span class="sxs-lookup"><span data-stu-id="ab1dd-118">See also</span></span>



[<span data-ttu-id="ab1dd-119">Общие сведения об объектах и интерфейсах MAPI</span><span class="sxs-lookup"><span data-stu-id="ab1dd-119">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

