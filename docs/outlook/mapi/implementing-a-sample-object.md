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
# <a name="implementing-a-sample-object"></a>Реализация объекта образца

**Относится к**: Outlook 2013 | Outlook 2016 
  
Уведомить приемник объекты — объекты, поддерживающие [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) интерфейс — являются MAPI объектов, что клиентские приложения реализовать для обработки уведомлений. **IMAPIAdviseSink** наследует непосредственно от [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) и содержит только один метод **OnNotify**. Таким образом для реализации объекта приемник уведомлений, клиент создает код для трех методы **IUnknown** и [OnNotify](imapiadvisesink-onnotify.md).
  
Файл заголовка Mapidefs.h определяет реализация интерфейса **IMAPIAdviseSink** с помощью **DECLARE_MAPI_INTERFACE**следующим образом:
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

Клиенты, которые реализуют уведомить объектов приемника интерфейсы можно определить их в своих объектов вручную или с помощью макросов **MAPI_IUNKNOWN_METHODS** и **MAPI_IMAPIADVISESINK_METHODS** . Объект специалистов по внедрению следует использовать макросы интерфейс по возможности для обеспечения согласованности между объектами и сохранить время и силы. 
  
Реализация методов [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) и [функции IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) будет достаточно простым, так как обычно требуется только несколько строк текста. Таким образом клиентов и поставщиков услуг, которые реализуют объекты можно делать их реализаций встроенных **AddRef** и **Release** . Ниже показано, как определить C++ объект приемника с помощью встроенного реализации **AddRef** и **Release**рекомендаций.
  
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

В C объект приемника уведомлений состоит из следующих элементов:
  
- Указатель vtable, который содержит указатели на реализации каждого из методов в **IUnknown** и **IMAPIAdviseSink**.
    
- Элементы данных.
    
В следующем примере кода показано, как определить объект приемника уведомлений в C и создать его vtable. 
  
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

После объявления переменной объекта в C вы должны инициализировать путем установки для параметра адрес созданного vtable указателя vtable, как показано в следующем коде:
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a>См. также

- [Обзор свойств MAPI](mapi-property-overview.md)
- [Реализация объектов MAPI](implementing-mapi-objects.md)

