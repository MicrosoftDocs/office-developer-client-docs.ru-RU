---
title: IOlkErrorUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9cfbf12c-a71c-092b-d86a-c5585b0f1edb
ms.openlocfilehash: dc2fe6bbaf4515d5c5f5be694b15040bf03ef374
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384642"
---
# <a name="iolkerrorunknown"></a>IOlkErrorUnknown

Дополнительные сведения о последней ошибки.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследует от:  <br/> |[Интерфейс IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Предоставлено:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IOlkErrorUnknown  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetLastError](iolkerrorunknown-getlasterror.md) <br/> |Получает строку сообщения для заданной ошибки.  <br/> |
   
## <a name="remarks"></a>Замечания

Этот интерфейс предоставляет дополнительные сведения об ошибке в [IOlkAccountManager](iolkaccountmanager.md), [IOlkAccountNotify](iolkaccountnotify.md)и [IOlkAccount](iolkaccount.md). Это базовый интерфейс для **IOlkAccountManager**, **IOlkAccountNotify**и **IOlkAccount**. 
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)

