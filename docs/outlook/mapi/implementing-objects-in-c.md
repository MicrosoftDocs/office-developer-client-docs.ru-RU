---
title: Реализация объектов в C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 24fc4d78-726d-40ff-bad2-25dc298bd51a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6026e697cc31545bf7ef518fcbd33ea8db48af5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414944"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="59a47-103">Реализация объектов в C</span><span class="sxs-lookup"><span data-stu-id="59a47-103">Implementing objects in C</span></span>

<span data-ttu-id="59a47-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59a47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59a47-105">Клиентские приложения и поставщики услуг, написанные в C, определяют объекты MAPI путем создания структуры данных и массива упорядоченных указателей функций, известных как виртуальная таблица функций или vtable.</span><span class="sxs-lookup"><span data-stu-id="59a47-105">Client applications and service providers written in C define MAPI objects by creating a data structure and an array of ordered function pointers known as a virtual function table, or vtable.</span></span> <span data-ttu-id="59a47-106">Указатель на vtable должен быть первым членом структуры данных.</span><span class="sxs-lookup"><span data-stu-id="59a47-106">A pointer to the vtable must be the first member of the data structure.</span></span>
  
<span data-ttu-id="59a47-107">В самом vtable есть один указатель для каждого метода в каждом интерфейсе, поддерживаемом объектом.</span><span class="sxs-lookup"><span data-stu-id="59a47-107">In the vtable itself, there is one pointer for every method in each interface supported by the object.</span></span> <span data-ttu-id="59a47-108">Порядок указателей должен следовать порядку методов в спецификации интерфейса, опубликованной в заглавном файле Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="59a47-108">The order of the pointers must follow the order of the methods in the interface specification published in the Mapidefs.h header file.</span></span> <span data-ttu-id="59a47-109">Каждый указатель функции в vtable за набором адресов фактической реализации метода.</span><span class="sxs-lookup"><span data-stu-id="59a47-109">Each function pointer in the vtable is set to the address of the actual implementation of the method.</span></span> <span data-ttu-id="59a47-110">В C++компилятор автоматически настраивает vtable.</span><span class="sxs-lookup"><span data-stu-id="59a47-110">In C++, the compiler automatically sets up the vtable.</span></span> <span data-ttu-id="59a47-111">В C это не так.</span><span class="sxs-lookup"><span data-stu-id="59a47-111">In C, it does not.</span></span> 
  
<span data-ttu-id="59a47-112">На следующем рисунке показано, как это работает.</span><span class="sxs-lookup"><span data-stu-id="59a47-112">The following illustration shows how this works.</span></span> <span data-ttu-id="59a47-113">Поле слева представляет клиента, который должен использовать объект поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="59a47-113">The box on the far left represents a client that needs to use a service provider object.</span></span> <span data-ttu-id="59a47-114">В ходе сеанса клиент получает указатель на объект **lpObject.**</span><span class="sxs-lookup"><span data-stu-id="59a47-114">Through the session, the client obtains a pointer to the object, **lpObject**.</span></span> <span data-ttu-id="59a47-115">В объекте сначала отображается vtable, а затем личные данные и методы.</span><span class="sxs-lookup"><span data-stu-id="59a47-115">The vtable appears first in the object followed by private data and methods.</span></span> <span data-ttu-id="59a47-116">Указатель vtable указывает на фактический vtable, который содержит указатели для каждой реализации методов в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="59a47-116">The vtable pointer points to the actual vtable, which contains pointers to each of the implementations of the methods in the interface.</span></span> 
  
<span data-ttu-id="59a47-117">**Реализация объекта**</span><span class="sxs-lookup"><span data-stu-id="59a47-117">**Object implementation**</span></span>
  
<span data-ttu-id="59a47-118">![Объектная реализация](media/amapi_42.gif "объекта реализации")</span><span class="sxs-lookup"><span data-stu-id="59a47-118">![Object implementation](media/amapi_42.gif "Object implementation")</span></span>
  
