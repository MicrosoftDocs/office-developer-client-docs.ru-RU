---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Указывает адрес электронной почты для учетной записи.
ms.openlocfilehash: 115941fdf2fdec01da8d6bc1320ac6cdc0930ffa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436778"
---
# <a name="prop_acct_user_email_addr"></a>PROP_ACCT_USER_EMAIL_ADDR

Указывает адрес электронной почты для учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

См. [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x000C  <br/> |
|Тип свойства:  <br/> |PT_UNICODE  <br/> |
|Тег свойства:  <br/> |0x000C001F  <br/> |
|Access:  <br/> |Чтение и запись  <br/> |
   
## <a name="remarks"></a>Примечания

 **PROP_ACCT_USER_EMAIL_ADDR** ожидается не для каждой учетной записи. Например, учетная запись [](prop_mapi_identity_entryid.md) Exchange может иметь PROP_MAPI_IDENTITY_ENTRYID, **но не** PROP_ACCT_USER_EMAIL_ADDR, тогда как для учетной записи SMTP/POP3 ситуация обратная.
  
## <a name="see-also"></a>См. также

- [Сведения об API управления учетными записями](about-the-account-management-api.md)

