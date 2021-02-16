---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: Возвращает отметку учетной записи.
ms.openlocfilehash: fe3c6e65e12ab62bd1c2ec0245e4a22502f610eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408252"
---
# <a name="prop_acct_stamp"></a>PROP_ACCT_STAMP

Возвращает отметку учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

См. [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x000D  <br/> |
|Тип свойства:  <br/> |PT_UNICODE  <br/> |
|Тег свойства:  <br/> |0x000D001F  <br/> |
|Access:  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Примечания

Получите это свойство с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md). Если клиент пытается установить это свойство, это свойство возвращает E_OLK_PROP_READ_ONLY **.** 
  
## <a name="see-also"></a>См. также

- [Сведения об API управления учетными записями](about-the-account-management-api.md)  
- [Constants (Account management API)](constants-account-management-api.md)

