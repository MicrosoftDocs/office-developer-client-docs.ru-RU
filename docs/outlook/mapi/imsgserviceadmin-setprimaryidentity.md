---
title: имсгсервицеадминсетпримаридентити
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.SetPrimaryIdentity
api_type:
- COM
ms.assetid: 763cab41-f6f6-4cb0-8cb8-170fdf2a92e6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b237a57dfea020c7bfcb66d49d43428c1f6506c2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430366"
---
# <a name="imsgserviceadminsetprimaryidentity"></a>IMsgServiceAdmin::SetPrimaryIdentity

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Назначает службу сообщений поставщику основного удостоверения для профиля.
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a>Параметры

 _лпуид_
  
> возврата Указатель на структуру [мапиуид](mapiuid.md) , которая содержит уникальный идентификатор для службы сообщений для предоставления основного удостоверения, или значение null, которое указывает на то, что **сетпримаридентити** должен очистить текущее удостоверение. 
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Поставщику службы сообщений успешно назначен поставщик основного удостоверения.
    
MAPI_E_NO_ACCESS 
  
> В **сетпримаридентити** предпринята попытка назначить службу сообщений с установленным флагом SERVICE_NO_PRIMARY_IDENTITY в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
## <a name="remarks"></a>Примечания

Метод **имсгсервицеадмин:: сетпримаридентити** устанавливает службу сообщений в качестве поставщика основного удостоверения для профиля. Обычно основным удостоверением является пользователь, который вошел в службу сообщений. Он представлен тремя свойствами: 
  
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))
    
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))
    
Каждый поставщик услуг в назначенной службе сообщений задает эти три свойства для отображаемого имени, идентификатора записи и ключа поиска пользователя обмена сообщениями, который предоставляет основное удостоверение. Клиенты могут получить идентификатор записи основного идентификатора, вызвав метод [IMAPISession:: куеридентити](imapisession-queryidentity.md) . 
  
Для свойства **PR_RESOURCE_FLAGS** задается значение STATUS_PRIMARY_IDENTITY для каждого поставщика, который является членом службы сообщений, предоставляющей основной идентификатор, и для SERVICE_PRIMARY_IDENTITY для службы сообщений. Если поставщик услуг не может предоставить основной идентификатор для своей службы сообщений, он устанавливает **PR_RESOURCE_FLAGS** в STATUS_NO_PRIMARY_IDENTITY. **Сетпримаридентити** задает свойство **PR_RESOURCE_FLAGS** для каждой службы сообщений, в которой не указывается основной идентификатор SERVICE_NO_PRIMARY_IDENTITY. 
  
Каждый поставщик службы сообщений, сведения о котором имеют MAPI, может установить удостоверение для каждого из пользователей, когда клиент входит в систему службы. Тем не менее, так как MAPI поддерживает подключения к нескольким поставщикам услуг для каждого сеанса MAPI, отсутствует определение удостоверения определенного пользователя для сеанса MAPI в целом; удостоверение пользователя зависит от того, какая служба задействована. Клиенты могут вызывать **сетпримаридентити** для назначения одного из множества удостоверений, установленных для пользователя службами сообщений в качестве основного удостоверения для этого пользователя. 
  
## <a name="see-also"></a>См. также



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

