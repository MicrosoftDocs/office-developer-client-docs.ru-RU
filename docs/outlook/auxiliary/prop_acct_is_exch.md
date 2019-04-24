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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327652"
---
# <a name="propacctisexch"></a>PROP_ACCT_IS_EXCH

Значение true, если учетная запись является учетной записью Exchange.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иолкаккаунт](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x0014  <br/> |
|Тип свойства:  <br/> |PT_LONG  <br/> |
|Тег свойства:  <br/> |0x00140003  <br/> |
|Обращения  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

Получить это свойство можно с помощью [иолкаккаунт::/Prop](iolkaccount-getprop.md). Если клиент пытается установить это свойство, это свойство возвращает **е_олк_проп_реад_онли**. 
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md) 
- [Constants (Account management API)](constants-account-management-api.md)

