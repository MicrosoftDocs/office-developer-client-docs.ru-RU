---
title: С помощью объявления параметра OWNERACCESS OPTION (Microsoft Access SQL)
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
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a>С помощью объявления параметра OWNERACCESS OPTION (Microsoft Access SQL)


**Область применения**: Access 2013, Office 2013

В многопользовательской среде с безопасной рабочей группой используйте это объявление с запросом, чтобы дать пользователю, выполняющему запрос, те же разрешения, что и у владельца запроса.

## <a name="syntax"></a>Синтаксис

*склстатемент* С ПАРАМЕТРОМ OWNERACCESS OPTION

## <a name="remarks"></a>Примечания

Объявление параметра WITH OWNERACCESS OPTION является необязательным.

В приведенном ниже примере показано, как разрешить пользователю просматривать сведения о зарплате (даже если пользователь не имеет разрешения на просмотр таблицы зарплаты), при условии, что у владельца запроса есть такое разрешение:

``` sql
SELECT LastName, 
FirstName, Salary
FROM Employees 
ORDER BY LastName 
WITH OWNERACCESS OPTION;
```

Если пользователю в противном случае не удалось создать или добавить таблицу, можно использовать параметр WITH OWNERACCESS OPTION, чтобы разрешить пользователю запускать запрос на создание таблицы или добавление.

Если вы хотите применить параметры безопасности рабочей группы и разрешения пользователей, не включайте объявление параметра WITH OWNERACCESS OPTION.

При использовании этого параметра необходимо иметь доступ к файлу System. mdw, связанному с базой данных. Он полезен только в защищенных многопользовательских реализациях.

