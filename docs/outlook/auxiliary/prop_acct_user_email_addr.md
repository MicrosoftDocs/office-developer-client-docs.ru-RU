---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Указывает адрес электронной почты для учетной записи.
ms.openlocfilehash: 7d0bbba2dcb104326c360da6a10f3e19d1740e46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807948"
---
# <a name="propacctuseremailaddr"></a>PROP_ACCT_USER_EMAIL_ADDR

Указывает адрес электронной почты для учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x000C  <br/> |
|Тип свойства:  <br/> |PT_UNICODE  <br/> |
|Свойство tag:  <br/> |0x000C001F  <br/> |
|Access:  <br/> |Чтение и запись  <br/> |
   
## <a name="remarks"></a>Замечания

 **PROP_ACCT_USER_EMAIL_ADDR** не должен существовать в каждой учетной записи. Например, учетную запись Exchange может быть [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) , но не **PROP_ACCT_USER_EMAIL_ADDR**, то время как для учетной записи SMTP/POP3, ситуации изменен на обратный.
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)

