---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Возвращает идентификатор учетной записи, которая является уникальным для профилей Outlook.
ms.openlocfilehash: 9b2e30c0f57a54af219e68a8c2fe91e5dba4ddbe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807944"
---
# <a name="propacctminiuid"></a>PROP_ACCT_MINI_UID

Возвращает идентификатор учетной записи, которая является уникальным для профилей Outlook.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x0003  <br/> |
|Тип свойства:  <br/> |PT_LONG  <br/> |
|Свойство tag:  <br/> |0x00030003  <br/> |
|Access:  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

Получение этого свойства с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md). При попытке установить для этого свойства, данное свойство возвращает **E_OLK_PROP_READ_ONLY**. 
  
Это свойство отличается от [PROP_ACCT_ID](prop_acct_id.md) , в том, что его значение однозначно определяет учетную запись в пределах и за ее пределами профилей, в которой была создана учетная запись, то время как **PROP_ACCT_ID** является уникальным только во все учетные записи в пределах одного профиля в котором был создан учетной записи. Если сообщение с помощью этих свойств перемещается на второй компьютер с другой профиль Outlook и другой набор учетных записей, **PROP_ACCT_MINI_UID** можно однозначно определить исходной учетной записи в исходный профиль. Тем не менее **PROP_ACCT_ID** возможно могут конфликтовать с использованием учетной записи в профиле второй компьютер. 
  
## <a name="see-also"></a>См. также

- [PROP_ACCT_ID](prop_acct_id.md)  
- [About the Account Management API](about-the-account-management-api.md) 
- [Constants (Account management API)](constants-account-management-api.md)

