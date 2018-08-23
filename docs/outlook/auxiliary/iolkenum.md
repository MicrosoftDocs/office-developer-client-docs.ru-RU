---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 19ec67bf033859073e7685912196369b664f4a36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592691"
---
# <a name="iolkenum"></a>IOlkEnum

Поддерживает перечисления учетных записей как объекты [IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) . 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследует от:  <br/> |[Интерфейс IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Реализованный:  <br/> |Outlook  <br/> |
|Предоставлено:  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|Вызывается:  <br/> |Клиент  <br/> |
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

