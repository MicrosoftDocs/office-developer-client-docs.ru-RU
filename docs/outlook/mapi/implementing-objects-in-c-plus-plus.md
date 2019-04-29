---
title: Реализация объектов в C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 89247ca1b263d6f06af73f1ffa14709a2aff23de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432956"
---
# <a name="implementing-objects-in-c"></a>Реализация объектов в C++

**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиенты и поставщики услуг C++ определяют объекты MAPI, создавая классы, которые наследуются от интерфейсов, которые они реализуют. Каждый из методов интерфейса является открытым, как конструктор и деструктор для класса. Если у класса есть дополнительные методы, они могут быть общедоступными или частными, в зависимости от реализации. Все элементы данных являются частными. 
  
В приведенном ниже примере кода показано, как определить объект состояния C++. `CMyMAPIObject` Класс наследуется от интерфейса [имапистатус: IMAPIProp](imapistatusimapiprop.md) . Многие макросы, используемые в этом примере, определены в файле заголовка OLE Компобж. h. Первыми членами класса являются методы базового интерфейса, за которыми следуют методы унаследованных интерфейсов в порядке наследования. После определения интерфейса можно добавить любые дополнительные методы, конструктор и деструктор, а также элементы данных. 
  
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

Чтобы использовать экземпляр `CMyMAPIObject` класса, клиенты C++ или поставщики услуг выполняют вызов одного из методов следующим образом: 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a>См. также

- [Реализация объектов MAPI](implementing-mapi-objects.md)

