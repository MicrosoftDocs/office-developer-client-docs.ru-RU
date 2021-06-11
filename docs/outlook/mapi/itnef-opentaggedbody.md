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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает интерфейс потока в тексте инкапсулированного сообщения.
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Parameters

 _lpMessage_
  
> [in] Указатель на сообщение, с которым связан поток. Это сообщение не обязательно должно быть таким же сообщением, которое передается в вызов функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx.](opentnefstreamex.md) 
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют открытие интерфейса потока. Можно установить следующие флаги:
    
MAPI_CREATE 
  
> Если свойство не существует в текущем сообщении, оно должно быть создано. Если свойство существует, текущие данные в свойстве должны быть заменены данными из Transport-Neutral формата Инкапсуляции (TNEF). Если реализация задает флаг MAPI_CREATE, она также должна установить MAPI_MODIFY флаг.
    
MAPI_MODIFY 
  
> Запросы на чтение и написание разрешений. Интерфейс по умолчанию только для чтения. MAPI_MODIFY должны быть установлены всякий раз, MAPI_CREATE установлено.
    
 _lppStream_
  
> [вышел] Указатель на указатель на объект **потока,** содержащий текст из свойства [PR_BODY (PidTagBody)](pidtagbody-canonical-property.md)инкапсулированного сообщения, поддерживаемого интерфейсом [IStream.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался и возвращает ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Поставщики транспорта, поставщики магазинов сообщений и шлюзы звонят по методу **ITnef::OpenTaggedBody,** чтобы открыть интерфейс потока в тексте инкапсулированного сообщения (т. е. на объекте TNEF). 
  
В рамках своей обработки **OpenTaggedBody** вставляет или обрабатывает теги вложений, которые указывают расположение любых вложений или объектов OLE в тексте сообщения. Теги вложений находятся в следующем формате: 
  
 **[[** _имя вложения:_  _n в_  _имени контейнера вложения]]_ 
  
 _Имя вложения_ описывает объект вложения;  _n_ — это число, которое определяет вложение, которое является частью последовательности, инкрементное значение, переданное в  _параметре lpKey_ функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx;](opentnefstreamex.md) и  _имя контейнера вложения_ описывает физический компонент, в котором находится объект вложения. 
  
 **OpenTaggedBody** считывает текст сообщения и вставляет тег вложения везде, где изначально в тексте появился объект вложения. Исходный текст сообщения не изменен. 
  
Когда сообщение с тегами передается потоку, теги отсеяются, а объекты вложений будут размещены в расположении тегов в потоке.
  
## <a name="see-also"></a>См. также



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Каноническое свойство PidTagBody](pidtagbody-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

