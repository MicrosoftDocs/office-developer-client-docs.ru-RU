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
ms.openlocfilehash: fac4978bef94650f85ac3179acd3858602f933ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405816"
---
# <a name="iabcontainerresolvenames"></a>IABContainer::ResolveNames

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Выполняет разрешение имен для одной или более записей получателей.
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a>Parameters

 _lpPropTagArray_
  
> [in] Указатель на структуру [SPropTagArray,](sproptagarray.md) которая содержит массив тегов свойств, описывающих свойства, которые должны быть включены в структуру [ADRLIST,](adrlist.md) возвращаемую поставщиком. Чтобы запросить набор свойств поставщика по умолчанию, передай NULL в _параметре lpPropTagArray._ 
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют тип текста в возвращенных строках. Можно установить следующие флаги:
    
EMS_AB_ADDRESS_LOOKUP
  
> Будут найдены только точные совпадения адресов прокси- адресов; частичные совпадения игнорируются. Этот флаг поддерживается только поставщиком Exchange адресной книги.
    
MAPI_CACHE_ONLY
  
> Для выполнения разрешения имен будет использоваться только офлайн-адресная книга. Например, этот флаг можно использовать для того, чтобы клиентская заявка открывала глобальный адресный список (GAL) в кэшировом режиме обмена и доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером. Этот флаг поддерживается только поставщиком Exchange адресной книги. 
    
MAPI_UNICODE 
  
> Возвращенные свойства строки находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.
    
 _lpAdrList_
  
> [in, out] На входе указатель на структуру **ADRLIST,** содержаную список получателей, которые необходимо устранить. На выходе указатель на структуру **ADRLIST,** содержаную разрешенные имена. 
    
 _lpFlagList_
  
> [in, out] Указатель на массив флагов, каждый флаг, соответствующий структуре [ADRENTRY](adrentry.md) в параметре  _lpAdrList,_ который обеспечивает состояние операции разрешения имен для получателя. Флаги в параметре _lpFlagList_ находятся в том же порядке, что и записи в _lpAdrList._ Можно установить следующие флаги:
    
MAPI_AMBIGUOUS 
  
> Соответствующий получатель был разрешен, но не для уникального идентификатора записи. Другие контейнеры не должны пытаться устранить этого получателя. 
    
MAPI_RESOLVED 
  
> Соответствующий получатель был решен с уникальным идентификатором записи. Другие контейнеры не должны пытаться устранить этого получателя. 
    
MAPI_UNRESOLVED 
  
> Соответствующая запись не разрешена. Другие контейнеры должны попытаться разрешить этот получатель.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Процесс разрешения имен был успешным.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.
    
MAPI_E_NO_SUPPORT 
  
> Поставщик адресных книг не поддерживает массовое разрешение имен с помощью этого метода.
    
## <a name="remarks"></a>Примечания

Метод **ResolveNames** пытается связать неурегулированных получателей из массива записей в параметре  _lpAdrList_ с получателями в этом контейнере адресной книги. Неурегулированный получатель обычно имеет только **свойство PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)и, возможно, несколько других свойств. Неурегулированный получатель не имеет **свойства PR_ENTRYID** [(PidTagEntryId),](pidtagentryid-canonical-property.md)а соответствующий флаг в параметре  _lpFlagList_ задан для MAPI_UNRESOLVED. И наоборот, у разрешенного получателя всегда есть по крайней мере **свойство PR_ENTRYID** плюс несколько других свойств, таких как **PR_EMAIL_ADDRESS** [(PidTagEmailAddress),](pidtagemailaddress-canonical-property.md) **PR_DISPLAY_NAME** и **PR_ADDRTYPE** [(PidTagAddressType).](pidtagaddresstype-canonical-property.md)
  
Разрешение имен обычно начинается, когда клиент вызывает [метод IAddrBook::ResolveName.](iaddrbook-resolvename.md) Outlook MAPI отвечает вызовом метода **ResolveNames** каждого контейнера адресной книги, включенного в путь поиска адресной книги, указанного в свойстве **PR_AB_SEARCH_PATH** [(PidTagAbSearchPath).](pidtagabsearchpath-canonical-property.md) Записи в  _параметре lpAdrList_ включают получателей, уже решенных, поскольку они находятся в контейнерах, для которых MAPI уже называется **ResolveNames,** так как записи отображаются ранее в пути поиска. 
  
Каждый контейнер пытается устранить неурегулированные записи, сообразуя имя отображения получателя с отображаемой именем одной из его записей. При обнаружении уникального совпадения  **ResolveNames** добавляет свойство PR_ENTRYID и другие свойства, включенные в параметр _lpPropTagArray,_ к соответствующей записи в исходячей структуре **ADRLIST.** **Затем ResolveNames** задает запись в параметре  _lpFlagList_ для MAPI_RESOLVED. Идентификатор записи, хранимый в **свойстве PR_ENTRYID,** может быть краткосрочным или долгосрочным. 
  
После того как все контейнеры в пути поиска попытались разрешить имя, MAPI открывает диалоговое окно, по возможности, чтобы подсказать пользователю помощь в разрешении оставшихся конфликтов. 
  
Клиенты также могут использовать возвращенную **структуру ADRLIST** в вызовах к методу [IMessage::ModifyRecipients.](imessage-modifyrecipients.md) 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Не требуется поддерживать разрешение имен методом **ResolveNames.** Вместо этого или дополнительно вы можете поддерживать его с помощью **ограничения** PR_ANR [(PidTagAnr).](pidtaganr-canonical-property.md) Если вы решите полагаться на **ограничение** PR_ANR для разрешения имен, вы можете MAPI_E_NO_SUPPORT. For more information, see [���������� ���������� ����](implementing-name-resolution.md).
  
Установите запись флага получателя в параметре  _lpFlagList_ MAPI_UNRESOLVED, если получатель не совпадает ни с одним из получателей контейнера. 
  
Если получатель соответствует нескольким получателям, установите его флаг MAPI_AMBIGUOUS и не измените структуру **ADRENTRY.** 
  
MAPI требует определенных свойств для получателей, включенных в список получателей сообщения. Их можно включить в структуру **ADRENTRY** в процессе разрешения имен или дождаться, когда MAPI запросит их с вызовами в [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) и [IMAPISupport::ExpandRecips.](imapisupport-expandrecips.md) Эти дополнительные вызовы можно устранить и повысить производительность, включив следующие свойства в **структуры ADRENTRY** всех разрешенных получателей: 
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)
    
- **PR_SEARCH_KEY** [(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)
    
- **PR_TRANSMITABLE_DISPLAY_NAME** [(PidTagTransmittableDisplayName)](pidtagtransmittabledisplayname-canonical-property.md)
    
Если некоторые свойства в параметре  _lpPropTagArray_ недоступны, как правило, из-за того, что запись контейнера не поддерживает свойства и они не включены в член **ADRENTRY** получателя в структуре **ADRLIST,** установите тип свойства каждого недоступного свойства PT_ERROR. 
  
Не удалять свойства из структуры **ADRENTRY** решенного получателя. 
  
Если необходимо заменить, а не изменять структуру **ADRENTRY,** сначала освободите оригинальную структуру **ADRENTRY,** назвав функцию [MAPIFreeBuffer,](mapifreebuffer.md) а затем распределите структуру **ADRENTRY** на [MAPIAllocateBuffer.](mapiallocatebuffer.md)
  
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

