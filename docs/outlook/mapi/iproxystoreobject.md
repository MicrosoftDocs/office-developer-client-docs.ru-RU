---
title: IProxyStoreObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject
api_type:
- COM
ms.assetid: 567bede4-39a3-bfb4-af85-ba678e2cf4a5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 485d3f3cd4b6be4748a2ebf2ba0d0b71f691478f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315521"
---
# <a name="iproxystoreobject"></a>IProxyStoreObject

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет объект хранения протокола доступа к интернету (IMAP), который был растрачен и позволяет получать доступ к элементу в файле персональных папок (PST) без синхронизации и скачивания элементов.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Унаследовано от:  <br/> |[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|Предоставлено:  <br/> |Поставщик магазина сообщений  <br/> |
|Идентификатор интерфейса:  <br/> |**IID_IProxyStoreObject** <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
| *Член placeholder*  <br/> | *Не поддерживается или не документируется.*  <br/> |
|[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md) <br/> |Получает указатель в незавербованный магазин IMAP.  <br/> |
| *Член placeholder*  <br/> | *Не поддерживается или не документируется.*  <br/> |
   
## <a name="remarks"></a>Примечания

Вызов [IUnknown::QueryInterface в](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) хранилище исходных сообщений для получения **интерфейса IProxyStoreObject.** Затем **позвоните в IProxyStoreObject::UnwrapNoRef,** чтобы получить незавершенный объект магазина. Если **QueryInterface** возвращает **ошибку** MAPI_E_INTERFACE_NOT_SUPPORTED, магазин не был завернут. 
  
Так как **UnwrapNoRef** не добавляет количество ссылок для этого нового указателя на объект незавержденного магазина, после успешного вызова **UnwrapNoRef** необходимо вызвать [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) для поддержания эталонного подсчета. 
  

