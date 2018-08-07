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
ms.openlocfilehash: ea9f37183f33459b09f2730b3efbb7afed3d4766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809314"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="a6ce8-103">Внедрение объектов в C++</span><span class="sxs-lookup"><span data-stu-id="a6ce8-103">Implementing objects in C++</span></span>

<span data-ttu-id="a6ce8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a6ce8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a6ce8-105">C++ клиентов и поставщиков услуг определения объектов MAPI, создав классы, наследующие от интерфейсы, которые их реализации.</span><span class="sxs-lookup"><span data-stu-id="a6ce8-105">C++ clients and service providers define MAPI objects by creating classes that inherit from the interfaces they are implementing.</span></span> <span data-ttu-id="a6ce8-106">Каждый из методов интерфейса является общей, как конструктора и деструктора для класса.</span><span class="sxs-lookup"><span data-stu-id="a6ce8-106">Each of the interface methods is public, as are the constructor and destructor for the class.</span></span> <span data-ttu-id="a6ce8-107">Если класс содержит дополнительные методы, они могут быть public или private, в зависимости от реализации.</span><span class="sxs-lookup"><span data-stu-id="a6ce8-107">If the class has additional methods, they can be public or private, depending on the implementation.</span></span> <span data-ttu-id="a6ce8-108">Доступны все элементы данных.</span><span class="sxs-lookup"><span data-stu-id="a6ce8-108">All data members are private.</span></span> 
  
<span data-ttu-id="a6ce8-109">В следующем примере кода показано, как определить состояние объект C++.</span><span class="sxs-lookup"><span data-stu-id="a6ce8-109">The following example code shows how to define a C++ status object.</span></span> <span data-ttu-id="a6ce8-110">`CMyMAPIObject` Класс наследует от [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a6ce8-110">The  `CMyMAPIObject` class inherits from the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="a6ce8-111">Многие макросы, используемые в этом примере определены в файле заголовка OLE Compobj.h.</span><span class="sxs-lookup"><span data-stu-id="a6ce8-111">Many of the macros used in this example are defined in the OLE header file Compobj.h.</span></span> <span data-ttu-id="a6ce8-112">Первый членов класса являются методы базового интерфейса, следуют методы наследуемых интерфейсов в порядке наследования.</span><span class="sxs-lookup"><span data-stu-id="a6ce8-112">The first members of the class are the methods of the base interface, followed by the methods of the inherited interfaces in order of inheritance.</span></span> <span data-ttu-id="a6ce8-113">После определения интерфейса являются любые дополнительные методы, конструктор и деструктор и элементов данных.</span><span class="sxs-lookup"><span data-stu-id="a6ce8-113">Following the interface definitions are any additional methods, the constructor and destructor, and the data members.</span></span> 
  
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

<span data-ttu-id="a6ce8-114">Чтобы использовать экземпляр `CMyMAPIObject` класса, C++ клиентами или поставщиками услуг делать вызов одного из методов следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a6ce8-114">To use an instance of the  `CMyMAPIObject` class, C++ clients or service providers make a call to one of its methods as follows:</span></span> 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a><span data-ttu-id="a6ce8-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a6ce8-115">See also</span></span>

- [<span data-ttu-id="a6ce8-116">Реализация объектов MAPI</span><span class="sxs-lookup"><span data-stu-id="a6ce8-116">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

