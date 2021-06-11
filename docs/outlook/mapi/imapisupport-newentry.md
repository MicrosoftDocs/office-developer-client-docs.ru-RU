---
title: IMAPISupportNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewEntry
api_type:
- COM
ms.assetid: 588d002b-8412-4ab9-9757-04ad89e0a6f8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3468e4a92787e440f230d60ab31f37526fe7d5e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405459"
---
# <a name="imapisupportnewentry"></a>IMAPISupport::NewEntry

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Добавляет нового получателя непосредственно в контейнер адресной книги или в список получателей исходя из сообщения.
  
```cpp
HRESULT NewEntry(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cbEIDContainer,
  LPENTRYID lpEIDContainer,
  ULONG cbEIDNewEntryTpl,
  LPENTRYID lpEIDNewEntryTpl,
  ULONG FAR * lpcbEIDNewEntry,
  LPENTRYID FAR * lppEIDNewEntry
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Ручка родительского окна диалогового окна.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _cbEIDContainer_
  
> [in] Количество byte в идентификаторе входа, на который указывает параметр _lpEIDContainer._ 
    
 _lpEIDContainer_
  
> [in] Указатель на идентификатор входа контейнера для получения новой записи. Если _cbEIDContainer_ — 0, а _lpEIDContainer_ — NULL, **NewEntry** создает идентификатор входа, который является таким же типом, что и при вызове метода [IMAPISupport::CreateOneOff.](imapisupport-createoneoff.md) 
    
 _cbEIDNewEntryTpl_
  
> [in] Количество byte в идентификаторе входа, на который указывает параметр _lpEIDNewEntryTpl._ 
    
 _lpEIDNewEntryTpl_
  
> [in] Указатель на идентификатор записи шаблона, который будет использоваться для создания новой записи. Если  _cbEIDNewEntryTpl_ — 0, а  _lpEIDNewEntryTpl_ — NULL, **NewEntry** отображает диалоговое окно, которое позволяет пользователю выбирать из списка шаблонов для добавления новых записей. 
    
 _lpcbEIDNewEntry_
  
> [вышел] Указатель на количество byte в идентификаторе входа, на который указывает параметр _lppEIDNewEntry._ 
    
 _lppEIDNewEntry_
  
> [вышел] Указатель на указатель на идентификатор входа вновь созданной записи.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Новая запись была успешно создана.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::NewEntry** реализован для объектов поддержки поставщиков адресных книг. Поставщики адресных книг звонят **в NewEntry,** чтобы создать новую запись адресной книги, которая будет добавлена непосредственно в контейнер или использоваться для решения исходяющих сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если вы хотите, чтобы новая запись была добавлена в определенный контейнер, установите  _lpEIDContainer_ в идентификатор входа контейнера и  _cbEIDContainer_ к счету byte в идентификаторе записи. 
  
Если вы хотите, чтобы новая запись была добавлена в список получателей исходячего сообщения, установите  _lpEIDContainer_ nULL и  _cbEIDContainer_ до 0. 
  
Если вы хотите разрешить пользователю клиентского приложения выбрать тип создаваемой записи, переведите 0 в  _cbEIDNewEntryTpl_ и NULL в  _lpEIDNewEntryTpl_. **NewEntry** отображает разовую таблицу MAPI , список шаблонов, которые MAPI и каждый из поставщиков адресных книг в поддержке сеанса. Каждый шаблон может создать запись получателя для одного или более типов адресов. 
  
Если вы хотите сохранить идентификатор входа новой записи, передай допустимые указатели в параметрах _lpcbEIDNewEntry_ и _lppEIDNewEntry._ Вы несете ответственность за то, чтобы освободить этот идентификатор записи после его завершения, позвонив в [функцию MAPIFreeBuffer.](mapifreebuffer.md) 
  
Чтобы использовать определенный шаблон для добавления новой записи в модификабельный контейнер, используйте следующую процедуру:
  
1. Чтобы открыть контейнер назначения, вызовите метод [IMAPISupport::OpenEntry](imapisupport-openentry.md) и установите параметр  _lpEntryID_ в идентификатор входа контейнера. 
    
2. Вызов метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера назначения **и** установите параметр _ulPropTag_ PR_CREATE_TEMPLATES [(PidTagCreateTemplates)](pidtagcreatetemplates-canonical-property.md)и параметр _lpiid_ для IID_IMAPITable. Контейнер возвращает разовую таблицу, в которую перечислены все шаблоны, поддерживаемые для создания новых записей. 
    
3. Извлечение строки, которая представляет шаблон для определенного типа записи, которую вы хотите создать. Столбец **PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)указывает тип адреса, поддерживаемый шаблоном. 
    
4. **Вызывай IMAPISupport::NewEntry** и задай параметр _lpEIDNewEntryTpl_ идентификатору входа выбранного шаблона. Идентификатор входа — это **столбец PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)из строки шаблона в разовой таблице. Pass 0 в  _cbEIDContainer_ и NULL в  _lpEIDContainer_. Передай допустимый указатель в  _параметре lppEIDNewEntry,_ если вы хотите сохранить идентификатор записи новой записи. 
    
## <a name="see-also"></a>См. также



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport::OpenEntry](imapisupport-openentry.md)
  
[Каноническое свойство PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

