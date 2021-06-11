---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Возвращает идентификатор, уникальный идентификатор учетной записи в профиле, в котором создается учетная запись.
ms.openlocfilehash: dcb0a7935b9b764c44088971a1acb1f3647cbdb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407167"
---
# <a name="prop_acct_id"></a>PROP_ACCT_ID

Возвращает идентификатор, уникальный идентификатор учетной записи в профиле, в котором создается учетная запись.
  
## <a name="quick-info"></a>Краткие сведения

См. [iOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x0001  <br/> |
|Тип свойства:  <br/> |PT_LONG  <br/> |
|Тег свойства:  <br/> |0x00010003  <br/> |
|Доступ:  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Примечания

Получите это свойство с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md). Если клиент пытается установить это свойство, это свойство возвращает **E_OLK_PROP_READ_ONLY.** 
  
Это свойство отличается от [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) тем, что его значение уникально только для всех учетных записей в том профиле, в котором была создана учетная запись, в то время как **PROP \_ ACCT_MINI_UID** однозначно определяет учетную запись в профиле и за его пределами. Если сообщение с этими свойствами перемещается на второй компьютер с другим профилем Outlook и другим набором учетных записей, PROP_ACCT_ID может конфликтировать с учетной записью в профиле второго компьютера, а PROP_ACCT_MINI_UID может однозначно идентифицировать исходную учетную запись в исходном профиле.   
  
## <a name="see-also"></a>См. также

- [Сведения об API управления учетными записями](about-the-account-management-api.md)  
- [Constants (Account management API)](constants-account-management-api.md)

