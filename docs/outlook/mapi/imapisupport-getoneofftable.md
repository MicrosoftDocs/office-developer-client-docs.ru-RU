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
ms.openlocfilehash: c0beec8a0b234794d3f623c4ceac773db698dd79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412760"
---
# <a name="imapisupportgetoneofftable"></a>IMAPISupport::GetOneOffTable

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает указатель на односервную таблицу MAPI (список шаблонов, поддерживаемый всеми поставщиками адресных книг для создания новых получателей).
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом строки столбцов. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строки столбцов в формате Юникод. Если флаг MAPI_UNICODE не установлен, строки столбцов имеют формат ANSI.
    
 _lppTable_
  
> [out] Указатель на указатель на одностолевую таблицу.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Односеаленная таблица была успешно извлечена.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::GetOneOffTable реализован** для объектов поддержки поставщика адресной книги. Поставщики адресных книг **звонят в GetOneOffTable,** чтобы получить полный список шаблонов для создания новых получателей. В эту таблицу входят шаблоны, которые включают поставщиков адресных книг, активных в поддержке сеанса, а также шаблоны, поддерживаемые MAPI. 
  
Созданные получатели можно использовать для обращения к сообщению или добавить в контейнер адресной книги.
  
Список свойств, которые составляют необходимый столбец, задав в однонастройных таблицах, см. в статье ["Разовые таблицы".](one-off-tables.md)
  
Установка флага MAPI_UNICODE в параметре _ulFlags_ влияет на формат столбцов, возвращаемых методами [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows.](imapitable-queryrows.md) Этот флаг также управляет типами свойств в порядке сортировки, возвращаемом методом [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md) 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если вы зарегистрированы для получения уведомлений об изменениях в этой разной таблице, вы также будете получать уведомления об изменениях в разовых таблицах других поставщиков. На основе этих уведомлений можно поддерживать новые типы адресов, добавленные во время текущего сеанса.
  
## <a name="see-also"></a>См. также



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPISupport::NewEntry](imapisupport-newentry.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[Каноническое свойство PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Разовые таблицы](one-off-tables.md)

