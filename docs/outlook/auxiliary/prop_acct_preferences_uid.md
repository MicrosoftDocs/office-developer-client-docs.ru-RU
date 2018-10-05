---
title: PROP_ACCT_PREFERENCES_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ec0aac33-624e-48f7-8177-8f7b8db6af7d
description: Получает уникальный идентификатор (UID) для раздела профиля, в которой хранятся параметры учетной записи.
ms.openlocfilehash: 97f1a858c8f58e13b72b8d5f052b35359581b718
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395296"
---
# <a name="propacctpreferencesuid"></a>PROP_ACCT_PREFERENCES_UID

Получает уникальный идентификатор (UID) для раздела профиля, в которой хранятся параметры учетной записи. 
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x0022  <br/> |
|Тип свойства:  <br/> |PT_BINARY  <br/> |
|Свойство tag:  <br/> |0x00220102  <br/> |
|Access:  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

Используйте **PROP_ACCT_PREFERENCES_UID** вызовы [IMAPISupport::OpenProfileSection](https://msdn.microsoft.com/library/cd1fa994-9531-46c4-94e5-505e7f90b884%28Office.15%29.aspx) для получения раздела профиля, который содержит параметры учетной записи. 
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)
- [About anti-spam settings](about-anti-spam-settings.md)

