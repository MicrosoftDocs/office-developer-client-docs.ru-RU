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
ms.openlocfilehash: d53304dd74a0e54974d479c66637079cd48b2fc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809308"
---
# <a name="implementing-mapi-objects"></a><span data-ttu-id="b513e-103">Реализация объектов MAPI</span><span class="sxs-lookup"><span data-stu-id="b513e-103">Implementing MAPI Objects</span></span>

  
  
<span data-ttu-id="b513e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b513e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b513e-105">Объекты MAPI можно реализовать с помощью классов C++ или C структуры данных, в зависимости от языка и API Настройка клиента или с помощью поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="b513e-105">MAPI objects can be implemented by using C++ classes or C data structures, depending on the language and the API set a client or service provider is using.</span></span> <span data-ttu-id="b513e-106">Поставщиков услуг может быть написан на C или C++ с помощью интерфейса поставщика службы MAPI; клиентские приложения также можно использовать C или C++.</span><span class="sxs-lookup"><span data-stu-id="b513e-106">Service providers can be written in C or C++ with the MAPI service provider interface; client applications can also use C or C++.</span></span> <span data-ttu-id="b513e-107">Если это возможно клиентов и поставщиков услуг, использующих интерфейс программирования объектно ориентированные следует использовать C++.</span><span class="sxs-lookup"><span data-stu-id="b513e-107">If possible, clients and service providers that use the object-oriented programming interface should use C++.</span></span> 
  
<span data-ttu-id="b513e-108">C++ является предпочтительным вариантом, потому что MAPI — это технология объектно ориентированные и C++ могут работать легче в объектно ориентированные разработки.</span><span class="sxs-lookup"><span data-stu-id="b513e-108">C++ is the preferred choice because MAPI is an object-oriented technology, and C++ lends itself more readily to object-oriented development.</span></span> <span data-ttu-id="b513e-109">Такой код более простой и более простые, что упрощает обслуживание.</span><span class="sxs-lookup"><span data-stu-id="b513e-109">The resulting code is simpler and more straightforward, making it easier to maintain.</span></span> <span data-ttu-id="b513e-110">Документация по MAPI, записывается в основном для разработчиков C++; все описания синтаксиса для методов интерфейса MAPI в этой справке, в C++.</span><span class="sxs-lookup"><span data-stu-id="b513e-110">The MAPI documentation is written primarily for C++ developers; all of the syntax descriptions for the MAPI interface methods in this Reference are in C++.</span></span>
  
<span data-ttu-id="b513e-111">Разработчики могут использовать Microsoft Visual Studio и средства сторонних производителей разработки для разработки решений, которые могут вызывать MAPI.</span><span class="sxs-lookup"><span data-stu-id="b513e-111">Developers can use Microsoft Visual Studio and third-party development tools to develop solutions that call MAPI.</span></span> <span data-ttu-id="b513e-112">Обратите внимание на то, что следует использовать C или C++ неуправляемые разработчиков (en), но не управляемый C++ для записи решений MAPI.</span><span class="sxs-lookup"><span data-stu-id="b513e-112">Note that developers should use C or unmanaged C++, but not managed C++ to write MAPI solutions.</span></span>
  
<span data-ttu-id="b513e-113">При реализации объект MAPI клиента или поставщика создает код для всех методов интерфейса, код для объявления частных методы, которые специфичны для реализации и код для поддержки личных данных участников по обслуживанию сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="b513e-113">When a MAPI object is implemented, a client or service provider creates code for all of the interface methods, code for any private methods that are specific to the implementation, and code to support private data members for maintaining state information.</span></span> <span data-ttu-id="b513e-114">Код для методов интерфейса должны соответствовать спецификации издательством MAPI, которые документов поведению.</span><span class="sxs-lookup"><span data-stu-id="b513e-114">The code for the interface methods must follow the specifications published by MAPI that document expected behavior.</span></span> 
  
<span data-ttu-id="b513e-115">Существует множество макросов в файл заголовка Mapidefs.h и OLE файлы заголовков, которые клиенты и поставщики услуг на любом языке можно использовать для справки при их определения объектов MAPI.</span><span class="sxs-lookup"><span data-stu-id="b513e-115">There are many macros in the Mapidefs.h header file and OLE header files that clients and service providers in either language can use to help them with their definitions of MAPI objects.</span></span> <span data-ttu-id="b513e-116">Например такое макрос для определения методов каждого интерфейса MAPI.</span><span class="sxs-lookup"><span data-stu-id="b513e-116">For example, there is a macro to define the methods of each of the MAPI interfaces.</span></span> <span data-ttu-id="b513e-117">Макрос для определения методов интерфейс [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) в Mapidefs.h бы выглядел следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b513e-117">The macro to define the methods of the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) interface appears in Mapidefs.h as follows:</span></span> 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a><span data-ttu-id="b513e-118">См. также</span><span class="sxs-lookup"><span data-stu-id="b513e-118">See also</span></span>



[<span data-ttu-id="b513e-119">Обзор интерфейса и объект MAPI</span><span class="sxs-lookup"><span data-stu-id="b513e-119">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

