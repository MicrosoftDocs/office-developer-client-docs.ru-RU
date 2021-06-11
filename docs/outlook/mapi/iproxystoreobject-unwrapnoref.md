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
ms.openlocfilehash: ef9f506c1a95fec86c7f092b0299198e6149d3ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320155"
---
# <a name="iproxystoreobjectunwrapnoref"></a>IProxyStoreObject::UnwrapNoRef

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получает указатель на незавернутый объект магазина протокола доступа к интернет-сообщениям (IMAP), который предоставляет доступ к основному файлу персональных папок (PST) без синхронизации и скачивания элементов.
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a>Parameters

 _ppvObject_
  
> [вышел] Указатель на [объект магазина IMsgStore : IMAPIProp,](imsgstoreimapiprop.md) который развернут. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK
  
- Вызов был успешным, и указатель на незавершенный интерфейс был возвращен в  _ppvObject_.
    
## <a name="remarks"></a>Примечания

Без первой разверки магазина IMAP доступ к сообщению в магазине может привести к синхронизации, которая пытается скачать все сообщение. Использование незаверченного магазина позволяет получить доступ к сообщению в текущем состоянии, не запуская скачивание.
  
Так как **UnwrapNoRef** не добавляет количество ссылок для этого нового указателя на объект незавержденного магазина, после успешного вызова **UnwrapNoRef** необходимо вызвать [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) для поддержания эталонного подсчета. 
  
## <a name="see-also"></a>См. также



[IProxyStoreObject](iproxystoreobject.md)

