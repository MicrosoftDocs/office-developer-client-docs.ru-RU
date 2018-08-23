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
ms.openlocfilehash: b842bee8d9e243aa38bafe39d786a31b5527b054
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567946"
---
# <a name="iproxystoreobject"></a>IProxyStoreObject

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит объект хранилища протокола доступа сообщения Интернета (IMAP), которая была оболочку и без вызова синхронизации и загрузку элементов, которая позволяет получить доступ к элементов в файл личных папок (PST).
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследуется от:  <br/> |[Интерфейс IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) <br/> |
|Автор:  <br/> |Поставщик хранилища сообщений  <br/> |
|Идентификатор интерфейса:  <br/> |**IID_IProxyStoreObject** <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
| *Заполнитель члена*  <br/> | *Не поддерживается, документированных.*  <br/> |
|[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md) <br/> |Получает указатель на хранилище оболочку IMAP.  <br/> |
| *Заполнитель члена*  <br/> | *Не поддерживается, документированных.*  <br/> |
   
## <a name="remarks"></a>Замечания

Вызов [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) хранилища сообщений источника для получения интерфейса **IProxyStoreObject** . Затем вызовите **IProxyStoreObject::UnwrapNoRef** , чтобы получить объект развернуть хранилища. Если **QueryInterface** возвращает ошибку **MAPI_E_INTERFACE_NOT_SUPPORTED**, затем хранилище не заключен. 
  
Так как **UnwrapNoRef** не увеличивает счетчик ссылок для этого нового указателя на объект оболочку хранилище после успешного вызова **UnwrapNoRef**, должны вызывать [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) для поддержки счетчик ссылок. 
  

