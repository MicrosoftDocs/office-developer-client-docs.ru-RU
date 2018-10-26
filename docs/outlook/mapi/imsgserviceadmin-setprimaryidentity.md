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
ms.openlocfilehash: 92807cb216e8a7f4eef6b4d95a8d12826b176e6e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564670"
---
# <a name="imsgserviceadminsetprimaryidentity"></a>IMsgServiceAdmin::SetPrimaryIdentity

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Назначает службы сообщений быть поставщика основной идентификатор профиля.
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a>Параметры

 _lpUID_
  
> [in] Указатель на структуру [MAPIUID](mapiuid.md) , который содержит уникальный идентификатор для службы сообщений для предоставления основной идентификатор или значение NULL, это означает, что **SetPrimaryIdentity** , необходимо очистить удостоверения текущего. 
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Служба сообщений успешно назначен поставщик основного удостоверения.
    
MAPI_E_NO_ACCESS 
  
> **SetPrimaryIdentity** предпринята попытка указать службы сообщений, которая имеет флаг SERVICE_NO_PRIMARY_IDENTITY в своем свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
## <a name="remarks"></a>Замечания

Метод **IMsgServiceAdmin::SetPrimaryIdentity** устанавливает службы сообщений в качестве поставщика основной идентификатор профиля. Основной идентификатор обычно имеет пользователя, выполнившего вход в службу сообщений. Они представляют три свойства: 
  
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))
    
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))
    
Каждые поставщика услуг в службе назначенного сообщения задает эти три свойства отображаемое имя, идентификатор записи и ключа поиска сообщений пользователя, который предоставляет основного удостоверения. Клиенты могут принимать идентификатор записи основной идентификатор путем вызова метода [IMAPISession::QueryIdentity](imapisession-queryidentity.md) . 
  
Свойство **PR_RESOURCE_FLAGS** имеет значение STATUS_PRIMARY_IDENTITY для каждого поставщика, который является членом службы сообщений, которая предоставляет основного удостоверения и SERVICE_PRIMARY_IDENTITY для службы сообщений. Если поставщик службы нельзя указывать основного удостоверения для его службы сообщений, STATUS_NO_PRIMARY_IDENTITY устанавливает **PR_RESOURCE_FLAGS** . **SetPrimaryIdentity** задает свойство **PR_RESOURCE_FLAGS** каждой службы сообщений, не предоставляющий основной идентификатор для SERVICE_NO_PRIMARY_IDENTITY. 
  
Каждый поставщик услуг сообщение со сведениями о MAPI могут устанавливать удостоверение для каждого из пользователей при входе клиента в службу. Тем не менее так как MAPI поддерживает соединения с несколькими поставщиками услуг для каждого сеанса MAPI, нет нет утвержденных определения удостоверение конкретного пользователя для сеанса MAPI как на единое целое; удостоверения пользователя зависит от того, какие службы участвует. Клиенты могут вызывать **SetPrimaryIdentity** назначение одного из многих удостоверений, установленные для пользователя службы сообщений как основной идентификатор для этого пользователя. 
  
## <a name="see-also"></a>См. также



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

