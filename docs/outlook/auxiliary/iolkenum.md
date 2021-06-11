---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322101"
---
# <a name="iolkenum"></a>IOlkEnum

Поддерживает учетные записи в качестве [объектов IUnknown.](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследует от:  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
|Предоставлено:  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IOlkEnum  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[GetCount](iolkenum-getcount.md) <br/> |Получает количество учетных записей в этом переуметоре.  <br/> |
|[Reset](iolkenum-reset.md) <br/> |Сбрасывает переустановку в начале.  <br/> |
|[GetNext](iolkenum-getnext.md) <br/> |Получает следующую учетную запись в переуметоре.  <br/> |
|[Skip](iolkenum-skip.md) <br/> |Пропускает указанное количество учетных записей в этом переуметоре.  <br/> |
   
## <a name="remarks"></a>Примечания

Этот интерфейс возвращается **IOlkAccountManager::EnumerateAccounts** при получении переучета учетных записей. 
  
## <a name="see-also"></a>См. также

- [Сведения об API управления учетными записями](about-the-account-management-api.md) 
- [Constants (Account management API)](constants-account-management-api.md)

