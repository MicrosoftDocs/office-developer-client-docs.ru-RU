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

**Относится к**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Параметры

_ulUIParam_
  
> [in] Handle to the parent window of the common address dialog box and other related displays.
    
_cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
_lpEntryID_
  
> [in] Указатель на идентификатор записи для открываемого хранения сообщений. Параметр  _lpEntryID_ не должен иметь NULL. 
    
_lpInterface_
  
> [in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который будет использоваться для доступа к хранилище сообщений. При передаче NULL параметр _lppMDB_ возвращает указатель на стандартный интерфейс для хранения сообщений (**IMsgStore).**
    
_ulFlags_
  
> [in] Битоваяmas флагов, которая управляет открытием объекта. Можно использовать следующие флаги:
    
  - MAPI_BEST_ACCESS: запрашивает, чтобы хранилище сообщений было открыто с максимальным разрешенным для пользователя сетевым разрешением и максимальным разрешением клиентского приложения. Например, если у клиента есть разрешение на чтение и записи, хранилище сообщений должно быть открыто с разрешением на чтение и записи; Если у клиента есть разрешение только на чтение, хранилище сообщений должно быть открыто с разрешением только для чтения. 
      
  - MAPI_DEFERRED_ERRORS: позволяет **OpenMsgStore** успешно возвращаться, возможно, до того, как хранилище сообщений будет полностью доступно вызываемому клиенту. Если хранилище сообщений не доступно, последующий вызов объекта может вызвать ошибку. 
      
  - MDB NO_DIALOG: предотвращает отображение диалогов для \_ логотипа. Если этот флаг установлен, а **в OpenMsgStore** недостаточно сведений о конфигурации, чтобы открыть хранилище сообщений без помощи пользователя, он возвращает MAPI_E_LOGON_FAILED. Если этот флажок не установлен, поставщик store сообщений может отправить пользователю запрос на исправление имени или пароля, а также выполнить другие действия, необходимые для установления подключения к хранилище сообщений. 
      
  - MDB NO_MAIL: хранилище сообщений не должно использоваться для отправки \_ или получения почты. Если этот флаг установлен, MAPI не уведомляет пул mapI о том, что это хранилище сообщений открыто.
      
  - MDB ONLINE: в режиме кэшации Exchange клиент или поставщик услуг может вызвать этот метод с помощью MDB_ONLINE переопределять подключение к локальному хранилище сообщений и открывать хранилище на удаленном \_ сервере. Невозможно открыть хранилище Exchange в режиме кэшации и в режиме без кэшации одновременно в одном сеансе MAPI. Если вы уже открыли хранилище кэшированных сообщений, потребуется его закрыть перед открытием с этим флагом или открыть новый сеанс MAPI, в котором можно будет открыть хранилище Exchange на удаленном сервере с использованием этого флага.
      
  - MDB_TEMPORARY: сообщает MAPI, что хранилище сообщений не является постоянным и не должно быть добавлено в таблицу хранения сообщений. Этот флаг используется для входа в хранилище сообщений, чтобы получить сведения из раздела профиля программным путем. 
      
  - MDB_WRITE: запрашивает разрешение на чтение и записи в хранилище сообщений.
    
_lppMDB_
  
> [out] Указатель на указатель на хранилище сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Хранилище сообщений успешно открыто.
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка доступа к хранилище сообщений, для которого у пользователя недостаточно разрешений.
    
MAPI_E_NOT_FOUND 
  
> Хранилище сообщений, обозначенное  _lpEntryID,_ не существует. 
    
MAPI_E_UNKNOWN_CPID 
  
> Сервер не настроен для поддержки кодовой страницы клиента.
    
MAPI_E_UNKNOWN_LCID 
  
> Сервер не настроен для поддержки сведений о региональных настройках клиента.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов был успешным, но у поставщика хранения сообщений есть сведения об ошибке. При возврате этого предупреждения вызов должен быть обработан как успешный. Чтобы получить сведения об ошибке от поставщика, вызовите метод [IMAPISession::GetLastError.](imapisession-getlasterror.md) Чтобы проверить это предупреждение, используйте **макрос HR_FAILED.** Дополнительные сведения см. в [теме "Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::OpenMsgStore** открывает определенное хранилище сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Уровень разрешений по умолчанию для хранилищ сообщений — только для чтения. Если вы установите флаг MDB_WRITE, возможно, вам все равно не будет предоставлено разрешение на чтение и записи. Окончательный уровень доступа, назначаемого MAPI хранилищем сообщений, зависит от вашего уровня разрешений, самого магазина сообщений и поставщика. 
  
Если вызвать **OpenMsgStore,** чтобы открыть хранилище сообщений с разрешением только на чтение, произойдет следующее: 
  
- В свойстве **PR \_ STORE_SUPPORT_MASK** Store [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)MODIFY_OK и \_ CREATE_OK \_ store. 
    
- Вызовы для открытия одного из сообщений или папок в хранилище сообщений с помощью [IMAPISession::OpenEntry](imapisession-openentry.md) с установленным MAPI_MODIFY не удастся. 
    
- Вызовы для открытия одного из свойств сообщений или папок в хранилище сообщений с помощью [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с флагом MAPI_MODIFY не удастся. 
    
- Вызовы любого из следующих методов не удастся: 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- Вызовы следующих методов не удастся, если место назначения для скопированного сообщения предназначено только для чтения, независимо от того, является ли назначение таким же, как хранилище исходных сообщений или другое хранилище, предназначенное только для чтения.
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |CallOpenMsgStore  <br/> |MFCMAPI использует метод **IMAPISession::OpenMsgStore** для открытия хранилищ сообщений.  <br/> |
   
## <a name="see-also"></a>См. также

- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession: IUnknown](imapisessioniunknown.md)
- [MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
- [Использование макроса для обработки ошибок](using-macros-for-error-handling.md)

