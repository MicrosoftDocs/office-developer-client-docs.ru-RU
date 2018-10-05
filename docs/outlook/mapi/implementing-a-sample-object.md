---
title: Реализация объекта образца
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23b6ad1a-0b50-429f-8819-ab72c56581c2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a681e68c0718e49da331946d75ecb7b4fab7afe2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396794"
---
# <a name="implementing-a-sample-object"></a><span data-ttu-id="40748-103">Реализация объекта образца</span><span class="sxs-lookup"><span data-stu-id="40748-103">Implementing a sample object</span></span>

<span data-ttu-id="40748-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40748-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40748-105">Уведомить приемник объекты — объекты, поддерживающие [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) интерфейс — являются MAPI объектов, что клиентские приложения реализовать для обработки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="40748-105">Advise sink objects — objects that support the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface — are MAPI objects that client applications implement for processing notifications.</span></span> <span data-ttu-id="40748-106">**IMAPIAdviseSink** наследует непосредственно от [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) и содержит только один метод **OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="40748-106">**IMAPIAdviseSink** inherits directly from [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) and contains only one method, **OnNotify**.</span></span> <span data-ttu-id="40748-107">Таким образом для реализации объекта приемник уведомлений, клиент создает код для трех методы **IUnknown** и [OnNotify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="40748-107">Therefore, to implement an advise sink object, a client creates code for the three methods in **IUnknown** and for [OnNotify](imapiadvisesink-onnotify.md).</span></span>
  
<span data-ttu-id="40748-108">Файл заголовка Mapidefs.h определяет реализация интерфейса **IMAPIAdviseSink** с помощью **DECLARE_MAPI_INTERFACE**следующим образом:</span><span class="sxs-lookup"><span data-stu-id="40748-108">The Mapidefs.h header file defines an **IMAPIAdviseSink** interface implementation by using **DECLARE_MAPI_INTERFACE**, as follows:</span></span>
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

<span data-ttu-id="40748-109">Клиенты, которые реализуют уведомить объектов приемника интерфейсы можно определить их в своих объектов вручную или с помощью макросов **MAPI_IUNKNOWN_METHODS** и **MAPI_IMAPIADVISESINK_METHODS** .</span><span class="sxs-lookup"><span data-stu-id="40748-109">Clients that implement advise sink objects can define their interfaces in their objects manually or with the **MAPI_IUNKNOWN_METHODS** and **MAPI_IMAPIADVISESINK_METHODS** macros.</span></span> <span data-ttu-id="40748-110">Объект специалистов по внедрению следует использовать макросы интерфейс по возможности для обеспечения согласованности между объектами и сохранить время и силы.</span><span class="sxs-lookup"><span data-stu-id="40748-110">Object implementers should use the interface macros whenever possible to ensure consistency across objects and to save time and effort.</span></span> 
  
<span data-ttu-id="40748-111">Реализация методов [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) и [функции IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) будет достаточно простым, так как обычно требуется только несколько строк текста.</span><span class="sxs-lookup"><span data-stu-id="40748-111">Implementing the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods is relatively simple because typically only a few lines of code are needed.</span></span> <span data-ttu-id="40748-112">Таким образом клиентов и поставщиков услуг, которые реализуют объекты можно делать их реализаций встроенных **AddRef** и **Release** .</span><span class="sxs-lookup"><span data-stu-id="40748-112">Therefore, clients and service providers that implement objects can make their **AddRef** and **Release** implementations inline.</span></span> <span data-ttu-id="40748-113">Ниже показано, как определить C++ объект приемника с помощью встроенного реализации **AddRef** и **Release**рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="40748-113">The following code shows how to define a C++ advise sink object with inline implementations of **AddRef** and **Release**.</span></span>
  
```cpp
class  CMAPIAdviseSink : public IMAPIAdviseSink
{
public:
    STDMETHODIMP QueryInterface
                    (REFIID                     riid,
                     LPVOID *                   ppvObj);
    inline STDMETHODIMP_(ULONG) AddRef
                    () { InterlockedIncrement(m_cRef);
                         ++m_cRef;
                         InterlockedDecrement(m_cRef);
                         return m_cRef; };
    inline STDMETHODIMP_(ULONG) Release
                    () { InterlockedIncrement(m_cRef);
                         ULONG ulCount = --m_cRef;
                         InterlockedDecrement(m_cRef);
                         if (!ulCount)  delete this;
                         return ulCount;};
    MAPI_IMAPIADVISESINK_METHODS(IMPL);
    BOOL WINAPI AddConnection (LPMDB pMDBObj, ULONG ulConnection);
    void WINAPI RemoveAllLinks (LPMDB pMDBObj);
// Constructors and destructors.
public :
    inline CMAPIAdviseSink  (CStoreClient * pStore)
                            { m_cRef = 1;
                              m_ulConnection = 0;
                              m_pStore = pStore;
                              AddRef;};
    ~CMAPIAdviseSink () {Release};
private :
    ULONG               m_cRef;
    CStoreClient *      m_pStore;
    ULONG               m_ulConnection;
};
 
```

<span data-ttu-id="40748-114">В C объект приемника уведомлений состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="40748-114">In C, the advise sink object is composed of the following elements:</span></span>
  
- <span data-ttu-id="40748-115">Указатель vtable, который содержит указатели на реализации каждого из методов в **IUnknown** и **IMAPIAdviseSink**.</span><span class="sxs-lookup"><span data-stu-id="40748-115">A pointer to a vtable that contains pointers to implementations of each of the methods in **IUnknown** and **IMAPIAdviseSink**.</span></span>
    
- <span data-ttu-id="40748-116">Элементы данных.</span><span class="sxs-lookup"><span data-stu-id="40748-116">Data members.</span></span>
    
<span data-ttu-id="40748-117">В следующем примере кода показано, как определить объект приемника уведомлений в C и создать его vtable.</span><span class="sxs-lookup"><span data-stu-id="40748-117">The following code example shows how to define an advise sink object in C and construct its vtable.</span></span> 
  
```cpp
// Object definition.
typedef struct _ADVISESINK
{
    const ADVISE_Vtbl FAR *    lpVtbl;
    ULONG             cRef;
    STORECLIENT      *pStore;
    ULONG             ulConnection;
} ADVISESINK, *LPADVISESINK;
// vtable definition.
static const ADVISE_Vtbl vtblADVISE =
{
    ADVISE_QueryInterface,
    ADVISE_AddRef,
    ADVISE_Release,
    ADVISE_OnNotify
};
 
```

<span data-ttu-id="40748-118">После объявления переменной объекта в C вы должны инициализировать путем установки для параметра адрес созданного vtable указателя vtable, как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="40748-118">After you declare an object in C, you must initialize it by setting the vtable pointer to the address of the constructed vtable, as shown in the following code:</span></span>
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a><span data-ttu-id="40748-119">См. также</span><span class="sxs-lookup"><span data-stu-id="40748-119">See also</span></span>

- [<span data-ttu-id="40748-120">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="40748-120">MAPI Property Overview</span></span>](mapi-property-overview.md)
- [<span data-ttu-id="40748-121">Реализация объектов MAPI</span><span class="sxs-lookup"><span data-stu-id="40748-121">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

