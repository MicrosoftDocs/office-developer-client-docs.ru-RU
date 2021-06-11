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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Работает со свойствами объектов раздела профилей. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Подвергается:  <br/> |Объекты раздела профилей  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IProfSect  <br/> |
|Тип указателя:  <br/> |LPPROFSECT  <br/> |
|Модель транзакции:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

Этот интерфейс не имеет уникальных методов.
  
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_PROFILE_NAME** [(PidTagProfileName)](pidtagprofilename-canonical-property.md)  <br/> |Только для чтения  <br/> |
   
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Интерфейс **IProfSect** не имеет собственных уникальных методов, но можно вызвать методы [IMAPIProp](imapipropiunknown.md) раздела профиля. Есть некоторые различия между **реализацией IProfSect** и другими реализациями **IMAPIProp:**
  
- **IProfSect** не поддерживает модель транзакций. 
    
- **IProfSect** не поддерживает названные свойства. 
    
- **IProfSect** оставляет диапазон идентификаторов 0x67F0 0x67ff для безопасных свойств. 
    
Не поддержка модели транзакций означает, что все изменения, внесенные в профильный раздел после звонков в [методы IMAPIProp::CopyProps](imapiprop-copyprops.md) и [IMAPIProp::CopyTo,](imapiprop-copyto.md) происходят немедленно. Вызовы к [методу IMAPIProp::SaveChanges](imapiprop-savechanges.md) успешно, но на самом деле не сохранения изменений. 
  
Чтобы защититься от изменений, которые происходят преждевременно, поставщикам услуг необходимо создавать копии своих разделов профилей, отображаемых пользователям через листы свойств. Листы свойств должны работать с копией, а не с реальным разделом профилей. Когда пользователь нажимает кнопку **ОК,** чтобы убедиться, что изменения точны, изменения можно сохранить в реальном разделе профилей. 
  
Чтобы реализовать лист свойств с помощью скопированного раздела профиля, используйте следующую процедуру:
  
1. Откройте раздел профилей, назвав [метод IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) или [IProviderAdmin::OpenProfileSection.](iprovideradmin-openprofilesection.md) 
    
2. Вызов [функции CreateIProp](createiprop.md) для получения объекта данных свойства — объекта, поддерживаюного **интерфейс IPropData.** 
    
3. Вызовите метод [IMAPIProp::CopyTo](imapiprop-copyto.md) в разделе профилей, чтобы скопировать свойства, которые будут отображаться на листе свойств из раздела профилей в объект данных свойства. 
    
4. Вызывай метод [IMAPISupport::D ConfigPropSheet,](imapisupport-doconfigpropsheet.md) чтобы попросить поставщика услуг отобразить лист свойств, и передать указатель объекту данных свойств в параметре _lpConfigData._ 
    
5. Когда пользователь сохраняет изменения свойств конфигурации в листе свойств, позвоните в [метод IMAPIProp::CopyTo,](imapiprop-copyto.md) чтобы скопировать свойства из объекта данных свойств обратно в раздел профиль. 
    
Разделы профилей, в отличие от других объектов, не поддерживают названные свойства. Методы [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) и [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) возвращаются MAPI_E_NO_SUPPORT, если они вызваны на объекте раздела профилей. Если вы используете метод [IMAPIProp::SetProps](imapiprop-setprops.md) для набора идентификаторов свойств в диапазоне выше 0x8000, тип PT_ERROR свойства будет возвращен. 
  
Разделы профилей резервировать диапазон идентификаторов 0x67F0 0x67FF для безопасных свойств. Поставщики услуг могут использовать этот диапазон для хранения паролей и других учетных данных, определенных для поставщика. Свойства в этом диапазоне не возвращаются в полный список свойств, когда NULL передается в _параметре lpPropTag_ метода [IMAPIProp::GetProps](imapiprop-getprops.md) и не возвращается в _параметре lppPropTagArray_ метода [IMAPIProp::GetPropList.](imapiprop-getproplist.md) Защищенные свойства должны запрашиваться в частности их идентификаторами. 
  
MAPI обставляет профильный раздел с жестко закодированными константными MUID_PROFILE_INSTANCE в качестве идентификатора и PR_SEARCH_KEY[(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)как одно свойство.  MAPI гарантирует, что **PR_SEARCH_KEY** свойств будет уникальным среди всех созданных профилей. Используйте **PR_SEARCH_KEY,** а **не PR_PROFILE_NAME,** когда важна уникальность, так как за удаленным профилем может последовать другой профиль с тем же именем. 
  
Дополнительные сведения об использовании разделов профилей см. в разделах [Администрирование профилей и служб сообщений.](administering-profiles-and-message-services.md)
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

