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
ms.openlocfilehash: 619357a608dd160cbe4811cc7db7ae3b392db858
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576892"
---
# <a name="imslogonopenentry"></a>IMSLogon::OpenEntry

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает папку или объект сообщения и возвращает указатель на объект для дальнейшего доступа. 
  
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
  
> [in] Размер в байтах, идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на адрес идентификатор записи объекта папки или сообщения, чтобы открыть. 
    
 _lpInterface_
  
> [in] Указатель на интерфейс идентификатор (ИД интерфейса) для объекта. Передача NULL означает, что объект приводится стандартный интерфейс для таких объектов. Параметр _lpInterface_ можно также назначается идентификатор соответствующий интерфейс для объекта. 
    
 _ulOpenFlags_
  
> [in] Битовая маска флаги, который определяет способ открытия объекта. Можно задать следующие флажки:
    
MAPI_BEST_ACCESS 
  
> Объект должен быть открыт максимального разрешения для пользователя и разрешения максимальное клиентского приложения. Например если клиент имеет разрешение на чтение и запись, объект открывается с разрешение на чтение и запись. Если клиент имеет разрешение только на чтение, объект открыт с разрешением только для чтения. Уровень разрешений можно получить путем получения свойство **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
    
MAPI_DEFERRED_ERRORS 
  
> Разрешено для успешного выполнения даже в том случае, если базовый объект недоступен вызывающему приложению. Если объект недоступен, следующий вызов объекта может возвращает ошибку.
    
MAPI_MODIFY 
  
> Запросы на разрешение чтения и записи. По умолчанию объекты создаются с разрешением только для чтения, и клиенты не должны работать предполагается, что чтение и запись, назначено разрешение. 
    
 _lpulObjType_
  
> [out] Указатель на тип объекта открыт.
    
 _lppUnk_
  
> [out] Указатель на указатель на объект открыт.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

MAPI вызывает метод **IMSLogon::OpenEntry** , чтобы открыть папку или сообщение в хранилище сообщений. Идентификатор записи объекта, чтобы открыть передает MAPI. Поставщик хранения сообщений должен возвращать указатель, который позволяет дальнейший доступ к объекту, указанный в параметре _lppUnk_ . 
  
Прежде чем MAPI вызывает **IMSLogon::OpenEntry**, сначала определяет, что данное сообщение или идентификатор записи папки соответствует одной зарегистрированные этим поставщиком хранилища сообщений. Дополнительные сведения о как зарегистрировать поставщиков хранилища идентификаторы записей можно [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).
  
 **IMSLogon::OpenEntry** идентичен методу [IMsgStore::OpenEntry](imsgstore-openentry.md) объекта хранилища сообщений, за исключением того, что клиент не вызывает **IMSLogon::OpenEntry**; MAPI вызывает **IMSLogon::OpenEntry** при обработке методом **IMAPISession::OpenEntry** . Будет открыто с помощью **IMSLogon::OpenEntry** объекты обрабатываются точно так же, как объекты открыто с помощью сообщения хранилищ объекта; в частности объектов открыто с помощью этого вызова должна недействительным после выхода объектов хранилища сообщений. 
  
## <a name="see-also"></a>См. также



[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

