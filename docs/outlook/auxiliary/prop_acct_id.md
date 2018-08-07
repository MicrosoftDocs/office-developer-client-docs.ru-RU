---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Возвращает идентификатор, который уникальным образом определяет учетную запись в профиль, в котором создается учетная запись.
ms.openlocfilehash: a4ae193b89132ea718e16aec82f592205f9771c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807943"
---
# <a name="propacctid"></a>PROP_ACCT_ID

Возвращает идентификатор, который уникальным образом определяет учетную запись в профиль, в котором создается учетная запись.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x0001  <br/> |
|Тип свойства:  <br/> |PT_LONG  <br/> |
|Свойство tag:  <br/> |0x00010003  <br/> |
|Access:  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

Получение этого свойства с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md). При попытке установить для этого свойства, данное свойство возвращает **E_OLK_PROP_READ_ONLY**. 
  
Это свойство отличается от [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) , в том, что его значение является уникальным только среди всех учетных записей в этот профиль, в котором был создан учетной записи, в то время как **Свойства\_ACCT_MINI_UID** однозначно определяет учетную запись в пределах и за пределами профилей, в которой была создана учетная запись. Когда сообщение с помощью этих свойств перемещается на второй компьютер с другой профиль Outlook и другой набор учетных записей, **PROP_ACCT_ID** можно возможно конфликтов с использованием учетной записи в профиле второй компьютер и **PROP_ACCT_MINI_UID** можно однозначно определить исходной учетной записи в исходный профиль. 
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)  
- [Constants (Account management API)](constants-account-management-api.md)

