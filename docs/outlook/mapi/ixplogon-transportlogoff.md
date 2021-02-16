---
title: IXPLogonTransportLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportLogoff
api_type:
- COM
ms.assetid: b2b368ce-4486-4f90-985f-59e50ca95229
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 78b4feeca263035b9c90184f10edd294e6cd7b10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417863"
---
# <a name="ixplogontransportlogoff"></a>IXPLogon::TransportLogoff

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Инициирует процесс выйдите из нее. 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и возвратил ожидаемое значение или значения. Если возвращается S_OK, поставщик выключается.
    
## <a name="remarks"></a>Примечания

Пулер MAPI вызывает метод **IXPLogon::TransportLogoff,** чтобы завершить сеанс поставщика транспорта для определенного пользователя. Перед **вызовом TransportLogoff** пулер MAPI удаляет все данные о поддерживаемых типах адресов сообщений для этого сеанса, переданные в [методе IXPLogon::AddressTypes.](ixplogon-addresstypes.md) 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщик транспорта должен быть готов принять вызов **TransportLogoff** в любое время. Если сообщение находится в процессе, поставщик должен остановить процесс отправки. 
  
Поставщик транспорта должен освободить все ресурсы, выделенные для текущего сеанса. Если для этого сеанса выделена память с помощью функции [MAPIAllocateBuffer,](mapiallocatebuffer.md) она должна освободить память с помощью функции [MAPIFreeBuffer.](mapifreebuffer.md) В настоящее время можно безопасно освободить любую память, выделенную поставщиком транспорта для удовлетворения вызовов метода [IXPLogon::AddressTypes.](ixplogon-addresstypes.md) 
  
Обычно при выполнении вызова **TransportLogoff** поставщик должен сначала сделать недействительным свой объект для логотипа, выполнив вызов метода [IMAPISupport::MakeInvalid,](imapisupport-makeinvalid.md) а затем освободить объект поддержки. Реализация **TransportLogoff** поставщика должна освободить последний объект поддержки, так как при выпуске объекта поддержки пул MAPI также может освободить сам объект поставщика. 
  
## <a name="see-also"></a>См. также



[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

