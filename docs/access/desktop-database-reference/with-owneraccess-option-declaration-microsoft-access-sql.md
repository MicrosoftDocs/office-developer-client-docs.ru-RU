---
title: ОБЪЯВЛЕНИЕ OWNERACCESS OPTION (Microsoft Access SQL)
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
ms.openlocfilehash: 0eca4738d07c54b049073aaf5d4b802864761fa5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920601"
---
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a>ОБЪЯВЛЕНИЕ OWNERACCESS OPTION (Microsoft Access SQL)


**Применимо к**: Access 2013, Office 2013

В многопользовательской среде с безопасной рабочей группы используйте следующее объявление с помощью запроса для предоставления пользователю, запускающему запрос разрешения как владелец запроса.

## <a name="syntax"></a>Синтаксис

*SQLStatement* С ПОМОЩЬЮ ПАРАМЕТРА OWNERACCESS

## <a name="remarks"></a>Примечания

Объявление OWNERACCESS OPTION не является обязательным.

Следующий пример позволяет пользователям просматривать сведения о зарплате (даже в том случае, если пользователь в противном случае — не имеет разрешения на просмотр в таблице зарплаты), при условии, что владелец запроса имеет данное разрешение:

``` sql
SELECT LastName, 
FirstName, Salary
FROM Employees 
ORDER BY LastName 
WITH OWNERACCESS OPTION;
```

Если пользователь в противном случае — не позволяет создание или добавление к таблице, можно использовать WITH OWNERACCESS OPTION дать ему для запуска на создание таблицы или запрос на добавление.

Если нужно применить параметры рабочей группы безопасности и разрешений пользователей, не включайте объявление OWNERACCESS OPTION.

Этот параметр, необходимо иметь доступ к файлу System.mdw, связанной с базой данных. Полезно только в защищенных многопользовательских системах.

