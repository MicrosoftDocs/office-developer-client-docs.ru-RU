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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Выполняет постпроцессинг в сообщении. 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameters

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

Метод **IMAPISupport::CompleteMsg** реализуется для объектов поддержки поставщика хранения сообщений и вызван только поставщиками магазинов сообщений, тесно соедиными с поставщиками транспорта. Поставщики магазинов с тесной парой звонят **iMAPISupport::CompleteMsg,** чтобы поручить шпалеру MAPI отправить сообщение. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызов **CompleteMsg** только при тесной связи с поставщиком транспорта можно обрабатывать все получатели сообщения, и существует одно из следующих условий: 
  
- Сообщение было предварительно процесировали.
    
- Сообщение требует постпроцессинга шпалером MAPI.
    
## <a name="see-also"></a>См. также



[IMAPISupport: IUnknown](imapisupportiunknown.md)

