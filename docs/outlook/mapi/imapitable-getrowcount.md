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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает общее количество строк в таблице. 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> Зарезервировано; должно быть нулевой.
    
 _lpulCount_
  
> [вышел] Указатель на количество строк в таблице.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Количество строк было успешно возвращено.
    
MAPI_E_BUSY 
  
> В настоящее время продолжается еще одна операция, которая не позволяет начать операцию по ирисовке подсчета строк. Либо операция должна быть разрешена к завершению, либо она должна быть остановлена.
    
MAPI_E_NO_SUPPORT 
  
> Таблица не может рассчитать количество строк.
    
MAPI_W_APPROX_COUNT 
  
> Вызов удался, но было возвращено приблизительное число строк, так как точное число строк не удалось определить из-за ограничений памяти. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. См. в руб. Использование [макроса для обработки ошибок.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::GetRowCount** извлекает общее количество строк в таблице. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если вы не можете определить точное количество строк в таблице, MAPI_W_APPROX_COUNT и приблизительное число строк в содержимом _параметра lpulCount._ 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы получить данные, используйте **GetRowCount,** чтобы узнать, сколько строк занимает таблица перед вызовом метода [IMAPITable::QueryRows.](imapitable-queryrows.md) Если в таблице менее 20 строк, можно с уверенностью вызвать **QueryPosition,** чтобы получить всю таблицу. Если в таблице более 20 строк, следует сделать несколько вызовов **в QueryPosition** и ограничить количество строк, полученных в каждом вызове. 
  
Некоторые таблицы не поддерживают **GetRowCount** и возвращают MAPI_E_NO_SUPPORT. Если **GetRowCount** не поддерживается, можно вызвать [IMAPITable::QueryPosition.](imapitable-queryposition.md) С помощью результатов **queryPosition** можно определить связь между текущей строкой и последней строкой. 
  
Когда **GetRowCount** возвращает MAPI_E_BUSY, так как она временно не может получить количество строк, позвоните по методу [IMAPITable::WaitForCompletion.](imapitable-waitforcompletion.md) Когда **waitForCompletion** возвращается, повторно вызов **GetRowCount**. Другой способ определить, проводится ли асинхронная операция, — вызвать метод [IMAPITable::GetStatus](imapitable-getstatus.md) и проверить содержимое _параметра lpulTableState._ 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyFolderContents  <br/> |MFCMAPI использует метод **IMAPITable::GetRowCount,** чтобы определить, сколько строк в исходных таблицах, чтобы можно было выделить память для выполнения копии.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

