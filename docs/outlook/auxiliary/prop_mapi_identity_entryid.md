---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Получает или задает идентификатор записи адресной книги для учетной записи.
ms.openlocfilehash: d85a779da36c2780fe058f906086f61cfc47d5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807945"
---
# <a name="propmapiidentityentryid"></a>PROP_MAPI_IDENTITY_ENTRYID

Получает или задает идентификатор записи адресной книги для учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x2002  <br/> |
|Тип свойства:  <br/> |PT_BINARY  <br/> |
|Свойство tag:  <br/> |0x20020102  <br/> |
|Access:  <br/> |Чтение и запись  <br/> |
   
## <a name="remarks"></a>Замечания

 **Свойства\_MAPI\_IDENTITY\_ENTRYID** не должен существовать в каждой учетной записи. К примеру, могут иметь учетную запись Exchange **Свойства\_MAPI\_УДОСТОВЕРЕНИЯ\_ENTRYID** задать и не [Свойства\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), а для учетной записи SMTP/POP3 ситуации изменен на обратный. **СВОЙСТВА\_MAPI_IDENTITY_ENTRYID** возвращает идентификатор записи, похожие на значение, возвращаемое _lppEntryID_ в [IMAPISession::QueryIdentity](http://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx). 
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)

