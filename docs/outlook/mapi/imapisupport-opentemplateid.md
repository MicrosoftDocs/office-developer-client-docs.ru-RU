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
ms.openlocfilehash: 855810f7ac3bc1bd433ddd56aba3fe1f938b9559
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575387"
---
# <a name="imapisupportopentemplateid"></a>IMAPISupport::OpenTemplateID

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает запись получателя в поставщик внешнего адресной книги.
  
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
  
> [in] Число байтов в идентификатор шаблона, на который указывает _lpTemplateID_. 
    
 _lpTemplateID_
  
> [in] Указатель на идентификатор шаблона свойство **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) получателей записи для открытия.
    
 _ulTemplateFlags_
  
> [in] Битовая маска флаги, описывается, как открыть запись. Можно задать следующий флаг:
    
FILL_ENTRY 
  
> Создается новая запись. При последующих вызовов [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) получает внешнего поставщика из MAPI, его можно управлять как операция создается путем изменения свойств, на который указывает параметр _lpMAPIPropData_ или возвращением определенного интерфейса Реализация в _lppMAPIPropNew_ для управления, как задать свойства для нового элемента. 
    
 _lpMAPIPropData_
  
> [in] Указатель на реализации интерфейса, используемый вызывающим объектом для доступа к операции. Это реализация, которые могут переносить собственные реализации и возврата в параметре _lppMAPIPropNew_ внешнего поставщика. Параметр _lpMAPIPropData_ должен указывать на реализацию интерфейса чтения и записи, которая является производным от [IMAPIProp: IUnknown](imapipropiunknown.md) и поддерживает интерфейс, запрашиваемый с помощью параметра _lpInterface_ . 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к операции. Параметр _lppMAPIPropNew_ указывает на интерфейс типа, указанного параметром _lpInterface_. Передача NULL Возвращает стандартный интерфейс для обмена сообщениями пользователя IID_IMailUser. 
    
 _lppMAPIPropNew_
  
> [out] Указатель на реализации интерфейса, который предоставляет внешнего поставщика для доступа к операции.
    
 _lpMAPIPropSibling_
  
> Зарезервировано; должен иметь значение NULL.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Процесс привязки прошла успешно.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Поставщик внешних адресной книги не существует.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::OpenTemplateID** применяется только для объектов поддержки поставщик адресной книги. **OpenTemplateID** вызывается только с поставщиками адресных книг, которые могут выступать в качестве узлов для записи, которые принадлежат другим поставщиками адресной книги также известной как внешнего поставщиков. Поставщики узла вызова **OpenTemplateID** Открытие внешнего запись, которая возникает, когда с привязкой к данным в поставщике узла к коду в внешнего поставщика. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызов **OpenTemplateID** только в том случае, если вы поддерживаете хранилища записей с идентификаторами шаблон с поставщиками внешнего адресной книги. Такая поддержка помещает Дополнительные требования к реализации [IABContainer::CreateEntry](iabcontainer-createentry.md) и [IABLogon::OpenEntry](iablogon-openentry.md) . Для получения дополнительных сведений см эти методы и [используется в качестве узла адресной книге](acting-as-a-host-address-book-provider.md).
  
Если звонок **OpenTemplateID** возвращает как привязанной интерфейс же реализация объекта свойство, которое передается в, могут освобождать ссылку на объект свойство. Это называется метод **AddRef** объекта для хранения собственный ссылку внешнего поставщика. Если внешний поставщик не требуется хранить ссылку на объект свойство, **OpenTemplateID** возвращает объект свободной свойств. 
  
В случае сбоя **OpenTemplateID** с MAPI_E_UNKNOWN_ENTRYID продолжать путем обработки записи с доступом только для чтения. 
  
## <a name="see-also"></a>См. также



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)
  
[Каноническое свойство PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

