---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Представляет структуру АККТ_БИН, которая содержит UID учетной записи Exchange.
ms.openlocfilehash: 6bb529da82cc24e41ddc70c5031f84050a2ece25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326553"
---
# <a name="propmapiemsmdbuid"></a>PROP_MAPI_EMSMDB_UID

Представляет структуру [аккт_бин](acct_bin.md) , которая содержит UID учетной записи Exchange. 
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иолкаккаунт](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x2009  <br/> |
|Тип свойства:  <br/> |PT_BINARY  <br/> |
|Тег свойства:  <br/> |0x20090102  <br/> |
|Обращения  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

Получить это свойство можно с помощью [иолкаккаунт::/Prop](iolkaccount-getprop.md).
  
Используйте [проп_аккт_ис_ексч](prop_acct_is_exch.md) , чтобы проверить, является ли учетная запись учетной записью Exchange. Если это так, **prop\_Мапи_емсмдб_уид** — это **аккт_бин** , СОДЕРЖАЩИЙ **емсмдбуид**, который является уникальным идентификатором для учетной записи Exchange. Если учетная запись не является учетной записью Exchange, это свойство не определено.
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md) 
- [Constants (Account management API)](constants-account-management-api.md)
- [Использование нескольких учетных записей Exchange](https://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [������������ �������� PidTagExchangeProfileSectionId](https://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

