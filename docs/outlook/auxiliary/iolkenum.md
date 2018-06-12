---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: be91a56f93b787f5570139768d96eb4f7fe9ac02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807880"
---
# <a name="iolkenum"></a>IOlkEnum

Поддерживает перечисления учетных записей как объекты [IUnknown](http://msdn.microsoft.com/library/com.iunknown%28Office.15%29.aspx) . 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследует от:  <br/> |[Интерфейс IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Реализованный:  <br/> |Outlook  <br/> |
|Предоставлено:  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|Вызывается:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IOlkEnum  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetCount](iolkenum-getcount.md) <br/> |Получает число учетных записей в перечислитель.  <br/> |
|[Сброс](iolkenum-reset.md) <br/> |Сбрасывает перечислитель к началу.  <br/> |
|[GetNext](iolkenum-getnext.md) <br/> |Получает перечислитель следующего учетной записи.  <br/> |
|[Пропустить](iolkenum-skip.md) <br/> |Пропускает указанное число учетных записей в перечислитель.  <br/> |
   
## <a name="remarks"></a>Замечания

Этот интерфейс возвращается **IOlkAccountManager::EnumerateAccounts** при получении перечислитель учетных записей. 
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md) 
- [Constants (Account management API)](constants-account-management-api.md)

