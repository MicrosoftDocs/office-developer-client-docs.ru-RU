---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: Значение true, если учетная запись является учетной записью Exchange.
ms.openlocfilehash: 2df750b208ff9d2a18cb0d7c22ec6b32b658c7b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418234"
---
# <a name="prop_acct_is_exch"></a>PROP_ACCT_IS_EXCH

Значение true, если учетная запись является учетной записью Exchange.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иолкаккаунт](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x0014  <br/> |
|Тип свойства:  <br/> |PT_LONG  <br/> |
|Тег свойства:  <br/> |0x00140003  <br/> |
|Обращения  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Примечания

Получить это свойство можно с помощью [иолкаккаунт::/Prop](iolkaccount-getprop.md). Если клиент пытается установить это свойство, это свойство возвращает **E_OLK_PROP_READ_ONLY**. 
  
## <a name="see-also"></a>См. также

- [Сведения об API управления учетными записями](about-the-account-management-api.md) 
- [Constants (Account management API)](constants-account-management-api.md)

