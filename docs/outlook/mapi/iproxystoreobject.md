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
  
Предоставляет объект хранилища протокола IMAP, который был развернут и предоставляет доступ к элементам в файле личных папок (PST), не вызывая синхронизацию и не загружая элементы.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследуется от:  <br/> |[Интерфейс](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|Предоставлено:  <br/> |Поставщик хранилища сообщений  <br/> |
|Идентификатор интерфейса:  <br/> |**IID_IProxyStoreObject** <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
| *Элемент PlaceHolder*  <br/> | *Не поддерживается или не задокументировано.*  <br/> |
|[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md) <br/> |Получает указатель на неупакованное хранилище IMAP.  <br/> |
| *Элемент PlaceHolder*  <br/> | *Не поддерживается или не задокументировано.*  <br/> |
   
## <a name="remarks"></a>Примечания

Вызовите метод [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) в исходном хранилище сообщений для получения интерфейса **ипроксистореобжект** . Затем вызовите **ипроксистореобжект:: унврапнореф** , чтобы получить объект неупакованного хранилища. Если **QueryInterface** возвращает ошибку **MAPI_E_INTERFACE_NOT_SUPPORTED**, то хранилище не было заключено в оболочку. 
  
Так как **унврапнореф** не увеличивает значение счетчика ссылок для нового указателя на неупакованный объект Store после успешного вызова **унврапнореф**, необходимо вызвать метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) для поддержания счетчика ссылок. 
  

