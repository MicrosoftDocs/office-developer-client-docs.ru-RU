---
title: Внедрение объектов в C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 24fc4d78-726d-40ff-bad2-25dc298bd51a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d07d756abded137d3268daf7dd0998f0c953cb1d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563949"
---
# <a name="implementing-objects-in-c"></a>Внедрение объектов в C

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения и поставщиков услуг, написанных на языке C определяется путем создания структуры данных и массив указателей упорядоченном функций, известных как таблицы виртуальной функции или vtable объектов MAPI. Указатель vtable должен быть первый элемент структуры данных.
  
В vtable самого существует один указатель для каждого метода каждого интерфейса поддерживается объектом. Порядок указатели должны соответствовать порядок методов в спецификации интерфейса, опубликованной в файл заголовка Mapidefs.h. Каждый указатель на функцию в таблице vtable задано значение адрес фактическую реализацию метода. В C++ компилятора автоматически выполняет настройку vtable. В C нет. 
  
На следующем рисунке показана, как это работает. Поле слева представляет клиента, которую необходимо использовать объект поставщика службы. Через сеанс клиент получает указатель на объект **lpObject**. Vtable отображается первым в объекте, а затем личных данных и методы. Указатель vtable указывает на фактический vtable, который содержит указатели на каждой реализации методов в интерфейсе. 
  
**Реализация объекта**
  
![Реализация объекта] (media/amapi_42.gif "Реализация объекта")
  
В следующем примере кода показано, как поставщик службы C можно определить простой состояние объекта. Первый элемент является указателя vtable; Остальная часть объекта состоит из элементов данных. 
  
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

Поскольку этот объект является объектом состояния, vtable содержит указатели на реализацию каждого из методов в [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) интерфейс, а также указатели на реализацию каждого из методов в базовые интерфейсы — **IUnknown **и **IMAPIProp**. Порядок методов в таблице vtable совпадает с указанным порядком, определенных в файле заголовка Mapidefs.h.
  
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

Клиенты и поставщиков услуг, написанных на языке C используйте объекты косвенно через vtable и добавьте указателя на объект в качестве первого параметра в каждого вызова. Каждый вызов метода интерфейса MAPI требуется указатель на объект, вызываемый в качестве первого параметра. C++ определяет специальные указатель, известных как **Этот** указатель для этой цели. Компилятор C++ неявно добавляет **Этот** указатель мыши в качестве первого параметра для каждого вызова метода. В C — нет такого указатель; она должна быть явно добавлена. 
  
В следующем коде показано, как клиент может позвонить в экземпляр MYSTATUSOBJECT:
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a>См. также

- [Реализация объектов MAPI](implementing-mapi-objects.md)

