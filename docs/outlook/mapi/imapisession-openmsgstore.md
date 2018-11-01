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
ms.openlocfilehash: fdf75787153f9a85e6a7bcddff44cf2c468a7975
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595036"
---
# <a name="imapisessionopenmsgstore"></a>IMAPISession::OpenMsgStore

**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает хранилища сообщений и возвращает указатель [IMsgStore](imsgstoreimapiprop.md) для дальнейшей доступа. 
  
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
  
> [in] Дескриптор родительского окна стандартным диалоговым окном адрес и других, связанных с отображает.
    
_cbEntryID_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
_lpEntryID_
  
> [in] Указатель на идентификатор записи хранилища сообщение, которое требуется открыть. Параметр _lpEntryID_ не должна быть NULL. 
    
_lpInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к хранилищу данных сообщений. Значение NULL вызывает параметр _lppMDB_ возвращает указатель на стандартный интерфейс для хранилища сообщений (**IMsgStore**).
    
_ulFlags_
  
> [in] Битовая маска флаги, который определяет способ открытия объекта. Можно использовать следующие флажки:
    
  - MAPI_BEST_ACCESS: Запросы открыть хранилище сообщений с разрешениями максимальное сетевое разрешено для пользователя и максимальное число клиентов разрешения приложения. Например если клиент имеет разрешение на чтение и запись, хранилища сообщений должен быть открыт с разрешением на чтение и запись; Если клиент имеет разрешение на чтение, хранилище сообщений должен быть открыт с разрешением только для чтения. 
      
  - MAPI_DEFERRED_ERRORS: Разрешает **OpenMsgStore** для возврата успешно, возможно перед сообщением хранилища доступными для клиента. Если хранилище сообщений недоступен, вызов последующих объектов может вызвать ошибку. 
      
  - MDB\_NO_DIALOG: не отображать диалоговые окна входа в систему. Если этот флаг установлен, и **OpenMsgStore** содержит сведения о конфигурации недостаточно для открытия хранилища сообщений без помощи пользователя, он возвращает MAPI_E_LOGON_FAILED. Если этот флаг не установлен, поставщик хранения сообщений можно запрашивать у пользователя в нужное имя или пароль или для выполнения других действий, необходимых для установки подключения к хранилищу сообщений. 
      
  - MDB\_NO_MAIL: хранилище сообщений не должна использоваться для отправки или получения почты. Если этот флаг, MAPI не уведомляет диспетчер очереди MAPI открыта, что хранилища.
      
  - MDB\_ONLINE: В режиме кэширования данных Exchange, клиента или поставщика можно вызвать этот метод с MDB_ONLINE переопределение подключения к хранилищу локального сообщения и откройте хранилище на удаленном сервере. Не удается открыть хранилища Exchange в режиме кэширования и в режиме без кэширования в то же время, в том же сеансе MAPI. Если вы уже открыли хранилище кэшированных сообщений, потребуется его закрыть перед открытием с этим флагом или открыть новый сеанс MAPI, в котором можно будет открыть хранилище Exchange на удаленном сервере с использованием этого флага.
      
  - MDB_TEMPORARY: Указывает, что MAPI, что хранилище сообщений не является постоянным и не следует добавлять к таблице хранилища сообщений. Этот флаг используется для входа в хранилище сообщений, сведения могут быть получены из раздела профиля программными средствами. 
      
  - MDB_WRITE: Запросы на чтение и запись разрешений для хранилища сообщений.
    
_lppMDB_
  
> [out] Указатель на указатель хранилища сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Хранилище сообщений был успешно открыт.
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка получить доступ к хранилища сообщений, для которого пользователь имеет недостаточно разрешений.
    
MAPI_E_NOT_FOUND 
  
> Хранилище сообщений, указанный в параметре _lpEntryID_ не существует. 
    
MAPI_E_UNKNOWN_CPID 
  
> Сервер не настроен для поддержки кодовой страницы клиента.
    
MAPI_E_UNKNOWN_LCID 
  
> Сервер не настроен для поддержки сведения о языковом стандарте клиента.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов завершился успешно, но поставщика хранилища сообщений имеет доступные сведения об ошибке. При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении. Чтобы получить сведения об ошибке от поставщика, вызовите метод [IMAPISession::GetLastError](imapisession-getlasterror.md) . Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Замечания

Метод **IMAPISession::OpenMsgStore** открывает хранилища конкретное сообщение. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Уровень разрешений по умолчанию для хранилищ сообщений доступен только для чтения. Если значение флага MDB_WRITE, вы по-прежнему может не иметь разрешение чтения и записи. Последний уровень доступа, который назначает MAPI для хранилища сообщений, зависит от уровней разрешений, сообщение хранилища себя и поставщика хранилища сообщений. 
  
При вызове **OpenMsgStore** , чтобы открыть хранилище сообщений с разрешением только для чтения, произойдет следующее: 
  
- Хранилище **связей с Общественностью\_STORE_SUPPORT_MASK** свойство ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), не будут иметь его ХРАНИЛИЩЕ\_MODIFY_OK и ХРАНИЛИЩЕ\_CREATE_OK бит set. 
    
- Откройте одну из сообщения или папки хранилища сообщений с помощью [IMAPISession::OpenEntry](imapisession-openentry.md) с установленным флагом MAPI_MODIFY вызовы завершится с ошибкой. 
    
- Откройте одну из свойств сообщения или папки хранилища сообщений с помощью [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с флагом MAPI_MODIFY вызовы завершится с ошибкой. 
    
- Вызовы любого из следующих методов произойдет ошибка. 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- Вызовы следующих методов завершится ошибкой, если назначения для скопированного сообщения доступен только для чтения, ли назначение — то же, что хранилище сообщений источника или другого хранилища только для чтения.
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |CallOpenMsgStore  <br/> |Mfcmapi (en) использует метод **IMAPISession::OpenMsgStore** для открытия хранилища сообщений.  <br/> |
   
## <a name="see-also"></a>См. также

- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession: IUnknown](imapisessioniunknown.md)
- [MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
- [Использование макросов для обработки ошибок](using-macros-for-error-handling.md)

