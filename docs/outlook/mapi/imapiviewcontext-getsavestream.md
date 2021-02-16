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
ms.openlocfilehash: 68eb74f53d6cee4661c98604ec2ea37609e20ab5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408427"
---
# <a name="imapiviewcontextgetsavestream"></a>IMAPIViewContext::GetSaveStream

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Извлекает поток, который будет использоваться для сохранения текущего сообщения.
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a>Параметры

 _pulFlags_
  
> [out] Указатель на битовуюметку флагов, которая управляет тем, как следует сохранить текст сообщения. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Текст сообщения сохранен в формате Юникод. Если флаг MAPI_UNICODE не установлен, текст будет сохранен в формате ANSI.
    
 _pulFormat_
  
> [out] Указатель на битовуюmask флагов, которая управляет форматом сохраненного текста. Можно установить следующие флаги:
    
SAVE_FORMAT_RICHTEXT 
  
> Текст сообщения должен быть сохранен в формате RTF. 
    
SAVE_FORMAT_TEXT 
  
> Текст сообщения должен быть сохранен в виде обычного текста. 
    
 _ppstm_
  
> [out] Указатель на указатель на поток, который будет содержать сохраненное сообщение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Поток был успешно извлечен.
    
## <a name="remarks"></a>Примечания

Объекты форм вызывают метод **IMAPIViewContext::GetSaveStream,** чтобы получить поток объекта, реализующий **интерфейс IStream** для поддержки обработки команды "Сохранить как" в представлении формы. Метод [IMAPIForm::D oVerb,](imapiform-doverb.md) который реализуется на сервере форм и вызывается просмотром формы для вызова команды, не должен возвращаться, пока сообщение не будет полностью преобразовано в соответствующий текстовый формат и помещено в соответствующий поток. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Не записывай в поток, на который указывает _ppstm,_ перед вызовом **GetSaveStream.** При **возвращении GetSaveStream** не сбрасывать положение указателя поиска. Этот указатель должен оставаться в конце сохраненного текста сообщения. 
  
## <a name="see-also"></a>См. также



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

