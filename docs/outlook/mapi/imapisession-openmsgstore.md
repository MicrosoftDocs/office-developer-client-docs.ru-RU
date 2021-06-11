---
title: IMAPISessionOpenMsgStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenMsgStore
api_type:
- COM
ms.assetid: 7f73b5cf-7093-42e9-8acc-63d73df77cf5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 19d3df004676a71e2bf6243d9288efd824d99c33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418024"
---
# <a name="imapisessionopenmsgstore"></a>IMAPISession::OpenMsgStore

**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает хранилище сообщений и возвращает указатель [IMsgStore](imsgstoreimapiprop.md) для дальнейшего доступа. 
  
```cpp
HRESULT OpenMsgStore(
  ULONG_PTR ulUIParam,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a>Parameters

_ulUIParam_
  
> [in] Ручка родительского окна общего диалогового окна адресов и других связанных дисплеев.
    
_cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
_lpEntryID_
  
> [in] Указатель на идентификатор входа открываемого магазина сообщений. Параметр  _lpEntryID_ не должен быть NULL. 
    
_lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который будет использоваться для доступа к хранилище сообщений. Передача NULL заставляет _параметр lppMDB_ возвращать указатель в стандартный интерфейс для магазина **сообщений (IMsgStore).**
    
_ulFlags_
  
> [in] Битмашка флагов, контролируемая тем, как открывается объект. Можно использовать следующие флаги:
    
  - MAPI_BEST_ACCESS. Запрашивает, чтобы хранилище сообщений было открыто с максимальным разрешением сети, разрешенным для пользователя, и с максимальным разрешением клиентского приложения. Например, если у клиента есть разрешение на чтение и написание, магазин сообщений должен быть открыт с разрешения на чтение и написание; если у клиента есть разрешение только для чтения, магазин сообщений должен быть открыт с разрешения только для чтения. 
      
  - MAPI_DEFERRED_ERRORS: Позволяет **OpenMsgStore** успешно возвращаться, возможно, до того, как хранилище сообщений будет полностью доступно для вызываемого клиента. Если хранилище сообщений не доступно, последующий вызов объекта может вызвать ошибку. 
      
  - MDB \_ NO_DIALOG: предотвращает отображение диалогов с логотипом. Если этот флаг установлен, а **у OpenMsgStore** недостаточно сведений о конфигурации, чтобы открыть хранилище сообщений без помощи пользователя, он возвращается MAPI_E_LOGON_FAILED. Если этот флаг не установлен, поставщик магазина сообщений может побудить пользователя исправить имя или пароль или выполнить другие действия, необходимые для установления подключения к хранилище сообщений. 
      
  - MDB NO_MAIL: хранилище сообщений не должно использоваться для \_ отправки или получения почты. Когда этот флаг установлен, MAPI не уведомляет шпалер MAPI о том, что этот хранилище сообщений открывается.
      
  - MDB ONLINE. В режиме кэшировать Exchange клиент или поставщик услуг может вызвать этот метод с помощью MDB_ONLINE переопределения подключения к локальному хранилище сообщений и открытия магазина на удаленном \_ сервере. Нельзя открыть хранилище Exchange в кэшном режиме и в режиме без кэшации одновременно в том же сеансе MAPI. Если вы уже открыли хранилище кэшированных сообщений, потребуется его закрыть перед открытием с этим флагом или открыть новый сеанс MAPI, в котором можно будет открыть хранилище Exchange на удаленном сервере с использованием этого флага.
      
  - MDB_TEMPORARY: предписывает MAPI, что хранилище сообщений не является постоянным и не должно быть добавлено в таблицу хранения сообщений. Этот флаг используется для входа в хранилище сообщений, чтобы получить сведения программным образом из раздела профилей. 
      
  - MDB_WRITE: запрашивает разрешение на чтение и записи в хранилище сообщений.
    
_lppMDB_
  
> [вышел] Указатель на указатель магазина сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Хранилище сообщений было успешно открыто.
    
MAPI_E_NO_ACCESS 
  
> Была предпринята попытка доступа к хранилище сообщений, для которого у пользователя недостаточно разрешений.
    
MAPI_E_NOT_FOUND 
  
> Хранилище сообщений, указанный  _lpEntryID,_ не существует. 
    
MAPI_E_UNKNOWN_CPID 
  
> Сервер не настроен для поддержки страницы кода клиента.
    
MAPI_E_UNKNOWN_LCID 
  
> Сервер не настроен для поддержки сведений о локальном уровне клиента.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов удался, но у поставщика магазина сообщений есть сведения об ошибках. Когда это предупреждение возвращается, вызов должен быть обработан как успешный. Чтобы получить сведения об ошибках от поставщика, позвоните по [методу IMAPISession::GetLastError.](imapisession-getlasterror.md) Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::OpenMsgStore** открывает определенный магазин сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Уровень разрешений по умолчанию для магазинов сообщений является только для чтения. Если вы установите флаг MDB_WRITE, вам все равно может не быть предоставлено разрешение на чтение и написание. Конечный уровень доступа, который MAPI назначает в хранилище сообщений, зависит от уровня разрешений, самого магазина сообщений и поставщика магазина сообщений. 
  
Если вы **позвоните в OpenMsgStore,** чтобы открыть хранилище сообщений с разрешения только для чтения, произойдет следующее: 
  
- Pr-STORE_SUPPORT_MASK **магазина \_** [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)не будет иметь набор MODIFY_OK store \_ \_ CREATE_OK. 
    
- Вызовы для открытия одного из сообщений или папок магазина сообщений с помощью [IMAPISession::OpenEntry](imapisession-openentry.md) с набором флага MAPI_MODIFY не удастся. 
    
- Вызовы для открытия одного из свойств сообщений или папок магазина сообщений с помощью [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с флагом MAPI_MODIFY не удастся. 
    
- Вызовы к любому из следующих методов сбой: 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- Вызовы к следующим методам не будут работать, если предназначение для скопированного сообщения только для чтения, является ли пункт назначения таким же, как хранилище исходных сообщений или другой магазин только для чтения.
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |CallOpenMsgStore  <br/> |MFCMAPI использует **метод IMAPISession::OpenMsgStore** для открытия магазина сообщений.  <br/> |
   
## <a name="see-also"></a>См. также

- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession: IUnknown](imapisessioniunknown.md)
- [MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
- [Использование макроса для обработки ошибок](using-macros-for-error-handling.md)

