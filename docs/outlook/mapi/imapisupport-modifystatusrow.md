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
ms.openlocfilehash: 06a5c9de5c0ce4c0f936791086a731a55510a124
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592145"
---
# <a name="imapisupportmodifystatusrow"></a>IMAPISupport::ModifyStatusRow

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Изменяет состояние таблицы путем добавления строки или изменение существующей строки.
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _cValues_
  
> [in] Число свойств, включаемых в строку новое или измененное состояние таблицы. 
    
 _lpColumnVals_
  
> [in] Указатель на массив значений свойств, которые описывают свойства в качестве столбцов в строке состояния новые или измененные таблицы.
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее порядок обработки информации, которая определяет строку в таблице состояния. Можно задать следующий флаг:
    
STATUSROW_UPDATE 
  
> Направляет MAPI для объединения свойств, включенных в массиве, на который указывает _lpColumnVals_ с существующей строки в таблице состояния, а не в новую строку. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> В таблице состояния обновлен успешно.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::ModifyStatusRow** применяется для всех объектов поддержки поставщика службы. Поставщики услуг вызвать **ModifyStatusRow** во время входа в систему для добавления строки в таблице состояния и в других случаях во время сеанса для обновления строки. **ModifyStatusRow** предоставляет сведения, необходимые для создания таблицы состояния MAPI. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Установите флаг STATUSROW_UPDATE при вызове **ModifyStatusRow** вносить изменения свойств в вашей существующей строки в таблице состояния. Это информирует MAPI передачи только изменяемый столбцы с помощью параметра _lpColumnVals_ . 
  
Клиенты могут использовать сведения в таблице состояния для доступа к объекту ваше состояние. 
  
Полный список столбцов, которые необходимо включить в ваше состояние строки в таблице [Состояния](status-tables.md)см.
  
## <a name="see-also"></a>См. также



[IMAPISupport: IUnknown](imapisupportiunknown.md)

