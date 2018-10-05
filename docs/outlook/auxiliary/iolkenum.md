---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389738"
---
# <a name="iolkenum"></a>IOlkEnum

Поддерживает перечисления учетных записей как объекты [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) . 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследует от:  <br/> |[Интерфейс IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
|Предоставлено:  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IOlkEnum  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetCount](iolkenum-getcount.md) <br/> |Получает число учетных записей в перечислитель.  <br/> |
|[Reset (Сбросить)](iolkenum-reset.md) <br/> |Сбрасывает перечислитель к началу.  <br/> |
|[GetNext](iolkenum-getnext.md) <br/> |Получает перечислитель следующего учетной записи.  <br/> |
|[Пропустить](iolkenum-skip.md) <br/> |Пропускает указанное число учетных записей в перечислитель.  <br/> |
   
## <a name="remarks"></a>Замечания

Этот интерфейс возвращается **IOlkAccountManager::EnumerateAccounts** при получении перечислитель учетных записей. 
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md) 
- [Constants (Account management API)](constants-account-management-api.md)

