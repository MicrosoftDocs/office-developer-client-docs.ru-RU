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
ms.openlocfilehash: 7c6c763e918947c423c5dae283b0d4ab2f880616
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809528"
---
# <a name="iproxystoreobjectunwrapnoref"></a>IProxyStoreObject::UnwrapNoRef

  
  
**Относится к**: Outlook 
  
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

