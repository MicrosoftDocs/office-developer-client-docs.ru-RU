---
title: ITableDataHrGetView
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
  
Создает представление таблицы, возвращая указатель на [реализацию IMAPITable.](imapitableiunknown.md) 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a>Параметры

 _lpSSortOrderSet_
  
> [in] Указатель на структуру порядка сортировки, которая описывает порядок сортировки для представления таблицы. Если в параметре  _lpSSortOrderSet_ передается NULL, представление не сортироваться. 
    
 _lpfCallerRelease_
  
> [in] Указатель на функцию вызова на основе прототипа [CALLERRELEASE,](callerrelease.md) вызываемого MAPI при выпуске представления. Если в параметре  _lpfCallerRelease_ передается NULL, функция не будет вызвана при выпуске представления. 
    
 _ulCallerData_
  
> [in] Данные, которые должны быть сохранены в новом представлении и переданы функции вызова, на которую указывает _lpfCallerRelease._
    
 _lppMAPITable_
  
> [out] Указатель на указатель на созданное представление.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Представление успешно создано.
    
## <a name="remarks"></a>Примечания

Метод **ITableData::HrGetView** создает представление данных в таблице только для чтения, отсортировали в порядке, на который указывает параметр _lpSSortOrderSet._ Курсор помещается в начале первой строки представления. Возвращается **реализация интерфейса IMAPITable** для доступа к представлению. 
  
Поставщики услуг **звонят HrGetView,** когда им нужно предоставить клиенту доступ к таблице. **HrGetView** создает представление и возвращает **указатель IMAPITable.** Поставщики услуг, в свою очередь, передают указатель клиенту. Когда клиент завершает работу с таблицей и вызывает метод [IUnknown::Release,](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) **HrGetView** вызывает функцию вызова, на которая указывает параметр _lpfCallerRelease._ 
  
Если поставщику услуг необходимо вернуть клиенту представление с настроенным набором столбцов или ограничением, поставщик может вызвать методы [IMAPITable::SetColumns](imapitable-setcolumns.md) и [IMAPITable::Restrict,](imapitable-restrict.md) прежде чем разрешить клиентский доступ. 
  
## <a name="see-also"></a>См. также



[CALLERRELEASE](callerrelease.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[SSortOrderSet](ssortorderset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

