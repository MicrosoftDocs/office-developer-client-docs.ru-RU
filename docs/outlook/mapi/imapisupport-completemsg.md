---
title: IMAPISupportCompleteMsg
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
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: db28d9684f1bb679ce36f99346f4ecc67a1a93e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/21/2018
ms.locfileid: "19809106"
---
# <a name="imapisupportcompletemsg"></a>IMAPISupport::CompleteMsg

  
  
**Применимо к**: Outlook 
  
Выполняет постобработку сообщение. 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _cbEntryID_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи сообщения для обработки.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Постобработку прошла успешно.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::CompleteMsg** реализуется для объектов поддержки поставщика хранилища сообщений и вызывается только у поставщиков хранилища сообщений, которые тесно связаны с поставщиками транспорта. Поставщики тесно связанных хранилища вызовите **IMAPISupport::CompleteMsg** , чтобы указать диспетчер очереди MAPI для postprocess сообщение. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызовите **CompleteMsg** только в том случае, если вы тесно связан с поставщиком транспорта, может обрабатывать всех получателей сообщений и одного из следующих условий: 
  
- Сообщение было предварительной обработки.
    
- Сообщение необходимо постобработку диспетчером очереди MAPI.
    
## <a name="see-also"></a>См. также



[IMAPISupport: IUnknown](imapisupportiunknown.md)

