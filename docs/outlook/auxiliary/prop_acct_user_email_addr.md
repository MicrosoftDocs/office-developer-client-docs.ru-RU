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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326532"
---
# <a name="propacctuseremailaddr"></a>PROP_ACCT_USER_EMAIL_ADDR

Указывает адрес электронной почты для учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иолкаккаунт](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x000C  <br/> |
|Тип свойства:  <br/> |PT_UNICODE  <br/> |
|Тег свойства:  <br/> |0x000C001F  <br/> |
|Обращения  <br/> |Чтение и запись  <br/> |
   
## <a name="remarks"></a>Замечания

 **Проп_аккт_усер_емаил_аддр** не должен существовать на каждой учетной записи. Например, учетная запись Exchange может иметь [проп_мапи_идентити_ентрид](prop_mapi_identity_entryid.md) , но не **проп_аккт_усер_емаил_аддр**, в то время как для учетной записи SMTP/POP3 ситуация обратна.
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)

