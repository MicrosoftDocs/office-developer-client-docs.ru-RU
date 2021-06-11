---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Извлекает или задает ID записи адресной книги для учетной записи.
ms.openlocfilehash: 2352f64b46e9884e95b7bf1f3693321f7cd224ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326434"
---
# <a name="prop_mapi_identity_entryid"></a>PROP_MAPI_IDENTITY_ENTRYID

Извлекает или задает ID записи адресной книги для учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

См. [iOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x2002  <br/> |
|Тип свойства:  <br/> |PT_BINARY  <br/> |
|Тег свойства:  <br/> |0x20020102  <br/> |
|Доступ:  <br/> |Чтение и запись  <br/> |
   
## <a name="remarks"></a>Примечания

 **PROP \_ ЗАПИСЬ \_ \_ ИДЕНТИФИКАТОРА MAPI** не должна существовать во всех учетных записях. Например, у Exchange учетной записи МОЖЕТ быть набор ИДЕНТИФИКАТОРА PROP **\_ MAPI \_ \_ ENTRYID,** а не PROP [ \_ ACCT_USER_EMAIL_ADDR,](prop_acct_user_email_addr.md)в то время как для учетной записи SMTP/POP3 ситуация обратная. **PROP \_ MAPI_IDENTITY_ENTRYID** возвращает ID записи, аналогичный значению, возвращенным _lppEntryID_ в [IMAPISession::QueryIdentity.](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx) 
  
## <a name="see-also"></a>См. также

- [Сведения об API управления учетными записями](about-the-account-management-api.md)

