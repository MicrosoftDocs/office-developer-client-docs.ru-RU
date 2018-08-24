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
ms.openlocfilehash: 71178f1a531bd381387e0aa7fbacb02d4431a401
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584326"
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

## <a name="parameters"></a>���������

 _ulFlags_
  
> Зарезервировано; должно быть равно нулю.
    
 _lpulCount_
  
> [out] Указатель на число строк в таблице.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Число строк успешно возвращен.
    
MAPI_E_BUSY 
  
> В, не позволяющей операцию извлечения строки count запуск выполняется другой операции. В процессе выполнения операции должны выполнить либо должна быть остановлена.
    
MAPI_E_NO_SUPPORT 
  
> Таблицы не удается определить число строк.
    
MAPI_W_APPROX_COUNT 
  
> Вызов завершился успешно, но число приблизительно, например строк был возвращен из-за количество точное строк не может быть определена возможно из-за ограничений памяти. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. В разделе [Использование макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Замечания

Метод **IMAPITable::GetRowCount** возвращает общее число строк в таблице. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если не удается определить число точное строк таблицы, возвращаемое MAPI_W_APPROX_COUNT и приблизительно, например строку счетчик содержимое параметра _lpulCount_ . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Использование **GetRowCount** , чтобы узнать, сколько строк таблицы содержит перед вызовом метода [IMAPITable::QueryRows](imapitable-queryrows.md) для извлечения данных. При наличии менее 20 строк в таблице, безопасно для вызова **QueryPosition** для получения всей таблицы. При наличии более чем 20 строк в таблице, можно сделать несколько вызовов **QueryPosition** и ограничить число строк, полученные на каждого вызова. 
  
Некоторые таблицы не поддерживают **GetRowCount** и вернуть MAPI_E_NO_SUPPORT. Если **GetRowCount** не поддерживается, вместо возможно для вызова [IMAPITable::QueryPosition](imapitable-queryposition.md). С результатами из **QueryPosition**можно определить связь между текущей строки и последней строки. 
  
При **GetRowCount** возвращает MAPI_E_BUSY, так как они временно не удалось получить число строк, вызовите метод [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) . При возврате **WaitForCompletion** повторите вызов **GetRowCount**. Другим способом для определения, является ли в процессе выполнения асинхронной операции является можно вызвать метод [IMAPITable::GetStatus](imapitable-getstatus.md) , а также просматривать содержимое параметра _lpulTableState_ . 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyFolderContents  <br/> |Mfcmapi (en) использует метод **IMAPITable::GetRowCount** , чтобы определить, сколько строк в таблице источника, можно выделить память для выполнения копирования.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

