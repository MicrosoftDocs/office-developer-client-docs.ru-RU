---
title: итабледатахржетвиев
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrGetView
api_type:
- COM
ms.assetid: 0e2a47be-497b-4031-87ce-60b2635e25f7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 375a0f1d39b09b7ad453120f20752e00ffda0e15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278717"
---
# <a name="itabledatahrgetview"></a>ITableData::HrGetView

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает табличное представление, возвращая указатель на реализацию [IMAPITable](imapitableiunknown.md) . 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a>Параметры

 _лпссортордерсет_
  
> возврата Указатель на структуру порядка сортировки, в которой описывается порядок сортировки для представления таблицы. Если в параметре _лпссортордерсет_ передается значение null, представление не сортируется. 
    
 _лпфкаллеррелеасе_
  
> возврата Указатель на функцию обратного вызова, основанный на прототипе [каллеррелеасе](callerrelease.md) , который вызывает MAPI при освобождении представления. Если в параметре _лпфкаллеррелеасе_ передается значение null, функция не вызывается в выпуске представления. 
    
 _улкаллердата_
  
> возврата Данные, которые должны быть сохранены с новым представлением и переданы в функцию обратного вызова, на которую указывает _лпфкаллеррелеасе_.
    
 _лппмапитабле_
  
> вышли Указатель на указатель на вновь созданное представление.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Представление было успешно создано.
    
## <a name="remarks"></a>Примечания

Метод **итабледата:: хржетвиев** создает доступное только для чтения представление данных в таблице, отсортированное в порядке, указанном в параметре _лпссортордерсет_ . Курсор помещается в начало первой строки представления. Возвращается реализация интерфейса **IMAPITable** для доступа к представлению. 
  
Поставщики услуг вызывают **хржетвиев** , когда им нужно предоставить клиентский доступ к таблице. **Хржетвиев** создает представление и возвращает указатель **IMAPITable** . Поставщики услуг, в свою очередь, передают указатель клиенту. Когда клиент завершит использование таблицы и вызывает метод [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) , **хржетвиев** вызывает функцию обратного вызова, на которую указывает параметр _лпфкаллеррелеасе_ . 
  
Если поставщик услуг должен возвратить клиенту представление с настроенным набором столбцов или ограничением, поставщик может вызвать метод [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) и [IMAPITable:: restrict](imapitable-restrict.md) , прежде чем разрешить клиентский доступ. 
  
## <a name="see-also"></a>См. также



[CALLERRELEASE](callerrelease.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[SSortOrderSet](ssortorderset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

