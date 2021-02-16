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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Добавляет нового получателя непосредственно в контейнер адресной книги или в список получателей исходяного сообщения.
  
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

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Handle to the parent window of the dialog box.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _cbEIDContainer_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEIDContainer._ 
    
 _lpEIDContainer_
  
> [in] Указатель на идентификатор записи контейнера для получения новой записи. Если _cbEIDContainer_ имеет 0, а _lpEIDContainer_ — NULL, **NewEntry** создает идентификатор одноразрядной записи, который имеет тот же тип, что и при вызове метода [IMAPISupport::CreateOneOff.](imapisupport-createoneoff.md) 
    
 _cbEIDNewEntryTpl_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEIDNewEntryTpl._ 
    
 _lpEIDNewEntryTpl_
  
> [in] Указатель на идентификатор записи шаблона, который будет использоваться для создания новой записи. Если  _cbEIDNewEntryTpl_ имеет 0, а  _lpEIDNewEntryTpl_ — NULL, **NewEntry** отображает диалоговое окно, которое позволяет пользователю выбирать из списка шаблонов для добавления новых записей. 
    
 _lpcbEIDNewEntry_
  
> [out] Указатель на количество byte в идентификаторе записи, на который указывает параметр _lppEIDNewEntry._ 
    
 _lppEIDNewEntry_
  
> [out] Указатель на указатель на идентификатор записи только что созданной записи.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Новая запись успешно создана.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::NewEntry** реализован для объектов поддержки поставщика адресной книги. Поставщики адресных книг **звонят NewEntry,** чтобы создать новую запись адресной книги, которая будет добавлена непосредственно в контейнер или будет использоваться для адресов исходяния сообщения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если вы хотите добавить новую запись в определенный контейнер, задайте  _для lpEIDContainer_ идентификатор записи контейнера, а  _cbEIDContainer_ для подсчета в идентификаторе записи. 
  
Если вы хотите, чтобы новая запись была добавлена в список получателей исходячего сообщения, установите  _для lpEIDContainer_ nULL, а  _для cbEIDContainer_ – 0. 
  
Если вы хотите разрешить пользователю клиентского приложения выбирать тип создаемой записи, передайте 0 в  _cbEIDNewEntryTpl_ и NULL в  _lpEIDNewEntryTpl_. **NewEntry** отображает одностолевую таблицу MAPI , список шаблонов, которые MAPI и каждый из поставщиков адресных книг в поддержке сеанса. Каждый шаблон может создать запись получателя для одного или более типов адресов. 
  
Если вы хотите сохранить идентификатор записи новой записи, передав допустимые указатели в параметрах _lpcbEIDNewEntry_ и _lppEIDNewEntry._ После завершения работы с этим идентификатором вы несете ответственность за его освобождение путем вызова функции [MAPIFreeBuffer.](mapifreebuffer.md) 
  
Чтобы использовать определенный шаблон для добавления новой записи в измояемый контейнер, используйте следующую процедуру:
  
1. Вызовите метод [IMAPISupport::OpenEntry,](imapisupport-openentry.md) чтобы открыть контейнер назначения, и установите для параметра  _lpEntryID_ идентификатор записи контейнера. 
    
2. Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера назначения и установите для параметра  _ulPropTag_ PR_CREATE_TEMPLATES **(** [PidTagCreateTemplates),](pidtagcreatetemplates-canonical-property.md)а для параметра  _lpiid_ — IID_IMAPITable. Контейнер возвращает одностолевую таблицу со списком всех шаблонов, которые он поддерживает для создания новых записей. 
    
3. Извлекает строку, представляюную шаблон для определенного типа записи, которую необходимо создать. Столбец **PR_ADDRTYPE** ([PidTagAddressType)](pidtagaddresstype-canonical-property.md)указывает тип адреса, поддерживаемый шаблоном. 
    
4. Вызовите **IMAPISupport::NewEntry** и установите для параметра  _lpEIDNewEntryTpl_ идентификатор записи выбранного шаблона. Идентификатором записи является столбец **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)из строки шаблона в одноразовой таблице. Передав 0 в _cbEIDContainer_ и NULL в _lpEIDContainer._ Передав допустимый указатель в  _параметре lppEIDNewEntry,_ если необходимо сохранить идентификатор записи новой записи. 
    
## <a name="see-also"></a>См. также



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport::OpenEntry](imapisupport-openentry.md)
  
[Каноническое свойство PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

