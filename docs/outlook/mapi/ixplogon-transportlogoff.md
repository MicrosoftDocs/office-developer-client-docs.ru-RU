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
ms.openlocfilehash: 761228a01e0dc778b962c62436e872ff20d72088
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586314"
---
# <a name="ixplogontransportlogoff"></a>IXPLogon::TransportLogoff

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Запускает процесс выхода из системы. 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов успешно и возвращается ожидаемым значением или значения. Если что-либо других значение S_OK возвращается поставщик выход.
    
## <a name="remarks"></a>Замечания

Диспетчер очереди MAPI вызывает метод **IXPLogon::TransportLogoff** , чтобы завершить сеанс поставщика транспорта для определенного пользователя. До вызова метода **TransportLogoff**, диспетчер очереди MAPI удаляет все данные о поддерживаемых типов адреса обмена сообщениями для данного сеанса, переданной в метод [IXPLogon::AddressTypes](ixplogon-addresstypes.md) . 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщика транспорта должно быть готово для принятия вызова **TransportLogoff** в любое время. Если сообщение не в процессе, поставщик должен остановить процесс отправки. 
  
Поставщика транспорта освобождать все ресурсы, выделенные для текущего сеанса. Если он выделенной памяти для данного сеанса с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) , он должен освободить память с помощью функции [MAPIFreeBuffer](mapifreebuffer.md) . Памяти, выделенной поставщика транспорта для удовлетворения вызовы метода [IXPLogon::AddressTypes](ixplogon-addresstypes.md) может безопасно снята в данный момент. 
  
Как правило на завершение вызова **TransportLogoff** поставщика следует сначала объявить недействительным возвращается объект входа путем вызова метода [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) и затем выпуска возвращается объект поддержки. Реализация поставщика из **TransportLogoff** должен освободить объект поддержки и, наконец, так как после выхода объекта поддержки, диспетчер очереди MAPI может быть выпущен сам объект поставщика. 
  
## <a name="see-also"></a>См. также



[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