<span data-ttu-id="59a47-119">В следующем примере кода показано, как поставщик C-служб может определить простой объект состояния.</span><span class="sxs-lookup"><span data-stu-id="59a47-119">The following code example shows how a C service provider can define a simple status object.</span></span> <span data-ttu-id="59a47-120">Первый член — это указатель vtable; остальная часть объекта состоит из участников данных.</span><span class="sxs-lookup"><span data-stu-id="59a47-120">The first member is the vtable pointer; the rest of the object is made up of data members.</span></span> 
  
```C
typedef struct _MYSTATUSOBJECT
{
    const STATUS_Vtbl FAR *lpVtbl;
    ULONG              cRef;
    ANOTHEROBJ        *pObj;
    LPMAPIPROP         lpProp;
    LPFREEBUFFER       lpFreeBuf;
} MYSTATUSOBJECT, *LPMYSTATUSOBJ;
 
```

<span data-ttu-id="59a47-121">Поскольку этот объект является объектом состояния, vtable включает указатели на реализацию каждого из методов интерфейса [IMAPIStatus: IMAPIProp,](imapistatusimapiprop.md) а также указатели на реализацию каждого из методов в базовых интерфейсах — **IUnknown** и **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="59a47-121">Because this object is a status object, the vtable includes pointers to implementations of each of the methods in the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, as well as pointers to implementations of each of the methods in the base interfaces — **IUnknown** and **IMAPIProp**.</span></span> <span data-ttu-id="59a47-122">Порядок методов в vtable соответствует указанному порядку, указанному в файле заглавного файла Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="59a47-122">The order of methods in the vtable matches the specified order as defined in the Mapidefs.h header file.</span></span>
  
```js
static const MYOBJECT_Vtbl vtblSTATUS =
{
    STATUS_QueryInterface,
    STATUS_AddRef,
    STATUS_Release,
    STATUS_GetLastError,
    STATUS_SaveChanges,
    STATUS_GetProps,
    STATUS_GetPropList,
    STATUS_OpenProperty,
    STATUS_SetProps,
    STATUS_DeleteProps,
    STATUS_CopyTo,
    STATUS_CopyProps,
    STATUS_GetNamesFromIDs,
    STATUS_GetIDsFromNames,
    STATUS_ValidateState,
    STATUS_SettingsDialog,
    STATUS_ChangePassword,
    STATUS_FlushQueues
};
 
```

<span data-ttu-id="59a47-123">Клиенты и поставщики услуг, написанные в C, косвенно используют объекты через vtable и добавляют указатель объекта в качестве первого параметра в каждом вызове.</span><span class="sxs-lookup"><span data-stu-id="59a47-123">Clients and service providers written in C use objects indirectly through the vtable and add an object pointer as the first parameter in every call.</span></span> <span data-ttu-id="59a47-124">Для каждого вызова к методу интерфейса MAPI требуется указатель на объект, который называется его первым параметром.</span><span class="sxs-lookup"><span data-stu-id="59a47-124">Every call to a MAPI interface method requires a pointer to the object being called as its first parameter.</span></span> <span data-ttu-id="59a47-125">C++ определяет специальный указатель, известный как **этот** указатель для этой цели.</span><span class="sxs-lookup"><span data-stu-id="59a47-125">C++ defines a special pointer known as the **this** pointer for this purpose.</span></span> <span data-ttu-id="59a47-126">Компилятор C++ неявно добавляет этот **указатель** в качестве первого параметра для каждого вызова метода.</span><span class="sxs-lookup"><span data-stu-id="59a47-126">The C++ compiler implicitly adds the **this** pointer as the first parameter to every method call.</span></span> <span data-ttu-id="59a47-127">В C такой указатель не существует; она должна быть явно добавлена.</span><span class="sxs-lookup"><span data-stu-id="59a47-127">In C there is no such pointer; it must be explicitly added.</span></span> 
  
<span data-ttu-id="59a47-128">В следующем коде показано, как клиент может звонить в экземпляр MYSTATUSOBJECT:</span><span class="sxs-lookup"><span data-stu-id="59a47-128">The following code demonstrates how a client can make a call to an instance of MYSTATUSOBJECT:</span></span>
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a><span data-ttu-id="59a47-129">См. также</span><span class="sxs-lookup"><span data-stu-id="59a47-129">See also</span></span>

- [<span data-ttu-id="59a47-130">Реализация объектов MAPI</span><span class="sxs-lookup"><span data-stu-id="59a47-130">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

