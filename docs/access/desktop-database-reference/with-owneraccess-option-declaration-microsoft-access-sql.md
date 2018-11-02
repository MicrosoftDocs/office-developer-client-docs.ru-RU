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
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a><span data-ttu-id="333de-102">ОБЪЯВЛЕНИЕ OWNERACCESS OPTION (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="333de-102">WITH OWNERACCESS OPTION declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="333de-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="333de-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="333de-104">В многопользовательской среде с безопасной рабочей группы используйте следующее объявление с помощью запроса для предоставления пользователю, запускающему запрос разрешения как владелец запроса.</span><span class="sxs-lookup"><span data-stu-id="333de-104">In a multiuser environment with a secure workgroup, use this declaration with a query to give the user who runs the query the same permissions as the query's owner.</span></span>

## <a name="syntax"></a><span data-ttu-id="333de-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="333de-105">Syntax</span></span>

<span data-ttu-id="333de-106">*SQLStatement* С ПОМОЩЬЮ ПАРАМЕТРА OWNERACCESS</span><span class="sxs-lookup"><span data-stu-id="333de-106">*sqlstatement* WITH OWNERACCESS OPTION</span></span>

## <a name="remarks"></a><span data-ttu-id="333de-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="333de-107">Remarks</span></span>

<span data-ttu-id="333de-108">Объявление OWNERACCESS OPTION не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="333de-108">The WITH OWNERACCESS OPTION declaration is optional.</span></span>

<span data-ttu-id="333de-109">Следующий пример позволяет пользователям просматривать сведения о зарплате (даже в том случае, если пользователь в противном случае — не имеет разрешения на просмотр в таблице зарплаты), при условии, что владелец запроса имеет данное разрешение:</span><span class="sxs-lookup"><span data-stu-id="333de-109">The following example enables the user to view salary information (even if the user does not otherwise have permission to view the Payroll table), provided that the query's owner does have that permission:</span></span>

``` sql
SELECT LastName, 
FirstName, Salary
FROM Employees 
ORDER BY LastName 
WITH OWNERACCESS OPTION;
```

<span data-ttu-id="333de-110">Если пользователь в противном случае — не позволяет создание или добавление к таблице, можно использовать WITH OWNERACCESS OPTION дать ему для запуска на создание таблицы или запрос на добавление.</span><span class="sxs-lookup"><span data-stu-id="333de-110">If a user is otherwise prevented from creating or adding to a table, you can use WITH OWNERACCESS OPTION to enable the user to run a make-table or append query.</span></span>

<span data-ttu-id="333de-111">Если нужно применить параметры рабочей группы безопасности и разрешений пользователей, не включайте объявление OWNERACCESS OPTION.</span><span class="sxs-lookup"><span data-stu-id="333de-111">If you want to enforce workgroup security settings and users' permissions, do not include the WITH OWNERACCESS OPTION declaration.</span></span>

<span data-ttu-id="333de-112">Этот параметр, необходимо иметь доступ к файлу System.mdw, связанной с базой данных.</span><span class="sxs-lookup"><span data-stu-id="333de-112">This option requires you to have access to the System.mdw file associated with the database.</span></span> <span data-ttu-id="333de-113">Полезно только в защищенных многопользовательских системах.</span><span class="sxs-lookup"><span data-stu-id="333de-113">It is useful only in secured multiuser implementations.</span></span>

