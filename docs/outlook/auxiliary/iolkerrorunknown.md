---
title: IOlkErrorUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9cfbf12c-a71c-092b-d86a-c5585b0f1edb
ms.openlocfilehash: dc2fe6bbaf4515d5c5f5be694b15040bf03ef374
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321856"
---
# <a name="iolkerrorunknown"></a>IOlkErrorUnknown

Предоставляет дополнительные сведения о последней ошибке.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследует от:  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Предоставлено:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IOlkErrorUnknown  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[GetLastError](iolkerrorunknown-getlasterror.md) <br/> |Получает строку сообщения для указанной ошибки.  <br/> |
   
## <a name="remarks"></a>Примечания

Этот интерфейс предоставляет дополнительные сведения об ошибке [в IOlkAccountManager,](iolkaccountmanager.md) [IOlkAccountNotify](iolkaccountnotify.md)и [IOlkAccount](iolkaccount.md). Это также базовый интерфейс **для IOlkAccountManager,** **IOlkAccountNotify** и **IOlkAccount**. 
  
## <a name="see-also"></a>См. также

- [Сведения об API управления учетными записями](about-the-account-management-api.md)

