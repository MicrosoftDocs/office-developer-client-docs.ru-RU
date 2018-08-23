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
ms.openlocfilehash: 14964f367e3dbca484c4e1612b374a6a72ddf17b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593783"
---
# <a name="itnefopentaggedbody"></a>ITnef::OpenTaggedBody

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Открывает интерфейс потока на основе текста инкапсулированное сообщение.
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Параметры

 _lpMessage_
  
> [in] Указатель на сообщение, с которым связано потока. Это сообщение не требуется, чтобы то же сообщение, которое передается в вызове функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx](opentnefstreamex.md) . 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как открыть интерфейс потока. Можно задать следующие флажки:
    
MAPI_CREATE 
  
> Если свойство не существует в текущем сообщении, он должен быть создан. Если свойство существует, следует заменить текущие данные в свойстве с данными в потоке Transport-Neutral Encapsulation формата TNEF (). При реализации задает флаг MAPI_CREATE, он должен установить флаг MAPI_MODIFY.
    
MAPI_MODIFY 
  
> Запросы на разрешение чтения и записи. Интерфейс по умолчанию доступен только для чтения. При использовании MAPI_CREATE необходимо установить MAPI_MODIFY.
    
 _lppStream_
  
> [out] Указатель на указатель на объект потока, который содержит текст из свойства **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) передается в инкапсулированное сообщение, которая поддерживает интерфейс [IStream](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nn-objidl-istream) . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов успешно и возвращается ожидаемым значением или значения.
    
## <a name="remarks"></a>Замечания

Поставщики транспорта, поставщиков хранилища сообщений и шлюзов вызовите метод **ITnef::OpenTaggedBody** для открытия интерфейс потока на основе текста инкапсулированное сообщение (то есть на TNEF объектов). 
  
В процессе обработки **OpenTaggedBody** вставляет или анализирует теги вложения, которые указывают положения любого вложения или объекты OLE в качестве текста сообщения. Теги вложения, в следующем формате: 
  
 **[[** _имя вложения_ **:** _n_ **в** _имени контейнера вложения_ **]]**
  
 _имя вложения_ описывает объект вложения;  _n_ — это число, определяющее вложения, который является частью последовательности, увеличивающееся из значение, переданное в параметре _lpKey_ [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx](opentnefstreamex.md) функции; и _имени контейнера вложения_ описывает физические компоненты, где находится объект вложения. 
  
 **OpenTaggedBody** считывает текст сообщения и вставляет тег вложения везде, где объект вложения был записан в текст. Текст исходного сообщения не изменяется. 
  
При передаче сообщения с тегами потока, перечень тегов, будут опущены и объекты вложения будут перемещены в положение теги в потоке.
  
## <a name="see-also"></a>См. также



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Каноническое свойство PidTagBody](pidtagbody-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

