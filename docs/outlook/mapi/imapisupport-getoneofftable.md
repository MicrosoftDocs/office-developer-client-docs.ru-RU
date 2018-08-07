---
title: IMAPISupportGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetOneOffTable
api_type:
- COM
ms.assetid: 6800fd3a-aa43-45fe-9cc2-102d0ef43edf
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 51cd838164e3de28ab33d6ab8a08a021360f3183
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809114"
---
# <a name="imapisupportgetoneofftable"></a>IMAPISupport::GetOneOffTable

  
  
**Относится к**: Outlook 
  
Возвращает указатель на таблице одноразовых MAPI (список шаблонов, что все в адресной книге поставщиков поддержка создания новых получателей).
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип string столбцов. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Столбцы строку, в формате Юникод. Если флаг MAPI_UNICODE не установлен, столбцы строку, в формате ANSI.
    
 _lppTable_
  
> [out] Указатель на указатель на одноразовых таблицы.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> В таблице одноразовых был успешно извлечен.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::GetOneOffTable** реализуется для объектов поддержки поставщик адресной книги. Поставщиками адресной книги вызовите **GetOneOffTable** , чтобы получить полный список шаблонов для создания новых получателей. В этой таблице включает в себя шаблоны, которые поддерживают поставщиками адресных книг, которые включены в сеансе, а также шаблоны, которые поддерживает MAPI. 
  
Только что созданный получателей можно использовать адрес сообщения или можно добавить в контейнер адресной книги.
  
Список свойств, которые составляют обязательный столбец, задайте в одноразовых таблицах см в [Одноразовых таблиц](one-off-tables.md).
  
Установка флага MAPI_UNICODE с помощью параметра _ulFlags_ влияет на формат столбцов, возвращаемых с помощью методов [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows](imapitable-queryrows.md) . Этот флаг также определяет типы свойств в порядке сортировки, возвращенный методом [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Зарегистрированные для получения уведомлений об изменениях в этой таблице одноразовых также получат оповещений об изменениях в одноразовых таблицы других поставщиков. На основе этих уведомлений, может поддерживать новые типы адресов, которые добавляются во время текущего сеанса.
  
## <a name="see-also"></a>См. также



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPISupport::NewEntry](imapisupport-newentry.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[Каноническое свойство PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Одноразовые таблицы](one-off-tables.md)

