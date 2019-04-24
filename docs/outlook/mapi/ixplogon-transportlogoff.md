---
title: Иксплогонтранспортлогофф
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351585"
---
# <a name="ixplogontransportlogoff"></a>IXPLogon::TransportLogoff

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Инициирует процесс выхода из системы. 
  
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
  
> Вызов выполнен успешно и вернул ожидаемое значение или значения. Если возвращено значение, отличное от S_OK, то поставщик вышел из системы.
    
## <a name="remarks"></a>Примечания

Диспетчер очереди MAPI вызывает метод **иксплогон:: транспортлогофф** для завершения сеанса поставщика транспорта для определенного пользователя. Перед вызовом **транспортлогофф**Диспетчер очереди MAPI отбрасывает все данные о поддерживаемых типах адресов обмена сообщениями для этого сеанса, переданного в методе [Иксплогон:: аддресстипес](ixplogon-addresstypes.md) . 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщик транспорта должен быть готов к приему вызова **транспортлогофф** в любое время. Если сообщение находится в процессе, поставщик должен остановить процесс отправки. 
  
Поставщик транспорта должен освободить все ресурсы, выделенные для текущего сеанса. Если для этого сеанса выделяется память с помощью функции [мапиаллокатебуффер](mapiallocatebuffer.md) , она должна освободить память с помощью функции [мапифрибуффер](mapifreebuffer.md) . Любая память, выделенная поставщиком транспорта для удовлетворения вызовов метода [иксплогон:: аддресстипес](ixplogon-addresstypes.md) , может быть безопасно выпущена в настоящее время. 
  
Как правило, при завершении вызова **транспортлогофф** поставщик должен сначала сделать его объектом logon, вызвав метод [Имаписуппорт:: макеинвалид](imapisupport-makeinvalid.md) , а затем отпустить его объект поддержки. Реализация поставщика **транспортлогофф** должна освобождать объект поддержки последним, так как при отпускании объекта support Диспетчер очереди MAPI также может освободить сам объект поставщика. 
  
## <a name="see-also"></a>См. также



[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

