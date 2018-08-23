---
title: Внедрение объектов в C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4c233f9855674080496b2e54ba9548a53738ead8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574729"
---
# <a name="implementing-objects-in-c"></a>Внедрение объектов в C++

**Применимо к**: Outlook 2013 | Outlook 2016 
  
C++ клиентов и поставщиков услуг определения объектов MAPI, создав классы, наследующие от интерфейсы, которые их реализации. Каждый из методов интерфейса является общей, как конструктора и деструктора для класса. Если класс содержит дополнительные методы, они могут быть public или private, в зависимости от реализации. Доступны все элементы данных. 
  
В следующем примере кода показано, как определить состояние объект C++. `CMyMAPIObject` Класс наследует от [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) интерфейса. Многие макросы, используемые в этом примере определены в файле заголовка OLE Compobj.h. Первый членов класса являются методы базового интерфейса, следуют методы наследуемых интерфейсов в порядке наследования. После определения интерфейса являются любые дополнительные методы, конструктор и деструктор и элементов данных. 
  
```cpp
class  CMyMAPIObject : public IMAPIStatus
{
public:
// Methods of IUnknown.
    STDMETHODIMP QueryInterface (REFIID riid, LPVOID * ppvObj);
    STDMETHODIMP_(ULONG) AddRef ();
    STDMETHODIMP_(ULONG) Release ();
    MAPI_IMAPIPROP_METHODS(IMPL);
    MAPI_IMAPISTATUS_METHODS(IMPL);
// Other methods specific to CMyMAPIObject.
    BOOL WINAPI Method1 ();
    void WINAPI Method2 ();
// Constructors and destructors.
public :
    CMyMAPIObject () {};
    ~CMyMAPIObject () {};
// Data members specific to CMyMAPIObject.
private :
    ULONG               m_cRef;
    CAnotherObj *       m_pObj;
};
 
```

Чтобы использовать экземпляр `CMyMAPIObject` класса, C++ клиентами или поставщиками услуг делать вызов одного из методов следующим образом: 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a>См. также

- [Реализация объектов MAPI](implementing-mapi-objects.md)

