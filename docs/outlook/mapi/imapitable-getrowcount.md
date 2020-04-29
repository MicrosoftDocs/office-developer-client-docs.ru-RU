---
title: имапитаблежетровкаунт
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetRowCount
api_type:
- COM
ms.assetid: 44a12c92-7462-4acf-9520-5d4c2d7f1d47
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b13bf3bdd8392efc42ad189e48dffad8636f0708
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425605"
---
# <a name="imapitablegetrowcount"></a>IMAPITable::GetRowCount

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает общее количество строк в таблице. 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> Резервирования должно быть равно нулю.
    
 _лпулкаунт_
  
> вышли Указатель на число строк в таблице.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Успешно возвращено значение счетчика строк.
    
MAPI_E_BUSY 
  
> Выполняется другая операция, которая не позволяет запустить операцию получения количества строк. Выполнение выполняемой операции должно быть разрешено или остановлено.
    
MAPI_E_NO_SUPPORT 
  
> В таблице невозможно вычислить количество строк.
    
MAPI_W_APPROX_COUNT 
  
> Вызов выполнен успешно, но приблизительное число строк было возвращено из-за того, что не удалось определить точное количество строк, возможно, из-за ограничений памяти. Чтобы проверить это предупреждение, используйте макрос **HR_FAILED** . Просмотр и [Использование макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::** GetRows получает общее количество строк в таблице. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если не удается определить точное количество строк таблицы, возвращается MAPI_W_APPROX_COUNT и приблизительное число строк в содержимом параметра _лпулкаунт_ . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Используйте функцию GetRows, чтобы **узнать, сколько** строк содержит таблица, прежде чем совершать вызов метод [IMAPITable:: QueryRows](imapitable-queryrows.md) для получения данных. Если в таблице менее двадцати строк, для получения всей таблицы можно безопасно вызвать **куерипоситион** . Если таблица содержит более двадцати строк, рекомендуется выполнить несколько вызовов **куерипоситион** и ограничить количество строк, извлекаемых при каждом вызове. 
  
В некоторых таблицах не поддерживаются значения **ROWCOUNT** и Return MAPI_E_NO_SUPPORT. Если **метод** куерипоситион не поддерживается, то альтернативным вариантом может быть вызов [IMAPITable::](imapitable-queryposition.md). С помощью результатов из **куерипоситион**можно определить связь между текущей строкой и последней строкой. 
  
Если **метод** ваитфоркомплетион возвращает MAPI_E_BUSY, так как он временно не может получить количество строк, вызовите метод [IMAPITable::](imapitable-waitforcompletion.md) . Когда возвращается Ваитфоркомплетион, повторите вызов метода **WaitForCompletion** . **GetRowCount** Другой способ определить, выполняется ли асинхронная операция, — вызвать метод [IMAPITable::-Status](imapitable-getstatus.md) и проверить содержимое параметра _лпултаблестате_ . 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мапифунктионс. cpp  <br/> |копифолдерконтентс  <br/> |MFCMAPI использует метод **IMAPITable::** , чтобы определить количество строк в исходной таблице, чтобы можно было выделить память для выполнения копирования.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

