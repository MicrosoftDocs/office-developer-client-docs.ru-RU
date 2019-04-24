---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Возвращает идентификатор учетной записи, уникальный для профилей Outlook.
ms.openlocfilehash: 209f7dd89b8d947b999f2a068373aaf61a3e9784
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327631"
---
# <a name="propacctminiuid"></a>PROP_ACCT_MINI_UID

Возвращает идентификатор учетной записи, уникальный для профилей Outlook.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иолкаккаунт](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x0003  <br/> |
|Тип свойства:  <br/> |PT_LONG  <br/> |
|Тег свойства:  <br/> |0x00030003  <br/> |
|Обращения  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

Получить это свойство можно с помощью [иолкаккаунт::/Prop](iolkaccount-getprop.md). Если клиент пытается установить это свойство, это свойство возвращает **е_олк_проп_реад_онли**. 
  
Это свойство отличается от [проп_аккт_ид](prop_acct_id.md) в том, что его значение однозначно определяет учетную запись внутри и снаружи профиля, в котором была создана учетная запись, а **проп_аккт_ид** является уникальным только для всех учетных записей в пределах этого профиля. в котором была создана учетная запись. Когда сообщение с этими свойствами перемещается на второй компьютер с другим профилем Outlook и разными наборами учетных записей, **проп_аккт_мини_уид** может однозначно определить исходную учетную запись в исходном профиле. Однако **проп_аккт_ид** может конфликтовать с учетной записью в профиле второго компьютера. 
  
## <a name="see-also"></a>См. также

- [PROP_ACCT_ID](prop_acct_id.md)  
- [About the Account Management API](about-the-account-management-api.md) 
- [Constants (Account management API)](constants-account-management-api.md)

