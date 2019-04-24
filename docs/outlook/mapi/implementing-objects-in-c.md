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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310193"
---
# <a name="implementing-objects-in-c"></a>Реализация объектов в C

**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения и поставщики услуг, написанные на языке C, определяют объекты MAPI, создавая структуру данных и массив упорядоченных указателей функций, которые называются таблицей виртуальной функции или виртуальной таблицей. Указатель на таблицу vtable должен быть первым членом структуры данных.
  
В самой таблице vtable существует один указатель для каждого метода в каждом интерфейсе, поддерживаемом объектом. Порядок указателей должен соответствовать порядку методов в спецификации интерфейса, опубликованной в файле заголовка MAPIDEFS. h. Для каждого указателя функции в таблице vtable задается адрес фактической реализации метода. В C++ компилятор автоматически настраивает виртуальную таблицу (vtable). В C это не так. 
  
На следующем рисунке показано, как это работает. Поле в дальнем левом углу представляет клиент, который должен использовать объект поставщика услуг. Через сеанс клиент получает указатель на объект **лпобжект**. Таблица vtable отображается сначала в объекте, а затем в закрытых данных и методах. Указатель vtable указывает на фактическую виртуальную таблицу (vtable), содержащую указатели на каждую реализацию методов в интерфейсе. 
  
**Реализация объекта**
  
![Реализация объекта] (media/amapi_42.gif "Реализация объекта")
  
В приведенном ниже примере кода показано, как поставщик службы C может определить простой объект Status. Первый член является указателем vtable; Остальная часть объекта состоит из элементов данных. 
  
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

Так как этот объект является объектом status, таблица vtable содержит указатели на реализации каждого метода в интерфейсе [имапистатус: IMAPIProp](imapistatusimapiprop.md) , а также указатели на реализации каждого метода в базовых интерфейсах — **IUnknown **и **IMAPIProp**. Порядок методов в таблице vtable соответствует заданному порядку, как определено в файле заголовка MAPIDEFS. h.
  
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

Клиенты и поставщики услуг, написанные на языке C, косвенно используют объекты с помощью таблицы vtable и добавляют указатель объекта в качестве первого параметра в каждом вызове. При каждом вызове метода интерфейса MAPI требуется указатель на объект, вызываемый в качестве первого параметра. C++ определяет для этой цели Специальный указатель, который называется **этим** указателем. Компилятор C++ неявно добавляет **этот** указатель в качестве первого параметра для каждого вызова метода. В C нет такого указателя; его необходимо добавить явным образом. 
  
В приведенном ниже коде показано, как клиент может совершать вызов экземпляра МИСТАТУСОБЖЕКТ:
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a>См. также

- [Реализация объектов MAPI](implementing-mapi-objects.md)

