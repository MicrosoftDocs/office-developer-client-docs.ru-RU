---
title: Реализация образца объекта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23b6ad1a-0b50-429f-8819-ab72c56581c2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a681e68c0718e49da331946d75ecb7b4fab7afe2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332832"
---
# <a name="implementing-a-sample-object"></a><span data-ttu-id="d57d2-103">Реализация образца объекта</span><span class="sxs-lookup"><span data-stu-id="d57d2-103">Implementing a sample object</span></span>

<span data-ttu-id="d57d2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d57d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d57d2-105">Объекты приемника advise — объекты, которые поддерживают [интерфейс IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) — это объекты MAPI, которые клиентские приложения реализуют для обработки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d57d2-105">Advise sink objects — objects that support the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface — are MAPI objects that client applications implement for processing notifications.</span></span> <span data-ttu-id="d57d2-106">**IMAPIAdviseSink** наследует непосредственно от [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) и содержит только один **метод, OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="d57d2-106">**IMAPIAdviseSink** inherits directly from [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) and contains only one method, **OnNotify**.</span></span> <span data-ttu-id="d57d2-107">Поэтому для реализации объекта приемника консультации клиент создает код для трех методов **в IUnknown** и [OnNotify.](imapiadvisesink-onnotify.md)</span><span class="sxs-lookup"><span data-stu-id="d57d2-107">Therefore, to implement an advise sink object, a client creates code for the three methods in **IUnknown** and for [OnNotify](imapiadvisesink-onnotify.md).</span></span>
  
<span data-ttu-id="d57d2-108">Файл заголовок Mapidefs.h определяет реализацию интерфейса **IMAPIAdviseSink** с помощью DECLARE_MAPI_INTERFACE **следующим** образом:</span><span class="sxs-lookup"><span data-stu-id="d57d2-108">The Mapidefs.h header file defines an **IMAPIAdviseSink** interface implementation by using **DECLARE_MAPI_INTERFACE**, as follows:</span></span>
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

<span data-ttu-id="d57d2-109">Клиенты, которые реализуют объекты-мяконсульты, могут определять свои интерфейсы в своих объектах **вручную** или с помощью MAPI_IUNKNOWN_METHODS и **MAPI_IMAPIADVISESINK_METHODS** макроса.</span><span class="sxs-lookup"><span data-stu-id="d57d2-109">Clients that implement advise sink objects can define their interfaces in their objects manually or with the **MAPI_IUNKNOWN_METHODS** and **MAPI_IMAPIADVISESINK_METHODS** macros.</span></span> <span data-ttu-id="d57d2-110">Для обеспечения согласованности объектов и экономии времени и усилий, реализующих объекты, следует по возможности использовать макрос интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d57d2-110">Object implementers should use the interface macros whenever possible to ensure consistency across objects and to save time and effort.</span></span> 
  
<span data-ttu-id="d57d2-111">Реализация методов [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) и [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) относительно проста, так как обычно требуется всего несколько строк кода.</span><span class="sxs-lookup"><span data-stu-id="d57d2-111">Implementing the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods is relatively simple because typically only a few lines of code are needed.</span></span> <span data-ttu-id="d57d2-112">Таким образом, клиенты и поставщики услуг, реализуют объекты, могут использовать собственные реализации **AddRef** и **Release.**</span><span class="sxs-lookup"><span data-stu-id="d57d2-112">Therefore, clients and service providers that implement objects can make their **AddRef** and **Release** implementations inline.</span></span> <span data-ttu-id="d57d2-113">В следующем коде показано, как определить объект-тоник C++ с помощью внедренных реализаций **AddRef** и **Release.**</span><span class="sxs-lookup"><span data-stu-id="d57d2-113">The following code shows how to define a C++ advise sink object with inline implementations of **AddRef** and **Release**.</span></span>
  
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

<span data-ttu-id="d57d2-114">В C объект-источник рекомендации состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="d57d2-114">In C, the advise sink object is composed of the following elements:</span></span>
  
- <span data-ttu-id="d57d2-115">Указатель на vtable, который содержит указатели на реализации каждого из методов **в IUnknown** и **IMAPIAdviseSink**.</span><span class="sxs-lookup"><span data-stu-id="d57d2-115">A pointer to a vtable that contains pointers to implementations of each of the methods in **IUnknown** and **IMAPIAdviseSink**.</span></span>
    
- <span data-ttu-id="d57d2-116">Члены данных.</span><span class="sxs-lookup"><span data-stu-id="d57d2-116">Data members.</span></span>
    
<span data-ttu-id="d57d2-117">В следующем примере кода показано, как определить объект-конструктивный объект в C и создать его vtable.</span><span class="sxs-lookup"><span data-stu-id="d57d2-117">The following code example shows how to define an advise sink object in C and construct its vtable.</span></span> 
  
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

<span data-ttu-id="d57d2-118">После объявления объекта в C необходимо инициализировать его, настроив указатель vtable на адрес построенной vtable, как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="d57d2-118">After you declare an object in C, you must initialize it by setting the vtable pointer to the address of the constructed vtable, as shown in the following code:</span></span>
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a><span data-ttu-id="d57d2-119">См. также</span><span class="sxs-lookup"><span data-stu-id="d57d2-119">See also</span></span>

- [<span data-ttu-id="d57d2-120">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="d57d2-120">MAPI Property Overview</span></span>](mapi-property-overview.md)
- [<span data-ttu-id="d57d2-121">Реализация объектов MAPI</span><span class="sxs-lookup"><span data-stu-id="d57d2-121">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

