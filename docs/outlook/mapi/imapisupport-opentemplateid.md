---
title: IMAPISupportOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenTemplateID
api_type:
- COM
ms.assetid: 532f7af0-b2cc-49dd-b1de-e3ec1dc9a3e7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 07aa508b473f4a87d5b4909f83771549c301a600
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418507"
---
# <a name="imapisupportopentemplateid"></a>IMAPISupport::OpenTemplateID

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает запись получателя во внешнем поставщике адресной книги.
  
```cpp
HRESULT OpenTemplateID(
ULONG cbTemplateID,
LPENTRYID lpTemplateID,
ULONG ulTemplateFlags,
LPMAPIPROP lpMAPIPropData,
LPCIID lpInterface,
LPMAPIPROP FAR * lppMAPIPropNew,
LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a>Параметры

 _cbTemplateID_
  
> [in] Количество byte в идентификаторе шаблона, на который указывает _lpTemplateID._ 
    
 _lpTemplateID_
  
> [in] Указатель на идентификатор шаблона PR_TEMPLATEID **(** [PidTagTemplateid)](pidtagtemplateid-canonical-property.md)открываемой записи получателя.
    
 _ulTemplateFlags_
  
> [in] Битоваяmas флагов, используемая для описания открытия записи. Можно установить следующий флаг:
    
FILL_ENTRY 
  
> Создается новая запись. Когда внешнее поставщик получает последующий вызов [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) из MAPI, он может управлять тем, как создается запись, изменяя свойства, на которые указывает параметр  _lpMAPIPropData,_ или возвращая определенную реализацию интерфейса  _в lppMAPIPropNew,_ чтобы управлять тем, как заданы свойства новой записи. 
    
 _lpMAPIPropData_
  
> [in] Указатель на реализацию интерфейса, которую звоняя использует для доступа к записи. Это реализация, которую внешнее поставщик может обтекать собственной реализацией и вернуть в параметр _lppMAPIPropNew._ Параметр _lpMAPIPropData_ должен указать на реализацию интерфейса чтения и записи, которая является потомком [IMAPIProp : IUnknown](imapipropiunknown.md) и поддерживает интерфейс, запрашивается в _параметре lpInterface._ 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который будет использоваться для доступа к записи. Параметр _lppMAPIPropNew_ указывает на интерфейс типа, заданного _lpInterface._ Передача NULL возвращает стандартный интерфейс для пользователя обмена сообщениями, IID_IMailUser. 
    
 _lppMAPIPropNew_
  
> [out] Указатель на реализацию интерфейса, которую поставщик внешних поставщиков обеспечивает доступ к записи.
    
 _lpMAPIPropSibling_
  
> Зарезервировано; должно быть NULL.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Процесс привязки был успешным.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Поставщик внешней адресной книги не существует.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::OpenTemplateID** реализован только для объектов поддержки поставщика адресной книги. **OpenTemplateID** вызвано только поставщиками адресных книг, которые могут выступать в качестве хостов для записей, принадлежащих другим поставщикам адресных книг, также называемым внешних поставщиков. Поставщики услуг хоста **звонят openTemplateID** для открытия внешней записи, которая возникает, когда данные в поставщике хоста привязаны к коду во внешнем поставщике. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызовите **OpenTemplateID** только в том случае, если поддерживается хранение записей с идентификаторами шаблонов от поставщиков внешних адресных книг. Такая поддержка предъявляет дополнительные требования к реализациям [IABContainer::CreateEntry](iabcontainer-createentry.md) и [IABLogon::OpenEntry.](iablogon-openentry.md) Дополнительные сведения см. в описании этих методов и действия [в качестве поставщика адресной книги для хост-адресов.](acting-as-a-host-address-book-provider.md)
  
Если вызов **OpenTemplateID** возвращает в качестве привязанного интерфейса ту же реализацию объекта свойства, которую вы передали, вы можете освободить ссылку на объект свойства. Это вызвано тем, что внешние поставщики вызвали метод **AddRef** объекта, чтобы сохранить собственную ссылку. Если внешнему поставщику не нужно сохранять ссылку на объект свойства, **OpenTemplateID** возвращает объект свойства unbound. 
  
Если **сбой OpenTemplateID** MAPI_E_UNKNOWN_ENTRYID, попробуйте продолжить, обрабатывая запись как доступную только для чтения. 
  
## <a name="see-also"></a>См. также



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)
  
[Каноническое свойство PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

