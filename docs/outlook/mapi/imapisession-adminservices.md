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
ms.openlocfilehash: 850d4d952102e11d11234fa3184b88e280a98c21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809079"
---
# <a name="imapisessionadminservices"></a>IMAPISession::AdminServices

  
  
**Относится к**: Outlook 
  
Возвращает указатель [IMsgServiceAdmin](imsgserviceadminiunknown.md) для внесения изменений в службы сообщений. 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lppServiceAdmin_
  
> [out] Указатель на указатель на объект администрирования службы сообщений.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Указатель на объект администрирования службы сообщение успешно возвращен.
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Метод **IMAPISession::AdminServices** создает объект администрирования службы сообщений, объект, который поддерживает интерфейс **IMsgServiceAdmin** и возвращает указатель. С помощью этого указателя, можно вызвать методы **IMsgServiceAdmin** для измените какие-либо службы сообщений в профиле сеанса. Помните о том, что эти изменения не вступят в силу до следующего сеанса; не зависит от текущего сеанса. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |GetServerName  <br/> |Mfcmapi (en) использует метод **IMAPISession::AdminServices** для доступа к профилю для чтения имя сервера.  <br/> |
   
## <a name="see-also"></a>См. также



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IProfAdmin::AdminServices](iprofadmin-adminservices.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

