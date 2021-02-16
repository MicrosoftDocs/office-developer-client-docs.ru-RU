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
ms.openlocfilehash: 99ce944bec94a1e832f77fa8b0916ac1c76f6dc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406600"
---
# <a name="iprofsect--imapiprop"></a>IProfSect : IMAPIProp

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Работает со свойствами объектов раздела профиля. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Выставим:  <br/> |Объекты раздела профиля  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IProfSect  <br/> |
|Тип указателя:  <br/> |LPPROFSECT  <br/> |
|Модель транзакций:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

Этот интерфейс не имеет уникальных методов.
  
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Интерфейс **IProfSect** не имеет собственных уникальных методов, но можно вызвать методы [IMAPIProp](imapipropiunknown.md) раздела профиля. Между реализацией **IProfSect** и другими реализациями **IMAPIProp** существуют некоторые различия:
  
- **IProfSect** не поддерживает модель транзакций. 
    
- **IProfSect** не поддерживает именуемые свойства. 
    
- **IProfSect** резервировать диапазон 0x67F0 0x67ff для безопасных свойств. 
    
Если модель транзакций не поддерживается, все изменения, внесенные в раздел профиля после вызовов методов [IMAPIProp::CopyProps](imapiprop-copyprops.md) и [IMAPIProp::CopyTo,](imapiprop-copyto.md) происходят немедленно. Вызовы метода [IMAPIProp::SaveChanges будут](imapiprop-savechanges.md) успешными, но фактически не будут сохранять изменения. 
  
Чтобы защититься от преждевременных изменений, поставщики услуг должны создавать копии своих разделов профилей, которые отображаются для пользователей с помощью таблиц свойств. Листы свойств должны работать с копией, а не с реальным разделом профиля. Когда пользователь нажимает  кнопку "ОК", чтобы проверить правильность изменений, изменения можно сохранить в реальном разделе профиля. 
  
Чтобы реализовать лист свойств с помощью скопированные разделы профиля, используйте следующую процедуру:
  
1. Откройте раздел профиля, вызывая метод [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) или [IProviderAdmin::OpenProfileSection.](iprovideradmin-openprofilesection.md) 
    
2. Вызовите [функцию CreateIProp,](createiprop.md) чтобы получить объект данных свойства — объект, который поддерживает **интерфейс IPropData.** 
    
3. Вызовите метод [IMAPIProp::CopyTo](imapiprop-copyto.md) раздела профиля, чтобы скопировать свойства, которые будут отображаться на листе свойств, из раздела профиля в объект данных свойства. 
    
4. Вызовите метод [IMAPISupport::D oConfigPropSheet,](imapisupport-doconfigpropsheet.md) чтобы запросить, чтобы поставщик услуг отображал лист свойств, и передать указатель на объект данных свойства в параметре _lpConfigData._ 
    
5. Когда пользователь сохраняет изменения свойств конфигурации на листе свойств, вызовите метод [IMAPIProp::CopyTo,](imapiprop-copyto.md) чтобы скопировать свойства из объекта данных свойства обратно в раздел профиля. 
    
Разделы профилей, в отличие от других объектов, не поддерживают именуемые свойства. Методы [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) и [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) возвращают MAPI_E_NO_SUPPORT, если они вызваны в объекте раздела профиля. Если вы используете метод [IMAPIProp::SetProps,](imapiprop-setprops.md) чтобы установить идентификаторы свойств в диапазоне выше 0x8000, будет возвращен тип PT_ERROR свойства. 
  
Разделы профилей резервировать диапазон 0x67F0 0x67FF для безопасных свойств. Поставщики услуг могут использовать этот диапазон для хранения паролей и других учетных данных, характерных для конкретного поставщика. Свойства в этом диапазоне не возвращаются в полном списке свойств, когда NULL передается в _параметре lpPropTag_ метода [IMAPIProp::GetProps,](imapiprop-getprops.md) и не возвращаются в _параметре lppPropTagArray_ метода [IMAPIProp::GetPropList.](imapiprop-getproplist.md) Защищенные свойства должны запрашиваться в частности их идентификаторами. 
  
MAPI передает раздел профиля с жестко заданная константой MUID_PROFILE_INSTANCE в качестве идентификатора, а PR_SEARCH_KEY **(** [PidTagSearchKey)](pidtagsearchkey-canonical-property.md)в качестве своего единственного свойства. MAPI гарантирует, что **PR_SEARCH_KEY** свойства будет уникальным для всех созданных профилей. Используйте **PR_SEARCH_KEY** вместо **PR_PROFILE_NAME,** если важна уникальность, так как за удаленным профилем может следовать другой профиль с тем же именем. 
  
Дополнительные сведения об использовании разделов профилей см. в разделах ["Администрирование профилей и служб сообщений".](administering-profiles-and-message-services.md)
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

