---
title: ипроксистореобжектунврапнореф
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Получает указатель на неупакованный объект хранилища протокола IMAP, который предоставляет доступ к основному файлу личных папок (PST), не вызывая синхронизацию и не загружая элементы.
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a>Параметры

 _ппвобжект_
  
> вышли Указатель на объект [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) , который переключается в оболочку. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK
  
- Вызов выполнен успешно, и в _ппвобжект_возвращен указатель на неупакованный интерфейс.
    
## <a name="remarks"></a>Примечания

Без предварительного развертывания хранилища IMAP доступ к сообщению в хранилище может вызвать принудительную синхронизацию, которая пытается скачать все сообщение. Использование неупакованного хранилища позволяет получить доступ к сообщению в текущем состоянии, не запуская загрузку.
  
Так как **унврапнореф** не увеличивает значение счетчика ссылок для нового указателя на неупакованный объект Store после успешного вызова **унврапнореф**, необходимо вызвать метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) для поддержания счетчика ссылок. 
  
## <a name="see-also"></a>См. также



[IProxyStoreObject](iproxystoreobject.md)

