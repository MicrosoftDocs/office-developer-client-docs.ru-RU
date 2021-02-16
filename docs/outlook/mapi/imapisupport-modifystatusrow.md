---
title: IMAPISupportModifyStatusRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyStatusRow
api_type:
- COM
ms.assetid: a304ca8f-e404-4535-be76-0b673f2061a0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8c76e6059670e782ea6530ec8e94f77abfe5b9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417163"
---
# <a name="imapisupportmodifystatusrow"></a>IMAPISupport::ModifyStatusRow

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Изменяет таблицу состояния, добавляя новую строку или изменяя существующую строку.
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _cValues_
  
> [in] Количество свойств, которые необходимо включить в новую или измененную строку таблицы состояния. 
    
 _lpColumnVals_
  
> [in] Указатель на массив значений свойств, которые описывают свойства, которые необходимо включить в качестве столбцов в новую или измененную строку таблицы состояния.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет обработкой сведений, определяемых строкой таблицы состояния. Можно установить следующий флаг:
    
STATUSROW_UPDATE 
  
> Направляет MAPI для объединения свойств, включенных в массив, на который указывает  _lpColumnVals,_ с существующей строкой таблицы состояния, а не в новой строке. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица состояния успешно обновлена.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::ModifyStatusRow** реализован для всех объектов поддержки поставщика услуг. Поставщики услуг **звонят modifyStatusRow** во время логотипа, чтобы добавить строку в таблицу состояния, а в другое время во время сеанса обновить строку. **ModifyStatusRow** предоставляет MAPI информацию, необходимую для построения таблицы состояния. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Установите флаг STATUSROW_UPDATE при вызове **ModifyStatusRow,** чтобы внести изменения в свойства существующей строки таблицы состояния. Это сообщает MAPI о том, что в  _параметре lpColumnVals_ передаются только издаваемые столбцы. 
  
Клиенты могут использовать сведения в таблице состояния для доступа к объекту состояния. 
  
Полный список столбцов, которые необходимо включить в строку таблицы состояния, см. в [таблицах состояния.](status-tables.md)
  
## <a name="see-also"></a>См. также



[IMAPISupport: IUnknown](imapisupportiunknown.md)

