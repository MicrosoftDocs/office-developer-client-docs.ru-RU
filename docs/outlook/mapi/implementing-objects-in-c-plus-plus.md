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
# <a name="implementing-objects-in-c"></a><span data-ttu-id="2a827-103">Внедрение объектов в C++</span><span class="sxs-lookup"><span data-stu-id="2a827-103">Implementing objects in C++</span></span>

<span data-ttu-id="2a827-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a827-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a827-105">C++ клиентов и поставщиков услуг определения объектов MAPI, создав классы, наследующие от интерфейсы, которые их реализации.</span><span class="sxs-lookup"><span data-stu-id="2a827-105">C++ clients and service providers define MAPI objects by creating classes that inherit from the interfaces they are implementing.</span></span> <span data-ttu-id="2a827-106">Каждый из методов интерфейса является общей, как конструктора и деструктора для класса.</span><span class="sxs-lookup"><span data-stu-id="2a827-106">Each of the interface methods is public, as are the constructor and destructor for the class.</span></span> <span data-ttu-id="2a827-107">Если класс содержит дополнительные методы, они могут быть public или private, в зависимости от реализации.</span><span class="sxs-lookup"><span data-stu-id="2a827-107">If the class has additional methods, they can be public or private, depending on the implementation.</span></span> <span data-ttu-id="2a827-108">Доступны все элементы данных.</span><span class="sxs-lookup"><span data-stu-id="2a827-108">All data members are private.</span></span> 
  
<span data-ttu-id="2a827-109">В следующем примере кода показано, как определить состояние объект C++.</span><span class="sxs-lookup"><span data-stu-id="2a827-109">The following example code shows how to define a C++ status object.</span></span> <span data-ttu-id="2a827-110">`CMyMAPIObject` Класс наследует от [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a827-110">The  `CMyMAPIObject` class inherits from the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="2a827-111">Многие макросы, используемые в этом примере определены в файле заголовка OLE Compobj.h.</span><span class="sxs-lookup"><span data-stu-id="2a827-111">Many of the macros used in this example are defined in the OLE header file Compobj.h.</span></span> <span data-ttu-id="2a827-112">Первый членов класса являются методы базового интерфейса, следуют методы наследуемых интерфейсов в порядке наследования.</span><span class="sxs-lookup"><span data-stu-id="2a827-112">The first members of the class are the methods of the base interface, followed by the methods of the inherited interfaces in order of inheritance.</span></span> <span data-ttu-id="2a827-113">После определения интерфейса являются любые дополнительные методы, конструктор и деструктор и элементов данных.</span><span class="sxs-lookup"><span data-stu-id="2a827-113">Following the interface definitions are any additional methods, the constructor and destructor, and the data members.</span></span> 
  
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

<span data-ttu-id="2a827-114">Чтобы использовать экземпляр `CMyMAPIObject` класса, C++ клиентами или поставщиками услуг делать вызов одного из методов следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2a827-114">To use an instance of the  `CMyMAPIObject` class, C++ clients or service providers make a call to one of its methods as follows:</span></span> 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a><span data-ttu-id="2a827-115">См. также</span><span class="sxs-lookup"><span data-stu-id="2a827-115">See also</span></span>

- [<span data-ttu-id="2a827-116">Реализация объектов MAPI</span><span class="sxs-lookup"><span data-stu-id="2a827-116">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

