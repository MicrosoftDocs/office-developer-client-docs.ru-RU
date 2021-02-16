---
title: IMAPITableGetRowCount
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
  
Возвращает общее число строк в таблице. 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> Зарезервировано; должно быть нулем.
    
 _lpulCount_
  
> [out] Указатель на количество строк в таблице.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Количество строк успешно возвращено.
    
MAPI_E_BUSY 
  
> В настоящее время идет другая операция, которая препятствует запуску операции ирисовки подсчета строк. Либо операция должна быть завершена, либо она должна быть остановлена.
    
MAPI_E_NO_SUPPORT 
  
> В таблице не удается вычислить количество строк.
    
MAPI_W_APPROX_COUNT 
  
> Вызов был успешным, но было возвращено приблизительное количество строк, так как точное количество строк не удалось определить, возможно, из-за ограничений памяти. Чтобы проверить это предупреждение, используйте **макрос** HR_FAILED. См. ["Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::GetRowCount** извлекает общее количество строк в таблице. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если точное количество строк таблицы определить не удается, MAPI_W_APPROX_COUNT и приблизительное количество строк в содержимом параметра _lpulCount._ 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Используйте **Метод GetRowCount,** чтобы узнать, сколько строк содержит таблица перед вызовом метода [IMAPITable::QueryRows](imapitable-queryrows.md) для получения данных. Если в таблице менее 20 строк, можно вызвать **QueryPosition,** чтобы получить всю таблицу. Если в таблице более 20 строк, рассмотрите возможность выполнения нескольких вызовов **QueryPosition** и ограничить число строк, полученных в каждом вызове. 
  
Некоторые таблицы не поддерживают **GetRowCount** и возвращают MAPI_E_NO_SUPPORT. Если **GetRowCount** не поддерживается, можно вызвать [IMAPITable::QueryPosition.](imapitable-queryposition.md) С помощью результатов **из QueryPosition** можно определить отношение между текущей строкой и последней строкой. 
  
Когда **Метод GetRowCount** MAPI_E_BUSY, так как он временно не может получить количество строк, вызовите метод [IMAPITable::WaitForCompletion.](imapitable-waitforcompletion.md) Когда **waitForCompletion** возвращается, повторить вызов **GetRowCount.** Еще один способ определить, проводится ли асинхронная операция, — вызвать метод [IMAPITable::GetStatus](imapitable-getstatus.md) и проверить содержимое параметра _lpulTableState._ 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyFolderContents  <br/> |MFCMAPI использует метод **IMAPITable::GetRowCount,** чтобы определить количество строк в таблице источника, чтобы можно было выделить память для выполнения копирования.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

