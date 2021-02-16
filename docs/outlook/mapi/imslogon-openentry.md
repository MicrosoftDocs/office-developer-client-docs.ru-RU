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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает папку или объект сообщения и возвращает указатель на объект для обеспечения дальнейшего доступа. 
  
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

## <a name="parameters"></a>Параметры

 _cbEntryID_
  
> [in] Размер идентификатора записи в вайтах, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на адрес идентификатора записи открываемой папки или объекта сообщения. 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID) для объекта. Передача NULL означает, что объект передается в стандартный интерфейс для такого объекта. Параметр  _lpInterface_ также может быть задан в качестве идентификатора для соответствующего интерфейса объекта. 
    
 _ulOpenFlags_
  
> [in] Битоваяmas флагов, которая управляет открытием объекта. Можно установить следующие флаги:
    
MAPI_BEST_ACCESS 
  
> Объект должен быть открыт с максимальным количеством разрешений, разрешенных для пользователя, и максимальным разрешением клиентского приложения. Например, если у клиента есть разрешение на чтение и записи, объект открывается с разрешением на чтение и записи; если у клиента есть разрешение только для чтения, объект открывается с разрешением только для чтения. Клиент может получить уровень разрешений, получив **свойство PR_ACCESS_LEVEL** ([PidTagAccessLevel).](pidtagaccesslevel-canonical-property.md)
    
MAPI_DEFERRED_ERRORS 
  
> Вызов может быть успешным даже в том случае, если его объект недопустим для вызываемой программы. Если объект не доступен, последующий вызов объекта может вернуть ошибку.
    
MAPI_MODIFY 
  
> Запрашивает разрешение на чтение и записи. По умолчанию объекты создаются с разрешением только для чтения, и клиенты не должны работать при предположении, что разрешение на чтение и записи было предоставлено. 
    
 _lpulObjType_
  
> [out] Указатель на тип открытого объекта.
    
 _lppUnk_
  
> [out] Указатель на указатель на открытый объект.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

MAPI вызывает метод **IMSLogon::OpenEntry,** чтобы открыть папку или сообщение в хранилище сообщений. MAPI передает идентификатор записи объекта для открытия. Поставщик параметров хранения сообщений должен вернуть указатель, который обеспечивает дальнейший доступ к объекту, указанному в параметре _lppUnk._ 
  
Перед вызовом **СЛУЖБЫ MAPI IMSLogon::OpenEntry** сначала определяется, что заданный идентификатор записи сообщения или папки соответствует идентификатору, зарегистрированного этим поставщиком. Дополнительные сведения о регистрации идентификаторов записей поставщиками магазина см. в документе [IMAPISupport::SetProviderUID.](imapisupport-setprovideruid.md)
  
 **IMSLogon::OpenEntry** идентичен методу [IMsgStore::OpenEntry](imsgstore-openentry.md) объекта хранилище сообщений, за исключением того, что клиент не вызвать **IMSLogon::OpenEntry;** MAPI вызывает **IMSLogon::OpenEntry** при обработке метода **IMAPISession::OpenEntry.** Объекты, открытые с помощью **IMSLogon::OpenEntry,** должны рассматриваться точно так же, как объекты, открытые с помощью объекта хранения сообщений; в частности, объекты, открытые с помощью этого вызова, должны быть признаны недействительными при освобождения объекта хранения сообщений. 
  
## <a name="see-also"></a>См. также



[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

