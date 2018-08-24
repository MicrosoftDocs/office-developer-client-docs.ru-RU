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
ms.openlocfilehash: 0eb0374788da629c4c28eff2fce93536cf65a4ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582989"
---
# <a name="itabledatahrgetview"></a>ITableData::HrGetView

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создание нового представления таблицы, возвращает указатель на реализацию [IMAPITable](imapitableiunknown.md) . 
  
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
  
> [in] Указатель на структуру порядок сортировки, который описывает порядок сортировки в табличном представлении. Если значение NULL передается в параметре _lpSSortOrderSet_ , не сортировка. 
    
 _lpfCallerRelease_
  
> [in] Указатель на функцию обратного вызова, на основании прототип [CALLERRELEASE](callerrelease.md) , MAPI при освобождает представления. Если с помощью параметра _lpfCallerRelease_ передано значение NULL, функция не вызывается в выпуске представления. 
    
 _ulCallerData_
  
> [in] Данных, который должен быть сохранен с помощью нового представления и передается в функцию обратного вызова, на который указывает _lpfCallerRelease_.
    
 _lppMAPITable_
  
> [out] Указатель на указатель на только что созданный представления.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Представление успешно создан.
    
## <a name="remarks"></a>Замечания

Метод **ITableData::HrGetView** создает представления только для чтения данных в таблице, в порядке, на который указывает параметр _lpSSortOrderSet_ . Курсор в начале первой строки в представлении. Реализация интерфейса **IMAPITable** для доступа к представлении возвращается. 
  
Поставщиков услуг вызов **HrGetView** , когда требуется предоставить клиентского доступа в таблицу. **HrGetView** создает представление и возвращает указатель **IMAPITable** . В свою очередь, поставщиков услуг передайте указатель мыши на клиенте. Когда клиенту по завершении работы с помощью таблицы и вызывает метод [функции IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) , **HrGetView** вызывает функцию обратного вызова, на который указывает параметр _lpfCallerRelease_ . 
  
Если поставщик службы необходимо возвратить клиенту представление, набор настраиваемых столбцов или ограничение, поставщик может вызвать методы [IMAPITable::SetColumns](imapitable-setcolumns.md) и [IMAPITable::Restrict](imapitable-restrict.md) представления перед тем как разрешить клиентского доступа. 
  
## <a name="see-also"></a>См. также



[CALLERRELEASE](callerrelease.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[SSortOrderSet](ssortorderset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

