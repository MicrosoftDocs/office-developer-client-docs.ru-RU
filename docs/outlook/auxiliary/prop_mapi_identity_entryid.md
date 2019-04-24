---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Возвращает или задает идентификатор записи адресной книги для учетной записи.
ms.openlocfilehash: 2352f64b46e9884e95b7bf1f3693321f7cd224ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326434"
---
# <a name="propmapiidentityentryid"></a>PROP_MAPI_IDENTITY_ENTRYID

Возвращает или задает идентификатор записи адресной книги для учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иолкаккаунт](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x2002  <br/> |
|Тип свойства:  <br/> |PT_BINARY  <br/> |
|Тег свойства:  <br/> |0x20020102  <br/> |
|Обращения  <br/> |Чтение и запись  <br/> |
   
## <a name="remarks"></a>Замечания

 **Идентификатор\_EntryID\_идентификатора\_свойства Prop MAPI** не должен существовать на каждой учетной записи. Например, учетная запись Exchange может иметь **идентификатор\_EntryID\_идентификатора\_свойства Prop MAPI** и [Not\_Prop аккт_усер_емаил_аддр](prop_acct_user_email_addr.md), в то время как для учетной записи SMTP/POP3 ситуация обратна. **PROP\_МАПИ_ИДЕНТИТИ_ЕНТРИД** возвращает идентификатор записи, аналогичный значению, возвращенному _лппентрид_ в [IMAPISession:: куеридентити](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx). 
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)

