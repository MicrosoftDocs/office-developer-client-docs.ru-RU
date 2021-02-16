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
# <a name="implementing-a-sample-object"></a>Реализация образца объекта

**Относится к**: Outlook 2013 | Outlook 2016 
  
Объекты приемника advise — объекты, которые поддерживают [интерфейс IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) — это объекты MAPI, которые клиентские приложения реализуют для обработки уведомлений. **IMAPIAdviseSink** наследует непосредственно от [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) и содержит только один **метод, OnNotify**. Поэтому для реализации объекта приемника консультации клиент создает код для трех методов **в IUnknown** и [OnNotify.](imapiadvisesink-onnotify.md)
  
Файл заголовок Mapidefs.h определяет реализацию интерфейса **IMAPIAdviseSink** с помощью DECLARE_MAPI_INTERFACE **следующим** образом:
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

Клиенты, которые реализуют объекты-мяконсульты, могут определять свои интерфейсы в своих объектах **вручную** или с помощью MAPI_IUNKNOWN_METHODS и **MAPI_IMAPIADVISESINK_METHODS** макроса. Для обеспечения согласованности объектов и экономии времени и усилий, реализующих объекты, следует по возможности использовать макрос интерфейса. 
  
Реализация методов [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) и [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) относительно проста, так как обычно требуется всего несколько строк кода. Таким образом, клиенты и поставщики услуг, реализуют объекты, могут использовать собственные реализации **AddRef** и **Release.** В следующем коде показано, как определить объект-тоник C++ с помощью внедренных реализаций **AddRef** и **Release.**
  
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

В C объект-источник рекомендации состоит из следующих элементов:
  
- Указатель на vtable, который содержит указатели на реализации каждого из методов **в IUnknown** и **IMAPIAdviseSink**.
    
- Члены данных.
    
В следующем примере кода показано, как определить объект-конструктивный объект в C и создать его vtable. 
  
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

После объявления объекта в C необходимо инициализировать его, настроив указатель vtable на адрес построенной vtable, как показано в следующем коде:
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a>См. также

- [Обзор свойств MAPI](mapi-property-overview.md)
- [Реализация объектов MAPI](implementing-mapi-objects.md)

