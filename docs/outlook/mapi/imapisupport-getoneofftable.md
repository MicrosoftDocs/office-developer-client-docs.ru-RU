---
title: имаписуппортжетонеоффтабле
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
  
Возвращает указатель на одноразовую таблицу MAPI (список шаблонов, которые поддерживаются всеми поставщиками адресных книг для создания новых получателей).
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Битовая маска флагов, определяющих тип строковых столбцов. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строковые столбцы представлены в формате Юникод. Если флаг MAPI_UNICODE не установлен, строковые столбцы имеют формат ANSI.
    
 _лпптабле_
  
> вышли Указатель на указатель на одноразовую таблицу.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица с одноразовым извлечением успешно получена.
    
## <a name="remarks"></a>Примечания

Метод **имаписуппорт:: жетонеоффтабле** реализован для объектов поддержки поставщика адресных книг. Поставщики адресных книг вызывают **жетонеоффтабле** , чтобы получить полный список шаблонов для создания новых получателей. В этой таблице содержатся шаблоны, которые поддерживаются активными поставщиками книг, которые активны во время сеанса, а также шаблоны, поддерживаемые MAPI. 
  
Только что созданные получатели могут быть использованы для обращения к сообщению или могут быть добавлены в контейнер адресной книги.
  
Список свойств, составляющих обязательный набор столбцов в одноразовых таблицах, приведен в разделе [одноразовые таблицы](one-off-tables.md).
  
Установка флага MAPI_UNICODE в параметре _ulFlags_ влияет на формат столбцов, возвращаемых методами [IMAPITable:: куериколумнс](imapitable-querycolumns.md) и [IMAPITable:: QueryRows](imapitable-queryrows.md) . Этот флаг также контролирует типы свойств в порядке сортировки, возвращаемом методом [IMAPITable:: куерисортордер](imapitable-querysortorder.md) . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если вы зарегистрированы, чтобы получать уведомления об изменениях, внесенных в эту одноразовую таблицу, вы также получите уведомления об изменениях в одноразовых таблицах поставщиков. На основе этих уведомлений вы можете поддерживать новые типы адресов, добавленные во время текущего сеанса.
  
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

