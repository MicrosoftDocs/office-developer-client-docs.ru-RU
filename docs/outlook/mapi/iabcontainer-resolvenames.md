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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Выполняет разрешение имен для одной или более записей получателей.
  
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
  
> [in] Указатель на структуру [SPropTagArray,](sproptagarray.md) которая содержит массив тегов свойств, описывающих свойства, которые необходимо включить в структуру [ADRLIST,](adrlist.md) возвращаемую поставщиком. Чтобы запросить набор свойств поставщика по умолчанию, передав значение NULL в _параметре lpPropTagArray._ 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом текста в возвращаемой строке. Можно установить следующие флаги:
    
EMS_AB_ADDRESS_LOOKUP
  
> Будут найдены только точные совпадения с прокси-адресом; частичные совпадения игнорируются. Этот флаг поддерживается только поставщиком адресной книги Exchange.
    
MAPI_CACHE_ONLY
  
> Для разрешения имен будет использоваться только автономной адресной книги. Например, этот флаг можно использовать, чтобы клиентские приложения могли открывать глобальный список адресов (GAL) в режиме кэшации обмена и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером. Этот флаг поддерживается только поставщиком адресной книги Exchange. 
    
MAPI_UNICODE 
  
> Возвращенные строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.
    
 _lpAdrList_
  
> [in, out] При вводе указатель на структуру **ADRLIST,** которая содержит список получателей, которые необходимо разрешить. При выходе указатель на структуру **ADRLIST,** которая содержит разрешенные имена. 
    
 _lpFlagList_
  
> [in, out] Указатель на массив флагов, каждый флаг, соответствующий структуре [ADRENTRY](adrentry.md) в параметре  _lpAdrList,_ который предоставляет состояние операции разрешения имен для получателя. Флаги в параметре _lpFlagList_ находятся в том же порядке, что и записи _в списке lpAdrList._ Можно установить следующие флаги:
    
MAPI_AMBIGUOUS 
  
> Соответствующий получатель был разрешен, но не имеет уникального идентификатора записи. Другие контейнеры не должны пытаться разрешить этого получателя. 
    
MAPI_RESOLVED 
  
> Соответствующий получатель был разрешен в уникальный идентификатор записи. Другие контейнеры не должны пытаться разрешить этого получателя. 
    
MAPI_UNRESOLVED 
  
> Соответствующая запись не была разрешена. Другие контейнеры должны попытаться разрешить этого получателя.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Процесс разрешения имен был успешным.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.
    
MAPI_E_NO_SUPPORT 
  
> Поставщик адресной книги не поддерживает массовое разрешение имен с помощью этого метода.
    
## <a name="remarks"></a>Примечания

Метод **ResolveNames** пытается найти невыязвимые получатели из массива записей в параметре  _lpAdrList_ с получателями в этом контейнере адресной книги. Как правило, неразрешенный получатель имеет только свойство **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)и, возможно, несколько других свойств. У неустановленного **получателя** нет свойства PR_ENTRYID ([PidTagEntryId),](pidtagentryid-canonical-property.md)а соответствующему флагу в параметре  _lpFlagList_ задано MAPI_UNRESOLVED. И **наоборот,** у разрешенного получателя всегда есть как минимум свойство **PR_ENTRYID,** а также несколько других свойств, таких как PR_EMAIL_ADDRESS ([PidTagEmailAddress),](pidtagemailaddress-canonical-property.md) **PR_DISPLAY_NAME** и **PR_ADDRTYPE** ([PidTagAddressType).](pidtagaddresstype-canonical-property.md)
  
Разрешение имен обычно начинается, когда клиент вызывает [метод IAddrBook::ResolveName.](iaddrbook-resolvename.md) Outlook MAPI responds by calling the **ResolveNames** method of each address book container included in the address book search path, specified by the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath)](pidtagabsearchpath-canonical-property.md)property. Записи в параметре  _lpAdrList_ включают получателей, уже разрешенных, так как они находятся в контейнерах, для которых MAPI уже называется **ResolveNames**, так как записи отображаются ранее в пути поиска. 
  
Каждый контейнер пытается разрешить не разрешенные записи путем совпадения отображаемого имени получателя с отображаемой именем одной из его записей. При обнаружении уникального совпадения **ResolveNames** добавляет свойство **PR_ENTRYID** и другие свойства, включенные в параметр _lpPropTagArray,_ к соответствующей записи в исходячей структуре **ADRLIST.** **Затем ResolveNames** задает для параметра  _lpFlagList_ запись MAPI_RESOLVED. Идентификатор записи, хранимый в свойстве **PR_ENTRYID,** может быть краткосрочным или долгосрочным. 
  
После того как все контейнеры в пути поиска попытались разрешить имена, MAPI открывает диалоговое окно, если это возможно, чтобы затмить пользователя о помощи в устранении оставшихся конфликтов. 
  
Клиенты также могут использовать возвращенную **структуру ADRLIST** в вызовах метода [IMessage::ModifyRecipients.](imessage-modifyrecipients.md) 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поддержка разрешения имен с помощью метода **ResolveNames** не требуется. Вместо этого или, кроме того, вы можете поддерживать его с помощью ограничения свойства **PR_ANR** ([PidTagAnr).](pidtaganr-canonical-property.md) Если вы решили использовать  ограничение PR_ANR для разрешения имен, вы можете вернуть MAPI_E_NO_SUPPORT. For more information, see [���������� ���������� ����](implementing-name-resolution.md).
  
Установите для записи флага получателя в параметре  _lpFlagList_ MAPI_UNRESOLVED, если получатель не совпадает ни с одним из получателей контейнера. 
  
Если получатель соответствует нескольким получателям, установите для его флага MAPI_AMBIGUOUS и не изменяя его **структуру ADRENTRY.** 
  
MAPI требует определенных свойств для получателей, включенных в список получателей сообщения. Их можно включить в структуру **ADRENTRY** в процессе разрешения имен или дождаться запроса MAPI с вызовами методов [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) и [IMAPISupport::ExpandRecips.](imapisupport-expandrecips.md) Вы можете исключить эти дополнительные вызовы и повысить производительность, включив следующие свойства в структуры **ADRENTRY** всех разрешенных получателей: 
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)
    
- **PR_SEARCH_KEY** ([PidTagSearchKey)](pidtagsearchkey-canonical-property.md)
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName)](pidtagtransmittabledisplayname-canonical-property.md)
    
Если некоторые свойства в параметре  _lpPropTagArray_ недоступны ( как правило, так как запись контейнера не поддерживает свойства и они не включены в **член ADRENTRY** получателя в структуре **ADRLIST),** установите для типа свойства каждого недоступного свойства PT_ERROR. 
  
Не удалять свойства из структуры **ADRENTRY** разрешенного получателя. 
  
Если необходимо заменить, а не изменять структуру **ADRENTRY,** сначала освободите исходную структуру **ADRENTRY,** вызывая функцию [MAPIFreeBuffer,](mapifreebuffer.md) а затем выделите заменяемую структуру **ADRENTRY** с [MAPIAllocateBuffer.](mapiallocatebuffer.md)
  
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

