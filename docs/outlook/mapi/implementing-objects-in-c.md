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
# <a name="implementing-objects-in-c"></a>Реализация объектов в C

**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения и поставщики услуг, написанные на C, определяют объекты MAPI путем создания структуры данных и массива упорядоченных указателей функций, известных как таблица виртуальных функций или виртуальная таблица. Указатель на vtable должен быть первым членом структуры данных.
  
В самой vtable есть один указатель для каждого метода в каждом интерфейсе, поддерживаемом объектом. Порядок указателей должен следовать порядку методов в спецификации интерфейса, опубликованной в файле заговорки Mapidefs.h. Каждому указателю функции в vtable устанавливается адрес фактической реализации метода. В C++ компилятор автоматически настраивает vtable. В C это не так. 
  
На следующем рисунке показано, как это работает. Поле слева представляет клиент, который должен использовать объект поставщика услуг. Через сеанс клиент получает указатель на объект **lpObject.** В первую очередь в объекте отображается vtable, а затем личные данные и методы. Указатель на vtable указывает на фактическую vtable, которая содержит указатели на каждую реализацию методов в интерфейсе. 
  
**Реализация объекта**
  
![Реализация объекта реализации](media/amapi_42.gif "объекта")
  
В следующем примере кода показано, как поставщик службы C может определить простой объект состояния. Первый член — это указатель на vtable; Остальная часть объекта состоит из членов данных. 
  
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

Поскольку этот объект является объектом состояния, vtable включает указатели на реализации каждого из методов в интерфейсе [IMAPIStatus : IMAPIProp,](imapistatusimapiprop.md) а также указатели на реализации каждого из методов в базовых интерфейсах **— IUnknown** и **IMAPIProp**. Порядок методов в vtable соответствует указанному порядку, определенному в файле загона Mapidefs.h.
  
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

Клиенты и поставщики услуг, написанные на C, используют объекты косвенно через vtable и добавляют указатель объекта в качестве первого параметра в каждом вызове. Для каждого вызова метода интерфейса MAPI требуется указатель на объект, который будет вызываться в качестве первого параметра. C++ определяет специальный указатель, известный как **этот** указатель для этой цели. Компилятор C++ неявно добавляет этот указатель в качестве первого параметра для каждого вызова метода.  В C нет такого указателя; его необходимо явно добавить. 
  
В следующем коде показано, как клиент может вызывать экземпляр MYSTATUSOBJECT:
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a>См. также

- [Реализация объектов MAPI](implementing-mapi-objects.md)

