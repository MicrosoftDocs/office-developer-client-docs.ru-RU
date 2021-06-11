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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает запись получателя в иностранном поставщике адресной книги.
  
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

## <a name="parameters"></a>Parameters

 _cbTemplateID_
  
> [in] Количество byte в идентификаторе шаблона, на который указывает _lpTemplateID._ 
    
 _lpTemplateID_
  
> [in] Указатель на свойство идентификатора **шаблона PR_TEMPLATEID** [(PidTagTemplateid)](pidtagtemplateid-canonical-property.md)для открываемой записи получателя.
    
 _ulTemplateFlags_
  
> [in] Битмашка флагов, используемых для описания открытия записи. Можно установить следующий флаг:
    
FILL_ENTRY 
  
> Создается новая запись. Когда иностранный поставщик получает последующий вызов [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) из MAPI, он может управлять тем, как создается запись, изменяя свойства, на которые указывает параметр  _lpMAPIPropData,_ или возвращая определенную реализацию интерфейса  _в lppMAPIPropNew,_ чтобы контролировать, как заданы свойства для новой записи. 
    
 _lpMAPIPropData_
  
> [in] Указатель на реализацию интерфейса, который звонивка использует для доступа к записи. Это реализация, которую иностранный поставщик может обернуть с собственной реализацией и вернуть в _параметре lppMAPIPropNew._ Параметр _lpMAPIPropData_ должен указать на реализацию интерфейса чтения и записи, которая вытекает из [IMAPIProp: IUnknown](imapipropiunknown.md) и поддерживает запрашиваемого интерфейса в параметре _lpInterface._ 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к записи. Параметр _lppMAPIPropNew_ указывает на интерфейс типа, указанного _lpInterface._ Передача NULL возвращает стандартный интерфейс для пользователя обмена сообщениями, IID_IMailUser. 
    
 _lppMAPIPropNew_
  
> [вышел] Указатель на реализацию интерфейса, который иностранный поставщик поставляет для доступа к записи.
    
 _lpMAPIPropSibling_
  
> Зарезервировано; должно быть NULL.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Процесс привязки был успешным.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Иностранного поставщика адресных книг не существует.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::OpenTemplateID** реализован только для объектов поддержки поставщика адресных книг. **OpenTemplateID** называется только поставщиками адресных книг, которые могут выступать в качестве хостов для записей, принадлежащих другим поставщикам адресной книги, также известным как иностранные поставщики. Поставщики хостов звонят **в OpenTemplateID** для открытия иностранной записи, которая возникает, когда данные в принимающем поставщике обязаны кодироваться в иностранном поставщике. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызов **OpenTemplateID только** в том случае, если вы поддерживаете хранение записей с идентификаторами шаблонов от иностранных поставщиков адресных книг. Такая поддержка предъявляет дополнительные требования к реализации [IABContainer::CreateEntry](iabcontainer-createentry.md) и [IABLogon::OpenEntry.](iablogon-openentry.md) Дополнительные сведения см. в описании этих методов и в качестве поставщика [адресной книги для хостов.](acting-as-a-host-address-book-provider.md)
  
Если вызов **OpenTemplateID** возвращается в качестве связанного интерфейса той же реализации объекта свойства, в которую вы прошли, вы можете освободить ссылку на объект свойства. Это вызвано тем, что иностранный поставщик вызвал метод **AddRef** объекта для сохраняемой ссылки. Если иностранному поставщику не требуется сохранять ссылку на объект свойства, **openTemplateID** возвращает объект неограниченного свойства. 
  
Если **openTemplateID** не удается с MAPI_E_UNKNOWN_ENTRYID, попробуйте продолжить, обрабатывая запись только для чтения. 
  
## <a name="see-also"></a>См. также



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)
  
[Каноническое свойство PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

