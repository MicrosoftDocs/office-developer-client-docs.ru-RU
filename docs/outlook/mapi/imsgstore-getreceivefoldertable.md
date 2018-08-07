---
title: IMsgStoreGetReceiveFolderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolderTable
api_type:
- COM
ms.assetid: d115ab58-07d2-4b49-8e08-2881c2924102
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8146b5c2b9c9fb5429a9c1d46bca687c32bcf3dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809395"
---
# <a name="imsgstoregetreceivefoldertable"></a>IMsgStore::GetReceiveFolderTable

  
  
**Относится к**: Outlook 
  
Предоставляет доступ к таблице папок получения таблицу, содержащую сведения обо всех получения папки для хранения сообщений.
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, таблицы, что элементы управления доступом. Можно задать следующие флажки:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **GetReceiveFolderTable** для возврата успешно, возможно перед таблице доступными для вызывающего абонента. Если в таблице полностью недоступен, вызов последующие таблицы может вызвать ошибку. 
    
MAPI_UNICODE 
  
> В формате Юникод, возвращенных строк. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
 _lppTable_
  
> [out] Указатель на указатель в таблице папку получения.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> В таблице папку получения успешно возвращен.
    
## <a name="remarks"></a>Замечания

Метод **IMsgStore::GetReceiveFolderTable** предоставляет доступ к таблице, которая отображает значения свойств для всех хранилища сообщений получают папок. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Список обязательные столбцы в таблице папку получения см [получают папки](receive-folder-tables.md). 
  
Реализация вашей получать таблиц папки для поддержки задание ограничений свойств на свойство **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). В этом позволяет легко получить доступ к конкретным получают папок.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Установка флага MAPI_UNICODE с помощью параметра _ulFlags_ влияет на формат столбцов, возвращаемых с помощью методов [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows](imapitable-queryrows.md) . Этот флаг также определяет типы свойств в порядке сортировки, возвращенный методом [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDisplayReceiveFolderTable  <br/> |Mfcmapi (en) использует метод **IMsgStore::GetReceiveFolderTable** для получения таблицы получения папки для отображения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

