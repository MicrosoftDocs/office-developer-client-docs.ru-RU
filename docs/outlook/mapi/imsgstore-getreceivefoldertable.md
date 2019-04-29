---
title: Имсгсторежетрецеивефолдертабле
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
ms.openlocfilehash: 303c2ef855d5cfc1d6614bda92b46c2da97717c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421356"
---
# <a name="imsgstoregetreceivefoldertable"></a>IMsgStore::GetReceiveFolderTable

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к таблице получения папки, в которой содержатся сведения обо всех папках получения для хранилища сообщений.
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Битовая маска флагов, определяющих доступ к таблицам. Можно задать следующие флаги:
    
МАПИ_ДЕФЕРРЕД_ЕРРОРС 
  
> Позволяет **жетрецеивефолдертабле** успешно возвращать результат, возможно, прежде чем таблица будет полностью доступна вызывающему абоненту. Если таблица недоступна, то выполнение последующих вызовов таблицы может вызвать ошибку. 
    
MAPI_UNICODE 
  
> Возвращаемые строки представлены в формате Юникод. Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.
    
 _Лпптабле_
  
> вышли Указатель на указатель на таблицу "Получение папки".
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица получения папки успешно возвращена.
    
## <a name="remarks"></a>Примечания

Метод **IMsgStore:: жетрецеивефолдертабле** предоставляет доступ к таблице, в которой показаны параметры свойств для всех папок получения хранилища сообщений. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Список обязательных столбцов в таблице получения папок представлен в статье [получение таблиц](receive-folder-tables.md)с папками. 
  
Реализуйте таблицы приема-передачи для поддержки настройки ограничений свойств для свойства **пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Это позволяет легко получить доступ к определенным папкам получения.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Установка флага МАПИ_УНИКОДЕ в параметре _ulFlags_ влияет на формат столбцов, возвращаемых методами [IMAPITable:: куериколумнс](imapitable-querycolumns.md) и [IMAPITable:: QueryRows](imapitable-queryrows.md) . Этот флаг также контролирует типы свойств в порядке сортировки, возвращаемом методом [IMAPITable:: куерисортордер](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мсгсторедлг. cpp  <br/> |Кмсгсторедлг:: Ондисплайрецеивефолдертабле  <br/> |MFCMAPI использует метод **IMsgStore:: жетрецеивефолдертабле** , чтобы получить отображаемую таблицу с папкой получения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

