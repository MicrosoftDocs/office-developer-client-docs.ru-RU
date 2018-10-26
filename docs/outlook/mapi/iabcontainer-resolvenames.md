---
title: IABContainerResolveNames
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.ResolveNames
api_type:
- COM
ms.assetid: 27474af2-29a2-4cfb-b94f-72eb91562dac
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 81f35f659342d6258d60f40b12bd0a3ac2dc20b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588477"
---
# <a name="iabcontainerresolvenames"></a>IABContainer::ResolveNames

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Выполняет разрешение имен для одного или нескольких получателей записей.
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a>Параметры

 _lpPropTagArray_
  
> [in] Указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит массив тегов свойств, описывающий свойства, которые нужно включить в структуре [ADRLIST](adrlist.md) , возвращенных поставщиком. Чтобы запросить поставщика по умолчанию набор свойств, передайте в параметре _lpPropTagArray_ NULL. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип текста в возвращенных строк. Можно задать следующие флажки:
    
EMS_AB_ADDRESS_LOOKUP
  
> Будет найден только совпадения адрес точное прокси-сервера; Частичный совпадения, игнорируются. Этот флаг поддерживается только поставщик Exchange адресной книги.
    
MAPI_CACHE_ONLY
  
> Автономная адресная книга будет использоваться для выполнения разрешения имен. Например можно использовать этот флаг для включения в клиентское приложение для открытия глобальном списке адресов (GAL) в режиме кэширования данных exchange и доступа к записи в этот список адресов из кэша без создания трафика между клиентом и сервером. Этот флаг поддерживается только поставщик Exchange адресной книги. 
    
MAPI_UNICODE 
  
> Возвращенная строка условий в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
 _lpAdrList_
  
> [in, out] На входе указатель на структуру **ADRLIST** , содержащий список получателей разрешения. На выходе указатель на структуру **ADRLIST** , содержащий возможности разрешения имен. 
    
 _lpFlagList_
  
> [in, out] Указатель на массив флаги, каждый соответствующий на структуру [ADRENTRY](adrentry.md) в параметре _lpAdrList_ флаг, который предоставляет информацию о состоянии операцию разрешения имени для получателя. Флаги в параметре _lpFlagList_ , в том же порядке, как записи в _lpAdrList_. Можно задать следующие флажки:
    
MAPI_AMBIGUOUS 
  
> Была устранена, соответствующего получателю, но не уникальный идентификатор. Другие контейнеры не рекомендуется для устранения этой получателя. 
    
MAPI_RESOLVED 
  
> Уникальный идентификатор проблема устранена соответствующего получателя. Другие контейнеры не рекомендуется для устранения этой получателя. 
    
MAPI_UNRESOLVED 
  
> Запись не разрешен. Другие контейнеры должны пытаться разрешить этому получателю.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Процесс разрешения имен прошла успешно.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.
    
MAPI_E_NO_SUPPORT 
  
> Поставщик адресной книги не поддерживает массовое разрешение имен с помощью этого метода.
    
## <a name="remarks"></a>Замечания

Метод **ResolveNames** пытается сопоставить нерешенные получателей из массива записей с помощью параметра _lpAdrList_ список получателей в этот контейнер адресной книги. Неизвестный получатель обычно имеет только свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) и возможно несколько других свойств. Неизвестный получатель не имеет свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) и его соответствующий флаг в параметре _lpFlagList_ задано значение MAPI_UNRESOLVED. С другой стороны разрешенных получателя всегда имеет по крайней мере **PR_ENTRYID** свойства, а также некоторые другие свойства, такие как **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**и **PR_ADDRTYPE** ([ PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
Разрешение имен обычно запускается, когда клиент вызывает метод [IAddrBook::ResolveName](iaddrbook-resolvename.md) . Outlook MAPI отвечает путем вызова метода **ResolveNames** каждого контейнер адресной книги, включенных в путь поиска книги адрес, указанный в свойстве **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)). Операции с помощью параметра _lpAdrList_ включают получателей, уже разрешить, так как они находятся в контейнеров, для которых MAPI уже вызван **ResolveNames**, так как записи ранее в путь поиска. 
  
Каждый контейнер предпринимается попытка разрешить нерешенные записи соответствующей отображаемое имя получателя, с отображаемым именем одного из его записи. При обнаружении уникальное соответствие **ResolveNames** добавляет свойство **PR_ENTRYID** и других свойств, содержащихся в параметре _lpPropTagArray_ соответствующей записи в структуре исходящей **ADRLIST** . Затем **ResolveNames** задает запись в параметре _lpFlagList_ MAPI_RESOLVED. Идентификатор записи, хранящиеся в свойстве **PR_ENTRYID** может быть Краткосрочные или продолжительные. 
  
В конце концов контейнеров в поиск путь предпринята процесса разрешения имен, MAPI открывает диалоговое окно, если это возможно, чтобы запрашивать у пользователя за помощью в устранении любые оставшиеся. 
  
Клиенты могут также использовать возвращенный структура **ADRLIST** вызовы метода [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Вам не требуется для поддержки разрешение имен с помощью метода **ResolveNames** . Вместо этого, и Кроме того он может поддерживать с ограничением свойство **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Если вы решили зависеть от **PR_ANR** ограничения для разрешения имен, можно вернуть MAPI_E_NO_SUPPORT. For more information, see [���������� ���������� ����](implementing-name-resolution.md).
  
Установите флаг запись получателя в параметре _lpFlagList_ MAPI_UNRESOLVED, если получатель не соответствует контейнер получателей. 
  
Если получателя соответствует нескольким получателям, установить его флаг MAPI_AMBIGUOUS и не изменяйте его структуры **ADRENTRY** . 
  
MAPI требуется определенных свойств для получателей, которые включены в список получателей сообщения. Можно включить их в структуре **ADRENTRY** как часть процесса разрешения имен или дождитесь MAPI запросить их с помощью вызовов методов [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) и [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) . Можно исключить эти дополнительные вызовы и повысить производительность, включая следующие свойства в структуре **ADRENTRY** все возможности разрешения получателей: 
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Некоторые свойства с помощью параметра _lpPropTagArray_ недоступны — обычно поддерживает запись контейнер свойств и они не включаются в член **ADRENTRY** получателя в структуре **ADRLIST** — Задайте тип свойства каждого свойства недоступен для PT_ERROR. 
  
Не удаляйте все свойства из структуры **ADRENTRY** Разрешить получателя. 
  
Если вам необходимо заменить, а не изменять структуру **ADRENTRY** , сведениям исходной структуры **ADRENTRY** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) , а затем распределите замены структура **ADRENTRY** с [ MAPIAllocateBuffer](mapiallocatebuffer.md).
  
## <a name="see-also"></a>См. также



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Каноническое свойство PidTagAnr](pidtaganr-canonical-property.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

