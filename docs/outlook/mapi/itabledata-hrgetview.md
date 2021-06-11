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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает представление таблицы, возвращая указатель в [реализацию IMAPITable.](imapitableiunknown.md) 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a>Parameters

 _lpSSortOrderSet_
  
> [in] Указатель на структуру порядка сортировки, которая описывает порядок сортировки для представления таблицы. Если NULL передается в  _параметре lpSSortOrderSet,_ представление не сортироваться. 
    
 _lpfCallerRelease_
  
> [in] Указатель на функцию вызова на основе прототипа [CALLERRELEASE,](callerrelease.md) вызываемого MAPI при выпуске представления. Если NULL передается в  _параметре lpfCallerRelease,_ при выпуске представления функция не называется. 
    
 _ulCallerData_
  
> [in] Данные, которые необходимо сохранить с помощью нового представления и передать функции вызова, на которые указывает _lpfCallerRelease._
    
 _lppMAPITable_
  
> [вышел] Указатель на указатель на вновь созданное представление.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Представление было успешно создано.
    
## <a name="remarks"></a>Примечания

Метод **ITableData::HrGetView** создает представление данных в таблице только для чтения, отсортировали в порядке, указываемом параметром _lpSSortOrderSet._ Курсор помещается в начале первой строки в представлении. Возвращается реализация интерфейса **IMAPITable** для доступа к представлению. 
  
Поставщики услуг **звонят в HrGetView,** когда им необходимо предоставить клиенту доступ к таблице. **HrGetView** создает представление и возвращает **указатель IMAPITable.** Поставщики услуг в свою очередь передают указатель клиенту. Когда клиент заканчивает использовать таблицу и вызывает метод [IUnknown::Release,](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) **HrGetView** вызывает функцию вызова, отмеченную параметром _lpfCallerRelease._ 
  
Если поставщику услуг необходимо вернуть клиенту представление с настраиваемым набором столбцов или ограничением, перед разрешением клиентского доступа поставщик может вызвать [IMAPITable::SetColumns](imapitable-setcolumns.md) и [IMAPITable::Restrict.](imapitable-restrict.md) 
  
## <a name="see-also"></a>См. также



[CALLERRELEASE](callerrelease.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[SSortOrderSet](ssortorderset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

