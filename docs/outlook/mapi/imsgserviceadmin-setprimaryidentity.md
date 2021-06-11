---
title: IMsgServiceAdminSetPrimaryIdentity
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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Назначает службу сообщений поставщиком основного удостоверения для профиля.
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a>Parameters

 _lpUID_
  
> [in] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор для службы сообщений для поставки основного удостоверения, или NULL, что указывает на то, что **setPrimaryIdentity** должен очистить текущее удостоверение. 
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Службе сообщений успешно назначен поставщик основного удостоверения.
    
MAPI_E_NO_ACCESS 
  
> **SetPrimaryIdentity** попытался назначить службу сообщений с SERVICE_NO_PRIMARY_IDENTITY флагом в свойстве **PR_RESOURCE_FLAGS** [(PidTagResourceFlags).](pidtagresourceflags-canonical-property.md)
    
## <a name="remarks"></a>Примечания

Метод **IMsgServiceAdmin::SetPrimaryIdentity** устанавливает службу сообщений в качестве поставщика основного удостоверения для профиля. Основным удостоверением обычно является пользователь, который вошел в службу сообщений. Он представлен тремя свойствами: 
  
- **PR_IDENTITY_DISPLAY** [(PidTagIdentityDisplay)](pidtagidentitydisplay-canonical-property.md)
    
- **PR_IDENTITY_ENTRYID** [(PidTagIdentityEntryId)](pidtagidentityentryid-canonical-property.md)
    
- **PR_IDENTITY_SEARCH_KEY** [(PidTagIdentitySearchKey)](pidtagidentitysearchkey-canonical-property.md)
    
Каждый поставщик услуг в назначенной службе сообщений задает эти три свойства для имени отображения, идентификатора входа и ключа поиска пользователя обмена сообщениями, который поставляет основные удостоверения. Клиенты могут получить идентификатор входа основного удостоверения, позвонив [по методу IMAPISession::QueryIdentity.](imapisession-queryidentity.md) 
  
Свойство **PR_RESOURCE_FLAGS,** которое STATUS_PRIMARY_IDENTITY для каждого поставщика, который является членом службы сообщений, которая поставляет основные удостоверения, и SERVICE_PRIMARY_IDENTITY для службы сообщений. Если поставщик услуг не может предоставить основное удостоверение для службы сообщений, он **задает** PR_RESOURCE_FLAGS STATUS_NO_PRIMARY_IDENTITY. **SetPrimaryIdentity** задает PR_RESOURCE_FLAGS **каждой** службы сообщений, которая не поставляет основной идентификатор SERVICE_NO_PRIMARY_IDENTITY. 
  
Каждый поставщик службы сообщений, о которых имеется информация MAPI, может установить удостоверение для каждого из своих пользователей при входе клиента в службу. Однако, поскольку MAPI поддерживает подключения к нескольким поставщикам услуг для каждого сеанса MAPI, нет четкого определения удостоверения конкретного пользователя для сеанса MAPI в целом; удостоверение пользователя зависит от того, какая служба задействована. Клиенты могут вызвать **setPrimaryIdentity,** чтобы назначить одну из множества удостоверений, установленных для пользователя службами сообщений в качестве основного удостоверения для этого пользователя. 
  
## <a name="see-also"></a>См. также



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

