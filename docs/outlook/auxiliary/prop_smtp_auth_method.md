---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Задает способ проверки подлинности, используемый для учетной записи SMTP.
ms.openlocfilehash: bb5adeb1fe73ed8b7ab69ca584215b44e1a9e4b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434643"
---
# <a name="propsmtpauthmethod"></a>PROP_SMTP_AUTH_METHOD

Задает способ проверки подлинности, используемый для учетной записи SMTP.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Идентификатор:  <br/> |0x0208  <br/> |
|Тип свойства:  <br/> |ПТ_ДВОРД  <br/> |
|Тег свойства:  <br/> |0x02080003  <br/> |
|Обращения  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Примечания

Значение представляет собой битовую маску для следующих констант. В этом разделе приведены [константы (API управления учетНыми записями)](constants-account-management-api.md) для их значений. 
  
- **Смтп_аус_саме_ас_поп** означает использование тех же учетных данных, что и мой сервер входящей почты, что предоставляется [проп_инет_усер](prop_inet_user.md) и [проп_инет_пассворд](prop_inet_password.md).
    
- **Смтп_аус_усер_пасс** означает использование учетных данных, предоставляемых [проп_смтп_усер](prop_smtp_user.md) и [проп_смтп_пассворд](prop_smtp_password.md).
    
- **Смтп_аус_рецеиве_бефоре_сенд** означает, что пользователь должен войти на сервер входящей почты, прежде чем отправлять почту. 
    
## <a name="see-also"></a>См. также

- [Управление скачиванием сообщений для учетных записей POP3](managing-message-downloads-for-pop3-accounts.md)  
- [Constants (Account management API)](constants-account-management-api.md)

