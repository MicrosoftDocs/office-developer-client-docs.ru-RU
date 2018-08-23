---
title: IProxyStoreObjectUnwrapNoRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject.UnwrapNoRef
api_type:
- COM
ms.assetid: 1122b6e0-e7e1-e68a-e090-435777343d04
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8539f81ed1741063d878da492d925b63c488d1a9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586433"
---
# <a name="iproxystoreobjectunwrapnoref"></a>IProxyStoreObject::UnwrapNoRef

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Получает указатель на развернутый объект хранилища протокола доступа сообщения Интернета (IMAP), который предоставляет доступ к базовым файл личных папок (PST) без вызова синхронизации и загрузку элементов.
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a>Параметры

 _ppvObject_
  
> [out] Указатель на [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) объекта хранилища, который является оболочку. 
    
## <a name="return-values"></a>Возвращаемые значения

ЗНАЧЕНИЕ S_OK
  
- Вызов прошла успешно и возврата указатель на интерфейс развернуть в _ppvObject_.
    
## <a name="remarks"></a>Замечания

Без первого развертывания хранилище IMAP, доступ к сообщению в хранилище можно принудительно синхронизации, который пытается загрузить сообщение целиком. С помощью оболочку store позволяет получить доступ к сообщению в ее текущем состоянии без активации для загрузки.
  
Так как **UnwrapNoRef** не увеличивает счетчик ссылок для этого нового указателя на объект оболочку хранилище после успешного вызова **UnwrapNoRef**, должны вызывать [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) для поддержки счетчик ссылок. 
  
## <a name="see-also"></a>См. также



[IProxyStoreObject](iproxystoreobject.md)

