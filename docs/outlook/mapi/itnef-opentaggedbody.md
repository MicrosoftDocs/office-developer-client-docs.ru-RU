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
ms.openlocfilehash: ed433dc1fcf2a366d2ece07ac06d4e12558e4aa7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809606"
---
# <a name="itnefopentaggedbody"></a>ITnef::OpenTaggedBody

  
  
**Относится к**: Outlook 
  
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
  
> [out] Указатель на указатель на объект потока, который содержит текст из свойства **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) передается в инкапсулированное сообщение, которая поддерживает интерфейс [IStream](http://msdn.microsoft.com/library/stg.istream%28Office.15%29.aspx) . 
    
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
