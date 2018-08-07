---
title: IMAPISessionGetMsgStoresTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ba540b0fd3371b3e12be9eeeb102a9bd9d7e8d22
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809053"
---
# <a name="imapisessiongetmsgstorestable"></a>IMAPISession::GetMsgStoresTable

  
  
**Относится к**: Outlook 
  
Предоставляет доступ к таблице хранилища сообщений, который содержит сведения о всех хранилищ сообщений в профиле сеанса.
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, который определяет формат для столбцов, которые являются строками символов. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Столбцы строку, в формате Юникод. Если флаг MAPI_UNICODE не установлен, столбцы строку, в формате ANSI.
    
 _lppTable_
  
> [out] Указатель на указатель в таблице хранилища сообщений.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Таблица успешно возвращен.
    
MAPI_E_BAD_CHARWIDTH 
  
> Был установлен флажок MAPI_UNICODE и сеанса не поддерживает Юникод.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISession::GetMsgStoresTable** получает указатель в таблице хранилища сообщений, таблицы задаваемые с помощью интерфейса MAPI, содержащий сведения о каждом открыть сообщение хранилище в профиле. 
  
Полный список обязательные и дополнительные столбцы в сообщении хранилища в таблице, просматривать [Таблицы хранения сообщений](message-store-tables.md). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Так как MAPI обновляет таблицу хранилища сообщений во время сеанса при каждом возникновении изменений, вызовите метод **уведомлений** таблицы хранилища сообщений для регистрации уведомлений об этих изменений. Возможные изменения включают добавление новых хранилищ сообщений, удаления существующих хранит и изменяется на хранилище по умолчанию. 
  
Установка флага MAPI_UNICODE с помощью параметра _ulFlags_ влияет на формат столбцов, возвращаемых с помощью методов [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows](imapitable-queryrows.md) . Этот флаг также определяет типы свойств в порядке сортировки, возвращенный методом [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenMessageStoreTable  <br/> |Mfcmapi (en) использует метод **IMAPISession::GetMsgStoresTable** для получения таблицы хранилища сообщений, чтобы он отображался в диалоговом окне основной mfcmapi (en).  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Таблицы хранилища сообщений](message-store-tables.md)

