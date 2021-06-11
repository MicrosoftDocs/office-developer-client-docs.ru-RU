---
title: IMAPISessionAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.AdminServices
api_type:
- COM
ms.assetid: 487fab39-5c2c-4e1a-9f90-4da64f5e198b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c639523a02047bf00c378dafd7bc698d7d4e5fff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405907"
---
# <a name="imapisessionadminservices"></a>IMAPISession::AdminServices

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает [указатель IMsgServiceAdmin](imsgserviceadminiunknown.md) для внесения изменений в службы сообщений. 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lppServiceAdmin_
  
> [вышел] Указатель на указатель на объект администрирования службы сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Указатель на объект администрирования службы сообщений был успешно возвращен.
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Метод **IMAPISession::AdminServices** создает объект администрирования службы сообщений, объект, поддерживаючий интерфейс **IMsgServiceAdmin** и возвращая указатель. С помощью этого указателя можно вызвать **методы IMsgServiceAdmin,** чтобы изменить любую из служб сообщений в профиле сеанса. Следует помнить, что эти изменения не вступает в силу до следующего сеанса; текущий сеанс не влияет. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |GetServerName  <br/> |MFCMAPI использует **метод IMAPISession::AdminServices** для доступа к профиле для чтения имени сервера.  <br/> |
   
## <a name="see-also"></a>См. также



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IProfAdmin::AdminServices](iprofadmin-adminservices.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

