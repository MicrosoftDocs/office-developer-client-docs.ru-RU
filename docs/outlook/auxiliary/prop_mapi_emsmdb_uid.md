---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Представляет структуру ACCT_BIN, которая содержит уникальный идентификатор учетной записи Exchange.
ms.openlocfilehash: 6bb529da82cc24e41ddc70c5031f84050a2ece25
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395282"
---
# <a name="propmapiemsmdbuid"></a>PROP_MAPI_EMSMDB_UID

Представляет структуру [ACCT_BIN](acct_bin.md) , которая содержит уникальный идентификатор учетной записи Exchange. 
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x2009  <br/> |
|Тип свойства:  <br/> |PT_BINARY  <br/> |
|Свойство tag:  <br/> |0x20090102  <br/> |
|Access:  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

Получение этого свойства с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md).
  
Используйте [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) для проверки, если учетная запись является учетной записью Exchange. Если он установлен, **Свойства\_MAPI_EMSMDB_UID** — это **ACCT_BIN** , содержащий **emsmdbUID**, который является уникальным Идентификатором для учетной записи Exchange. Если учетная запись не является учетной записью Exchange, это свойство не определено.
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md) 
- [Constants (Account management API)](constants-account-management-api.md)
- [Использование нескольких учетных записей Exchange](https://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [������������ �������� PidTagExchangeProfileSectionId](https://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

