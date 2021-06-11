---
title: IMAPISessionQueryIdentity
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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает идентификатор входа объекта, который предоставляет основное удостоверение сеанса.
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parameters

 _lpcbEntryID_
  
> [вышел] Указатель на количество byte в идентификаторе входа, на который указывает параметр _lppEntryID._ 
    
 _lppEntryID_
  
> [вышел] Указатель на указатель на идентификатор входа объекта, который предоставляет основное удостоверение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Первичный идентификатор был успешно возвращен.
    
MAPI_W_NO_SERVICE 
  
> Вызов удался, но основного удостоверения для сеанса не существует. Когда это предупреждение возвращается, вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::QueryIdentity** извлекает основное удостоверение для текущего сеанса и возвращает значение через параметр _lppEntryID._ Основной идентификатор — это объект, как правило, пользователь обмена сообщениями, который представляет пользователя сеанса.  _lppEntryID_ возвращает основное удостоверение объекта [IMailUser,](imailuserimapiprop.md) который также хранится в качестве свойства [PidTagEntryID.](pidtagentryid-canonical-property.md) Значение, возвращенное в _lppEntryID,_ можно использовать для открытия объекта **IMailUser** с помощью [IMAPISession::OpenEntry.](imapisession-openentry.md)
  
Хотя многие поставщики услуг в нескольких службах сообщений могут предоставлять основные удостоверения для сеанса, MAPI назначает одного поставщика услуг. Поставщик услуг, который поставляет основные удостоверения, задает следующие элементы:
  
- Флаг STATUS_PRIMARY_IDENTITY в **свойстве PR_RESOURCE_FLAGS** [(PidTagResourceFlags).](pidtagresourceflags-canonical-property.md)
    
- Свойство **PR_IDENTITY_DISPLAY** [(PidTagIdentityDisplay).](pidtagidentitydisplay-canonical-property.md)
    
- Свойство **PR_IDENTITY_ENTRYID** [(PidTagIdentityEntryId).](pidtagidentityentryid-canonical-property.md)
    
- Свойство **PR_IDENTITY_SEARCH_KEY** [(PidTagIdentitySearchKey).](pidtagidentitysearchkey-canonical-property.md)
    
Если поставщик услуг, который поставляет основные удостоверения, принадлежит службе сообщений, другие поставщики услуг в службе сообщений также PR_IDENTITY свойства. Эти свойства публикуются в таблице состояния сеанса. 
  
По возможности **объект QueryId возвращает** значение для **свойства** PR_IDENTITY_ENTRYID из строки состояния, помеченной STATUS_PRIMARY_IDENTITY. Если свойство **PR_IDENTITY_ENTRYID** отсутствует в основной строке удостоверений, **объект QueryIdentity** возвращает идентификатор одноавтной записи, построенный с другими сведениями из этой строки. 
  
Если флаг STATUS_PRIMARY_IDENTITY отсутствует во всех  столбцах PR_RESOURCE_FLAG в таблице состояния, **queryIdentity** возвращает первый идентификатор записи, который он находит. Когда нет подходящего идентификатора записи для возврата, **queryIdentity** успешно с предупреждением MAPI_W_NO_SERVICE и указывает  _lppEntryID_ на жесткий кодовый идентификатор записи. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете вызвать [метод IMsgServiceAdmin::SetPrimaryIdentity,](imsgserviceadmin-setprimaryidentity.md) чтобы назначить службе сообщений задачу поставки основного удостоверения сеанса. 
  
Еще один способ получения основного удостоверения — поиск  таблицы состояния строки с PR_RESOURCE_FLAGS столбцов, STATUS_PRIMARY_IDENTITY. Дополнительные сведения об этом альтернативном способе получения сведений о удостоверениях см. в таблице [status Table и Status Objects.](status-table-and-status-objects.md)
  
После завершения использования идентификатора записи для основного удостоверения, возвращенного **объектом QueryIdentity,** освободите его память, позвонив в [функцию MAPIFreeBuffer.](mapifreebuffer.md) 
  
Дополнительные сведения о удостоверении в целом см. в [главной идентификации MAPI.](mapi-primary-identity.md) 
  
Дополнительные сведения о том, как получить удостоверение сеанса MAPI, см. в дополнительных сведениях о том, как получить удостоверение основного поставщика и удостоверение [поставщика.](retrieving-primary-and-provider-identity.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnQueryIdentity  <br/> |MFCMAPI использует **метод IMAPISession::QueryIdentity** для открытия записи адресной книги для основного удостоверения сеанса.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISession::OpenEntry](imapisession-openentry.md)
  
[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Основной идентификатор MAPI](mapi-primary-identity.md)
  
[Повторное иждивение удостоверения основного поставщика и поставщика](retrieving-primary-and-provider-identity.md)
  
[Использование макроса для обработки ошибок](using-macros-for-error-handling.md)
  
[Объекты таблицы состояния и состояния](status-table-and-status-objects.md)

