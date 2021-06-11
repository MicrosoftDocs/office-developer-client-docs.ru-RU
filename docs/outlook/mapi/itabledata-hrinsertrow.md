---
title: ITableDataHrInsertRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrInsertRow
api_type:
- COM
ms.assetid: e5ae37ea-81a5-49c7-9ad0-0bfac518426c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2709ac612fc9e2edaa57b280d52c0a5229ee9978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435441"
---
# <a name="itabledatahrinsertrow"></a>ITableData::HrInsertRow

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вставляет строку таблицы. 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Parameters

 _uliRow_
  
> [in] Последовательное число строк, представляю которое представляет определенную строку. Новая строка будет размещена после строки, на которую указывает номер. Параметр  _uliRow_ может содержит номера строк от 0 до n, где n — это общее число строк в таблице. Передача n  _в uliRow_ придает строку в конец таблицы. 
    
 _lpSRow_
  
> [in] Указатель на [структуру SRow,](srow.md) которая описывает строку, которую необходимо вставить. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Строка успешно вставлена.
    
MAPI_E_INVALID_PARAMETER 
  
> Строка, которая имеет то же значение для столбца индекса, что и строка, которую необходимо вставить, уже существует в таблице.
    
## <a name="remarks"></a>Примечания

Метод **ITableData::HrInsertRow** вставляет строку в таблицу в определенной позиции. Новая строка вставляется после строки, которая находится в позиции, указанной параметром _uliRow._ 
  
Если  _uliRow_ задан на количество строк в таблице, новая строка примыкает к концу таблицы. 
  
Свойство, которое выступает в качестве столбца индекса для таблицы, должно быть включено в член **lpProps** структуры [SRow,](srow.md) на который указывает параметр _lpSRow._ Это свойство индекса, **обычно PR_INSTANCE_KEY** [(PidTagInstanceKey),](pidtaginstancekey-canonical-property.md)используется для уникального определения строки для будущих задач обслуживания.
  
Столбцы свойств в структуре **SRow** не должны быть в том же порядке, что и столбцы свойств в таблице. 
  
После вставки строки уведомления отправляются всем клиентам или поставщикам услуг, которые имеют представление таблицы и вызвали метод [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений. Уведомление не отправляется, если вставленная строка не включена в представление из-за ограничения. 
  
## <a name="see-also"></a>См. также



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

