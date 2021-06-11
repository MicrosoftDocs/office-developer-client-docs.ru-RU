---
title: IMSLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenEntry
api_type:
- COM
ms.assetid: 612cbab7-60cb-48bb-906e-18d9135e7a86
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 544aaaace18a9d26972e6484803b63a1ee7060fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416302"
---
# <a name="imslogonopenentry"></a>IMSLogon::OpenEntry

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает папку или объект сообщения и возвращает указатель на объект, чтобы обеспечить дополнительный доступ. 
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulOpenFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in] Размер в bytes идентификатора записи, на который указывает _параметр lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на адрес открываемого идентификатора папки или объекта сообщения. 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID) для объекта. Передача NULL указывает на то, что объект отбрасывается в стандартный интерфейс для такого объекта. Параметр  _lpInterface_ также может быть задан идентификатору для соответствующего интерфейса объекта. 
    
 _ulOpenFlags_
  
> [in] Битмашка флагов, контролируемая тем, как открывается объект. Можно установить следующие флаги:
    
MAPI_BEST_ACCESS 
  
> Объект должен быть открыт с максимальным разрешением, разрешенным для пользователя, и с максимальным разрешением клиентского приложения. Например, если у клиента есть разрешение на чтение и записи, объект открывается с разрешения на чтение и записи; если у клиента есть разрешение только для чтения, объект открывается только для чтения. Клиент может получить уровень разрешений, получив **свойство PR_ACCESS_LEVEL** [(PidTagAccessLevel).](pidtagaccesslevel-canonical-property.md)
    
MAPI_DEFERRED_ERRORS 
  
> Вызов может быть успешным, даже если его объект недодоступн для вызываемой заявки. Если объект не доступен, последующий вызов объекта может привести к ошибке.
    
MAPI_MODIFY 
  
> Запросы на чтение и написание разрешений. По умолчанию объекты создаются с разрешения только для чтения, и клиенты не должны работать на предположении, что разрешение на чтение и записи было предоставлено. 
    
 _lpulObjType_
  
> [вышел] Указатель на тип открываемого объекта.
    
 _lppUnk_
  
> [вышел] Указатель на указатель на открытый объект.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

MAPI вызывает **метод IMSLogon::OpenEntry,** чтобы открыть папку или сообщение в хранилище сообщений. MAPI передает в идентификатор входа открываемого объекта. Поставщик магазина сообщений должен вернуть указатель, который позволяет получить дополнительный доступ к объекту, указанному в параметре _lppUnk._ 
  
Прежде чем MAPI вызывает **IMSLogon::OpenEntry,** сначала определяет, что данный идентификатор записи сообщения или папки совпадает с идентификатором, зарегистрированным поставщиком этого магазина сообщений. Дополнительные сведения о том, как поставщики магазинов регистрируют идентификаторы входа, см. в документе [IMAPISupport::SetProviderUID.](imapisupport-setprovideruid.md)
  
 **IMSLogon::OpenEntry** идентична методу [IMsgStore::OpenEntry](imsgstore-openentry.md) объекта магазина сообщений, за исключением того, что клиент не называет **IMSLogon::OpenEntry;** MAPI вызывает **IMSLogon::OpenEntry** при обработке **метода IMAPISession::OpenEntry.** Объекты, открытые с помощью **IMSLogon::OpenEntry,** должны рассматриваться точно так же, как объекты, открытые с помощью объекта магазина сообщений; в частности, объекты, открытые с помощью этого вызова, должны быть признаны недействительными при отображении объекта магазина сообщений. 
  
## <a name="see-also"></a>См. также



[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

