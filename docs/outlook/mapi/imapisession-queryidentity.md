---
title: имаписессионкуеридентити
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.QueryIdentity
api_type:
- COM
ms.assetid: a2cdda90-5457-49a7-b98c-7273ffe5cbbc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 396320c6b39553da09aa1f45d0c755f40a939382
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428223"
---
# <a name="imapisessionqueryidentity"></a>IMAPISession::QueryIdentity

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает идентификатор записи объекта, который предоставляет основной идентификатор для сеанса.
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Параметры

 _лпкбентрид_
  
> вышли Указатель на число байтов в идентификаторе записи, на который указывает параметр _лппентрид_ . 
    
 _лппентрид_
  
> вышли Указатель на указатель на идентификатор записи объекта, который предоставляет основное удостоверение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Основное удостоверение успешно возвращено.
    
MAPI_W_NO_SERVICE 
  
> Вызов выполнен успешно, но основной идентификатор для этого сеанса отсутствует. При возвращении этого предупреждения вызов должен обрабатываться как успешный. Чтобы проверить это предупреждение, используйте макрос **HR_FAILED** . Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession:: куеридентити** получает основное удостоверение для текущего сеанса и возвращает значение с помощью параметра _лппентрид_ . Основной идентификатор — это объект, обычно пользователь обмена сообщениями, представляющий пользователя сеанса.  _лппентрид_ Возвращает основной идентификатор объекта [имаилусер](imailuserimapiprop.md) , который также хранится в свойстве [PidTagEntryID](pidtagentryid-canonical-property.md) . Значение, возвращаемое в _лппентрид_ , можно использовать для открытия объекта **Имаилусер** с помощью [IMAPISession:: OpenEntry](imapisession-openentry.md).
  
Несмотря на то, что многие поставщики служб в нескольких службах сообщений могут предоставлять основной идентификатор сеанса, MAPI определяет одного поставщика услуг. Поставщик услуг, который предоставляет первичный идентификатор, задает следующие элементы:
  
- Флаг STATUS_PRIMARY_IDENTITY в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- Свойство **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)).
    
- Свойство **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)).
    
- Свойство **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)).
    
Если поставщик услуг, предоставляющий основной идентификатор, принадлежит службе сообщений, другие поставщики услуг в службе сообщений также устанавливают свойства PR_IDENTITY. Эти свойства публикуются в таблице состояния сеанса. 
  
Если это возможно, **куеридентити** возвращает значение свойства **PR_IDENTITY_ENTRYID** из строки состояния с тегом STATUS_PRIMARY_IDENTITY. Если в строке основного удостоверения отсутствует свойство **PR_IDENTITY_ENTRYID** , **куеридентити** возвращает идентификатор одноразовой записи, построенный с другими сведениями из этой строки. 
  
Если флаг STATUS_PRIMARY_IDENTITY отсутствует во всех столбцах **PR_RESOURCE_FLAG** в таблице status, **куеридентити** возвращает первый найденный идентификатор записи. Если нет подходящего идентификатора записи, **куеридентити** завершается с предупреждением MAPI_W_NO_SERVICE и указывает _лппентрид_ на жестко заданный идентификатор записи. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете вызвать метод [имсгсервицеадмин:: сетпримаридентити](imsgserviceadmin-setprimaryidentity.md) , чтобы назначить службе сообщений задачу предоставления основного удостоверения сеанса. 
  
Другой способ получения основного идентификатора — Поиск строки со столбцами **PR_RESOURCE_FLAGS** , для которых задано значение STATUS_PRIMARY_IDENTITY, в таблице состояния. Дополнительные сведения об этом альтернативном способе получения сведений об удостоверении можно узнать в статье [Status Table and Status Objects](status-table-and-status-objects.md).
  
По завершении использования идентификатора записи для основного удостоверения, возвращенного функцией **куеридентити**, освободите его память, вызвав функцию [мапифрибуффер](mapifreebuffer.md) . 
  
Для получения дополнительных сведений об удостоверении в разделе General ( [основной идентификатор MAPI](mapi-primary-identity.md)). 
  
Дополнительные сведения о получении удостоверения сеанса MAPI приведены в статье [Получение основного удостоверения и идентификатора поставщика](retrieving-primary-and-provider-identity.md). 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Маиндлг. cpp  <br/> |Кмаиндлг:: Онкуеридентити  <br/> |MFCMAPI использует метод **IMAPISession:: куеридентити** , чтобы открыть запись адресной книги для основного удостоверения сеанса.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISession::OpenEntry](imapisession-openentry.md)
  
[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Основной идентификатор MAPI](mapi-primary-identity.md)
  
[Получение основного удостоверения и удостоверения поставщика](retrieving-primary-and-provider-identity.md)
  
[Использование макросов для обработки ошибок](using-macros-for-error-handling.md)
  
[Объекты "таблица состояния" и "состояние"](status-table-and-status-objects.md)

