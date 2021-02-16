---
title: ITnefOpenTaggedBody
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.OpenTaggedBody
api_type:
- COM
ms.assetid: 70d5b34c-85b3-4d1f-860e-2838947ba428
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 154d6e4a4e333f3a6165c3875bdcd57957ebf70c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348736"
---
# <a name="itnefopentaggedbody"></a>ITnef::OpenTaggedBody

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает интерфейс потока в тексте инкапсулированного сообщения.
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Параметры

 _lpMessage_
  
> [in] Указатель на сообщение, с которым связан поток. Это сообщение не обязательно должно быть тем же сообщением, которое передается при вызове функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx.](opentnefstreamex.md) 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет открытием интерфейса потока. Можно установить следующие флаги:
    
MAPI_CREATE 
  
> Если свойство не существует в текущем сообщении, его следует создать. Если свойство существует, текущие данные в свойстве должны быть заменены данными из потока Transport-Neutral формата инкапсуляции (TNEF). Когда реализация устанавливает флаг MAPI_CREATE, она также должна MAPI_MODIFY флага.
    
MAPI_MODIFY 
  
> Запрашивает разрешение на чтение и записи. Интерфейс по умолчанию находится только для чтения. MAPI_MODIFY необходимо устанавливать каждый раз, MAPI_CREATE установлено.
    
 _lppStream_
  
> [out] Указатель на указатель на объект потока, который содержит текст из свойства **PR_BODY** ([PidTagBody)](pidtagbody-canonical-property.md)переданного сообщения инкапсулированного сообщения, который поддерживает [интерфейс IStream.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и возвратил ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Поставщики транспорта, поставщики хранимых сообщений и шлюзы вызывали метод **ITnef::OpenTaggedBody,** чтобы открыть интерфейс потока в тексте инкапсулированного сообщения (т. е. в объекте TNEF). 
  
В рамках обработки **OpenTaggedBody** вставляет или обрабатывает теги вложений, которые указывают положение любых вложений или объектов OLE в тексте сообщения. Теги вложений имеют следующий формат: 
  
 **[[** _имя вложения:_  _n_ в **имени** _контейнера вложений_ **]]**
  
 _имя вложения_ описывает объект вложения;  _n_ — это число, которое идентифицирует вложение, которое является частью последовательности, инкрементным от значения, переданного в  _параметре lpKey_ функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx;](opentnefstreamex.md) и  _имя контейнера вложений_ описывает физический компонент, в котором находится объект вложения. 
  
 **OpenTaggedBody** считывает текст сообщения и вставляет тег вложения везде, где изначально в тексте был объект вложения. Исходный текст сообщения не меняется. 
  
Когда сообщение с тегами передается в поток, теги срезаются, а объекты вложений находятся в положении тегов в потоке.
  
## <a name="see-also"></a>См. также



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Каноническое свойство PidTagBody](pidtagbody-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

