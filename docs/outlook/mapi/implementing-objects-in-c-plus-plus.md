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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310152"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="d722b-103">Реализация объектов в C++</span><span class="sxs-lookup"><span data-stu-id="d722b-103">Implementing objects in C++</span></span>

<span data-ttu-id="d722b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d722b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d722b-105">Клиенты и поставщики услуг C++ определяют объекты MAPI, создавая классы, которые наследуются от интерфейсов, которые они реализуют.</span><span class="sxs-lookup"><span data-stu-id="d722b-105">C++ clients and service providers define MAPI objects by creating classes that inherit from the interfaces they are implementing.</span></span> <span data-ttu-id="d722b-106">Каждый из методов интерфейса является открытым, как конструктор и деструктор для класса.</span><span class="sxs-lookup"><span data-stu-id="d722b-106">Each of the interface methods is public, as are the constructor and destructor for the class.</span></span> <span data-ttu-id="d722b-107">Если у класса есть дополнительные методы, они могут быть общедоступными или частными, в зависимости от реализации.</span><span class="sxs-lookup"><span data-stu-id="d722b-107">If the class has additional methods, they can be public or private, depending on the implementation.</span></span> <span data-ttu-id="d722b-108">Все элементы данных являются частными.</span><span class="sxs-lookup"><span data-stu-id="d722b-108">All data members are private.</span></span> 
  
<span data-ttu-id="d722b-109">В приведенном ниже примере кода показано, как определить объект состояния C++.</span><span class="sxs-lookup"><span data-stu-id="d722b-109">The following example code shows how to define a C++ status object.</span></span> <span data-ttu-id="d722b-110">`CMyMAPIObject` Класс наследуется от интерфейса [имапистатус: IMAPIProp](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="d722b-110">The  `CMyMAPIObject` class inherits from the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="d722b-111">Многие макросы, используемые в этом примере, определены в файле заголовка OLE Компобж. h.</span><span class="sxs-lookup"><span data-stu-id="d722b-111">Many of the macros used in this example are defined in the OLE header file Compobj.h.</span></span> <span data-ttu-id="d722b-112">Первыми членами класса являются методы базового интерфейса, за которыми следуют методы унаследованных интерфейсов в порядке наследования.</span><span class="sxs-lookup"><span data-stu-id="d722b-112">The first members of the class are the methods of the base interface, followed by the methods of the inherited interfaces in order of inheritance.</span></span> <span data-ttu-id="d722b-113">После определения интерфейса можно добавить любые дополнительные методы, конструктор и деструктор, а также элементы данных.</span><span class="sxs-lookup"><span data-stu-id="d722b-113">Following the interface definitions are any additional methods, the constructor and destructor, and the data members.</span></span> 
  
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

<span data-ttu-id="d722b-114">Чтобы использовать экземпляр `CMyMAPIObject` класса, клиенты C++ или поставщики услуг выполняют вызов одного из методов следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d722b-114">To use an instance of the  `CMyMAPIObject` class, C++ clients or service providers make a call to one of its methods as follows:</span></span> 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a><span data-ttu-id="d722b-115">См. также</span><span class="sxs-lookup"><span data-stu-id="d722b-115">See also</span></span>

- [<span data-ttu-id="d722b-116">Реализация объектов MAPI</span><span class="sxs-lookup"><span data-stu-id="d722b-116">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

