---
title: ОБЪЯВЛЕНИЕ ПАРАМЕТРА OWNERACCESS (Microsoft Access SQL)
TOCTitle: WITH OWNERACCESS OPTION declaration (Microsoft Access SQL)
ms:assetid: 82e51071-12b2-e97e-07b4-27ffceda831e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196724(v=office.15)
ms:contentKeyID: 48545993
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277584
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0882f143f13f6bd6d66c894f242a9cd50ebf9489
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302508"
---
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a>ОБЪЯВЛЕНИЕ ПАРАМЕТРА OWNERACCESS (Microsoft Access SQL)


**Область применения**: Access 2013, Office 2013

В многосервной среде с безопасной работой используйте это объявление с запросом, чтобы предоставить пользователю, который выполняет запрос, те же разрешения, что и владельцу запроса.

## <a name="syntax"></a>Синтаксис

*sqlstatement* С ПАРАМЕТРОМ OWNERACCESS

## <a name="remarks"></a>Заметки

Объявление ПАРАМЕТРА WITH OWNERACCESS является необязательным.

В следующем примере пользователь может просматривать сведения о зарплате (даже если у пользователя нет разрешения на просмотр таблицы ведомости о зарплате) при условии, что владелец запроса имеет это разрешение:

``` sql
SELECT LastName, 
FirstName, Salary
FROM Employees 
ORDER BY LastName 
WITH OWNERACCESS OPTION;
```

Если в противном случае пользователю не будет возможности создавать или добавлять таблицу, можно использовать ПАРАМЕТР WITH OWNERACCESS, чтобы позволить пользователю запускать запрос на создание таблицы или добавление.

Если вы хотите принудительно применить параметры безопасности и разрешения пользователей, не включаем объявление WITH OWNERACCESS OPTION.

Для этого параметра требуется доступ к файлу System.mdw, связанному с базой данных. Он полезен только в защищенных многоядерных реализациях.

