---
title: IMAPIViewContextGetSaveStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetSaveStream
api_type:
- COM
ms.assetid: 8316bfa1-3077-401f-aa1e-e9492aca12a8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 47ea122fce7969b326dbd48f875696b91de464f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568576"
---
# <a name="imapiviewcontextgetsavestream"></a>IMAPIViewContext::GetSaveStream

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получает поток, в который будет использоваться для сохранения текущего сообщения.
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a>Параметры

 _pulFlags_
  
> [out] Указатель на битовую маску флагов, который определяет, как должны сохраняться текста сообщения. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Текст сообщения сохраняются в формате Юникод. Если флаг MAPI_UNICODE не установлен, текст сохраняется в формате ANSI.
    
 _pulFormat_
  
> [out] Указатель на битовую маску флагов, который управляет формата текста, сохраненного. Можно задать следующие флажки:
    
SAVE_FORMAT_RICHTEXT 
  
> Текст сообщения является сохраняются как форматированный текст в форматированный текст (RTF). 
    
SAVE_FORMAT_TEXT 
  
> Текст сообщения является сохранен в виде обычного текста. 
    
 _ppstm_
  
> [out] Указатель на указатель в поток, который будет содержать сохраненное сообщение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Поток был успешно извлечен.
    
## <a name="remarks"></a>Примечания

Объекты формы вызовите метод **IMAPIViewContext::GetSaveStream** для извлечения потока объект, реализующий интерфейс **IStream** для обработки команды Сохранить как в средстве просмотра формы. Метод [IMAPIForm::DoVerb](imapiform-doverb.md) , который реализован на сервере формы и вызывается средством просмотра формы для вызова команды, не должен возвращать, пока сообщение полностью преобразуется в соответствующий текстовый формат и помещаются в соответствующие потока. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Не записывать в поток, который указывает _ppstm_ до вызова метода **GetSaveStream**. При возврате **GetSaveStream** , не сбрасывает позицию указателя поиска. В этом указатель должен оставаться в конце текста сохраненные сообщения. 
  
## <a name="see-also"></a>См. также



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

