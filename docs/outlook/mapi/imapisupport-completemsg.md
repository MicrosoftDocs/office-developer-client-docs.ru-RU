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
  
Выполняет постобсказку сообщения. 
  
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
    
 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи для обработки сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Послепроцессинг был успешным.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::CompleteMsg** реализован для объектов поддержки поставщика store сообщений и вызван только поставщиками хранения сообщений, тесносвязаными с поставщиками транспорта. Тесносвязаные поставщики магазина звонят по вызову **IMAPISupport::CompleteMsg,** чтобы упредить пулер MAPI выполнить postprocess сообщение. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызовите **CompleteMsg** только при тесной связи с поставщиком транспорта, вы можете обработать всех получателей сообщения и существует одно из следующих условий: 
  
- Сообщение было предварительно обсобрано.
    
- Сообщение требует postprocessing от пула MAPI.
    
## <a name="see-also"></a>См. также



[IMAPISupport: IUnknown](imapisupportiunknown.md)

