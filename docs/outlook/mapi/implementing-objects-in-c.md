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
# <a name="implementing-objects-in-c"></a><span data-ttu-id="ecb68-103">Реализация объектов в C</span><span class="sxs-lookup"><span data-stu-id="ecb68-103">Implementing objects in C</span></span>

<span data-ttu-id="ecb68-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecb68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecb68-105">Клиентские приложения и поставщики услуг, написанные на языке C, определяют объекты MAPI, создавая структуру данных и массив упорядоченных указателей функций, которые называются таблицей виртуальной функции или виртуальной таблицей.</span><span class="sxs-lookup"><span data-stu-id="ecb68-105">Client applications and service providers written in C define MAPI objects by creating a data structure and an array of ordered function pointers known as a virtual function table, or vtable.</span></span> <span data-ttu-id="ecb68-106">Указатель на таблицу vtable должен быть первым членом структуры данных.</span><span class="sxs-lookup"><span data-stu-id="ecb68-106">A pointer to the vtable must be the first member of the data structure.</span></span>
  
<span data-ttu-id="ecb68-107">В самой таблице vtable существует один указатель для каждого метода в каждом интерфейсе, поддерживаемом объектом.</span><span class="sxs-lookup"><span data-stu-id="ecb68-107">In the vtable itself, there is one pointer for every method in each interface supported by the object.</span></span> <span data-ttu-id="ecb68-108">Порядок указателей должен соответствовать порядку методов в спецификации интерфейса, опубликованной в файле заголовка MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="ecb68-108">The order of the pointers must follow the order of the methods in the interface specification published in the Mapidefs.h header file.</span></span> <span data-ttu-id="ecb68-109">Для каждого указателя функции в таблице vtable задается адрес фактической реализации метода.</span><span class="sxs-lookup"><span data-stu-id="ecb68-109">Each function pointer in the vtable is set to the address of the actual implementation of the method.</span></span> <span data-ttu-id="ecb68-110">В C++ компилятор автоматически настраивает виртуальную таблицу (vtable).</span><span class="sxs-lookup"><span data-stu-id="ecb68-110">In C++, the compiler automatically sets up the vtable.</span></span> <span data-ttu-id="ecb68-111">В C это не так.</span><span class="sxs-lookup"><span data-stu-id="ecb68-111">In C, it does not.</span></span> 
  
<span data-ttu-id="ecb68-112">На следующем рисунке показано, как это работает.</span><span class="sxs-lookup"><span data-stu-id="ecb68-112">The following illustration shows how this works.</span></span> <span data-ttu-id="ecb68-113">Поле в дальнем левом углу представляет клиент, который должен использовать объект поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="ecb68-113">The box on the far left represents a client that needs to use a service provider object.</span></span> <span data-ttu-id="ecb68-114">Через сеанс клиент получает указатель на объект **лпобжект**.</span><span class="sxs-lookup"><span data-stu-id="ecb68-114">Through the session, the client obtains a pointer to the object, **lpObject**.</span></span> <span data-ttu-id="ecb68-115">Таблица vtable отображается сначала в объекте, а затем в закрытых данных и методах.</span><span class="sxs-lookup"><span data-stu-id="ecb68-115">The vtable appears first in the object followed by private data and methods.</span></span> <span data-ttu-id="ecb68-116">Указатель vtable указывает на фактическую виртуальную таблицу (vtable), содержащую указатели на каждую реализацию методов в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="ecb68-116">The vtable pointer points to the actual vtable, which contains pointers to each of the implementations of the methods in the interface.</span></span> 
  
<span data-ttu-id="ecb68-117">**Реализация объекта**</span><span class="sxs-lookup"><span data-stu-id="ecb68-117">**Object implementation**</span></span>
  
<span data-ttu-id="ecb68-118">![Реализация объекта] (media/amapi_42.gif "Реализация объекта")</span><span class="sxs-lookup"><span data-stu-id="ecb68-118">![Object implementation](media/amapi_42.gif "Object implementation")</span></span>
  
<span data-ttu-id="ecb68-119">В приведенном ниже примере кода показано, как поставщик службы C может определить простой объект Status.</span><span class="sxs-lookup"><span data-stu-id="ecb68-119">The following code example shows how a C service provider can define a simple status object.</span></span> <span data-ttu-id="ecb68-120">Первый член является указателем vtable; Остальная часть объекта состоит из элементов данных.</span><span class="sxs-lookup"><span data-stu-id="ecb68-120">The first member is the vtable pointer; the rest of the object is made up of data members.</span></span> 
  
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

<span data-ttu-id="ecb68-121">Так как этот объект является объектом status, таблица vtable содержит указатели на реализации каждого метода в интерфейсе [имапистатус: IMAPIProp](imapistatusimapiprop.md) , а также указатели на реализации каждого метода в базовых интерфейсах — \*\*IUnknown \*\*и **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="ecb68-121">Because this object is a status object, the vtable includes pointers to implementations of each of the methods in the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, as well as pointers to implementations of each of the methods in the base interfaces — **IUnknown** and **IMAPIProp**.</span></span> <span data-ttu-id="ecb68-122">Порядок методов в таблице vtable соответствует заданному порядку, как определено в файле заголовка MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="ecb68-122">The order of methods in the vtable matches the specified order as defined in the Mapidefs.h header file.</span></span>
  
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

<span data-ttu-id="ecb68-123">Клиенты и поставщики услуг, написанные на языке C, косвенно используют объекты с помощью таблицы vtable и добавляют указатель объекта в качестве первого параметра в каждом вызове.</span><span class="sxs-lookup"><span data-stu-id="ecb68-123">Clients and service providers written in C use objects indirectly through the vtable and add an object pointer as the first parameter in every call.</span></span> <span data-ttu-id="ecb68-124">При каждом вызове метода интерфейса MAPI требуется указатель на объект, вызываемый в качестве первого параметра.</span><span class="sxs-lookup"><span data-stu-id="ecb68-124">Every call to a MAPI interface method requires a pointer to the object being called as its first parameter.</span></span> <span data-ttu-id="ecb68-125">C++ определяет для этой цели Специальный указатель, который называется **этим** указателем.</span><span class="sxs-lookup"><span data-stu-id="ecb68-125">C++ defines a special pointer known as the **this** pointer for this purpose.</span></span> <span data-ttu-id="ecb68-126">Компилятор C++ неявно добавляет **этот** указатель в качестве первого параметра для каждого вызова метода.</span><span class="sxs-lookup"><span data-stu-id="ecb68-126">The C++ compiler implicitly adds the **this** pointer as the first parameter to every method call.</span></span> <span data-ttu-id="ecb68-127">В C нет такого указателя; его необходимо добавить явным образом.</span><span class="sxs-lookup"><span data-stu-id="ecb68-127">In C there is no such pointer; it must be explicitly added.</span></span> 
  
<span data-ttu-id="ecb68-128">В приведенном ниже коде показано, как клиент может совершать вызов экземпляра МИСТАТУСОБЖЕКТ:</span><span class="sxs-lookup"><span data-stu-id="ecb68-128">The following code demonstrates how a client can make a call to an instance of MYSTATUSOBJECT:</span></span>
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a><span data-ttu-id="ecb68-129">См. также</span><span class="sxs-lookup"><span data-stu-id="ecb68-129">See also</span></span>

- [<span data-ttu-id="ecb68-130">Реализация объектов MAPI</span><span class="sxs-lookup"><span data-stu-id="ecb68-130">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

