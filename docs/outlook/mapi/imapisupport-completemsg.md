---
title: имаписуппорткомплетемсг
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompleteMsg
api_type:
- COM
ms.assetid: e7932433-abe0-4341-95e0-91b37c848145
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e8c52d71ee47966be09c6c0806eceafae0c5ff5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411192"
---
# <a name="imapisupportcompletemsg"></a>IMAPISupport::CompleteMsg

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Выполняет обработку сообщения. 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _кбентрид_
  
> возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ . 
    
 _лпентрид_
  
> возврата Указатель на идентификатор записи для обработки сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Пошаговая обработка выполнена успешно.
    
## <a name="remarks"></a>Примечания

Метод **имаписуппорт:: комплетемсг** реализован для объектов поддержки поставщика хранилища сообщений и вызывается только поставщиками хранилищ сообщений, тесно связанными с поставщиками транспорта. Тесно связанные поставщики магазинов вызывают **имаписуппорт:: комплетемсг** , чтобы указать, что диспетчер очереди MAPI должен обработать сообщение. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Call **комплетемсг** только в том случае, если у вас тесно связаны с поставщиком транспорта, вы можете обрабатывать всех получателей сообщения и одно из следующих условий: 
  
- Сообщение было предварительно обработано.
    
- Для сообщения требуется обработка с помощью диспетчера очереди MAPI.
    
## <a name="see-also"></a>См. также



[IMAPISupport: IUnknown](imapisupportiunknown.md)

