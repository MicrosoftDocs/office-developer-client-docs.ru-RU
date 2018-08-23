---
title: IProfSect IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfSect
api_type:
- COM
ms.assetid: 4e704044-5230-4521-a0d2-b7c2f981c954
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a8152a9cad7623a077cd9df3f678a9ada56e3960
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577963"
---
# <a name="iprofsect--imapiprop"></a>IProfSect : IMAPIProp

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Works со свойствами объектов раздела профилей. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Предоставляемые:  <br/> |Объекты раздела профиля  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IProfSect  <br/> |
|Тип указателя:  <br/> |LPPROFSECT  <br/> |
|Модель транзакций:  <br/> |Не входящих в транзакции  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

Этот интерфейс не имеет каких-либо уникальных методов.
  
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Интерфейс **IProfSect** не имеет уникальное методы свои собственные, но профиля можно вызвать методы [IMAPIProp](imapipropiunknown.md) раздела. Существуют различия между реализации **IProfSect** и другими реализациями **IMAPIProp**:
  
- **IProfSect** не поддерживает модели транзакции. 
    
- **IProfSect** не поддерживает именованные свойства. 
    
- **IProfSect** оставляет за собой диапазон идентификатор 0x67F0 для 0x67ff для свойства безопасности. 
    
Отсутствие поддержки модели транзакций означает, что все изменения, внесенные в раздел профиля следующие вызовы [IMAPIProp::CopyProps](imapiprop-copyprops.md) и [IMAPIProp::CopyTo](imapiprop-copyto.md) методы возникают сразу же. Вызовы метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) успешно, но не фактически сохранить все изменения. 
  
Для защиты от изменения, внесенные преждевременно, поставщиков услуг необходимо принять копий своих профилей разделов, отображаемых для пользователей с помощью страницы свойств. Страницы свойств должны работать с копией, вместо раздела реальных профилей. Когда пользователь нажимает кнопку **ОК** , чтобы проверить правильность изменения, можно сохранить изменения в раздел реальных профилей. 
  
Для реализации свойств с помощью скопированного профиля, используйте следующую процедуру:
  
1. Откройте раздел профиля путем вызова метода [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) или [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) . 
    
2. Вызовите функцию [CreateIProp](createiprop.md) для получения данных свойства объекта — объект, который поддерживает интерфейс **IPropData** . 
    
3. Вызов метода [IMAPIProp::CopyTo](imapiprop-copyto.md) раздела профиля для копирования свойства, которые будут отображаться на странице свойств из раздела профиля объект данных свойства. 
    
4. Вызовите метод [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) для запроса, что поставщик услуг открыть окно свойств и передать указатель на объект данных свойства с помощью параметра _lpConfigData_ . 
    
5. Когда пользователь сохраняет изменения свойства конфигурации в окне свойств, вызовите метод [IMAPIProp::CopyTo](imapiprop-copyto.md) , чтобы скопировать свойства из объекта данных свойства раздела профиля. 
    
Разделы профилей, в отличие от других объектов, не поддерживают именованные свойства. Методы [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) и [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) возвращает MAPI_E_NO_SUPPORT, если они называются для объекта раздела профиля. При использовании метода [IMAPIProp::SetProps](imapiprop-setprops.md) для определения идентификаторов свойств в диапазоне выше 0x8000 тип свойства PT_ERROR будут возвращены. 
  
Разделы профилей зарезервировать идентификатор диапазон 0x67F0 для 0x67FF для свойства безопасности. Поставщики услуг могут использовать этот диапазон для хранения паролей и других учетных данных от поставщика. В этот диапазон не возвращаются свойства в полный список свойств при передается в параметр _lpPropTag_ метода [IMAPIProp::GetProps](imapiprop-getprops.md) , а также их возвращаются в параметре _lppPropTagArray_ [ IMAPIProp::GetPropList](imapiprop-getproplist.md) метод. Защищенные свойства должны быть затребованы специально идентификаторам. 
  
MAPI предоставляющей профиля с жестко MUID_PROFILE_INSTANCE константу как его идентификатор и **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)), как его отдельное свойство. MAPI гарантирует, что значение свойства **PR_SEARCH_KEY** будет уникальным во всех созданных профилей. Используйте **PR_SEARCH_KEY** вместо **PR_PROFILE_NAME** уникальности важна, так как это возможно, для удаленного профиль, который необходимо следовать другого профиля с тем же именем. 
  
Дополнительные сведения об использовании профилей разделах содержатся в разделе [профили, Администрирование и службы сообщений](administering-profiles-and-message-services.md).
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

