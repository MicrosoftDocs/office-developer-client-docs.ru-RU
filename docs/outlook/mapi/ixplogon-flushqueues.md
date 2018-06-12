---
title: IXPLogonFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.FlushQueues
api_type:
- COM
ms.assetid: c1f630c6-9e95-49c0-9757-4685c98184dc
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 116e3cfaace9c0965001021575b76ec371667877
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809631"
---
# <a name="ixplogonflushqueues"></a>IXPLogon::FlushQueues

  
  
**Применимо к**: Outlook 
  
Запросы, что поставщик транспорта сразу же доставить все ожидающие входящих или исходящих сообщений.
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Дескриптор родительского окна все диалоговые окна или окна, которые отображаются этот метод.
    
 _cbTargetTransport_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpTargetTransport_
  
> [in] Зарезервировано; должен иметь значение NULL.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, каким образом осуществляется очистки очереди сообщений. Можно задать следующие флажки:
    
FLUSH_DOWNLOAD 
  
> Входящее сообщение или несколько очередей, должны быть очищены.
    
FLUSH_FORCE 
  
> Поставщика транспорта должен обработать этот запрос, если это возможно, даже в том случае, если это много времени. 
    
FLUSH_NO_UI 
  
> Поставщика транспорта не должно отображать пользовательский интерфейс.
    
FLUSH_UPLOAD 
  
> Исходящие сообщения или несколько очередей, должны быть очищены.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов успешно и возвращается ожидаемым значением или значения.
    
## <a name="remarks"></a>Замечания

Диспетчер очереди MAPI вызывает метод **IXPLogon::FlushQueues** рекомендация по использованию поставщика транспорта, что диспетчер очереди MAPI — начать обработку сообщений. Поставщика транспорта необходимо вызвать метод [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) Установка соответствующий бит для ее состояния в свойстве **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) его строке состояния. После обновления его строки состояния, поставщика транспорта должен возвращать значение S_OK для вызова **FlushQueues** . Диспетчер очереди MAPI начинает отправку сообщения, с помощью операции, синхронные диспетчер очереди MAPI. 
  
Для поддержки его реализация метода [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) , диспетчер очереди MAPI вызывает **IXPLogon::FlushQueues** для всех объектов входа в систему для поставщиков активный перенос, на которых выполняется в рамках сеанса профилей. При вызове метода **FlushQueues** поставщика транспорта из-за вызов клиентского приложения **IMAPIStatus::FlushQueues**обработки сообщений происходит асинхронно клиенту.
  
## <a name="see-also"></a>См. также



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon: IUnknown](ixplogoniunknown.md)

