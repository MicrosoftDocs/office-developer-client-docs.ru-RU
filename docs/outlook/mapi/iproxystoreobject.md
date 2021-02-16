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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет объект хранения протокола IMAP, который был расхвачен и который обеспечивает доступ к элементов в файле личных папок (PST) без необходимости синхронизации и скачивания элементов.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследуется от:  <br/> |[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|Предоставлено:  <br/> |Поставщик store сообщений  <br/> |
|Идентификатор интерфейса:  <br/> |**IID_IProxyStoreObject** <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
| *Член-заметель*  <br/> | *Не поддерживается и не документируется.*  <br/> |
|[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md) <br/> |Получает указатель на нерасхваченное хранилище IMAP.  <br/> |
| *Член-заметель*  <br/> | *Не поддерживается и не документируется.*  <br/> |
   
## <a name="remarks"></a>Примечания

Вызовите [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) в хранилище исходных сообщений, чтобы получить **интерфейс IProxyStoreObject.** Затем **вызовите IProxyStoreObject::UnwrapNoRef,** чтобы получить незавершенный объект store. Если **QueryInterface** возвращает ошибку **MAPI_E_INTERFACE_NOT_SUPPORTED,** хранилище не было оболочки. 
  
Поскольку **UnwrapNoRef** не добавит количество ссылок для этого нового указателя на объект неподтвержденного хранения, после успешного вызова **UnwrapNoRef** необходимо вызвать [IUnknown::AddRef,](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) чтобы сохранить количество ссылок. 
  

