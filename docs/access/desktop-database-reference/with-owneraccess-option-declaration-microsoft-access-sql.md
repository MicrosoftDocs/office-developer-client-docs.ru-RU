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
localization_priority: Normal
ms.openlocfilehash: 0882f143f13f6bd6d66c894f242a9cd50ebf9489
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718870"
---
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a><span data-ttu-id="da1a3-102">ОБЪЯВЛЕНИЕ OWNERACCESS OPTION (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="da1a3-102">WITH OWNERACCESS OPTION declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="da1a3-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="da1a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="da1a3-104">В многопользовательской среде с безопасной рабочей группы используйте следующее объявление с помощью запроса для предоставления пользователю, запускающему запрос разрешения как владелец запроса.</span><span class="sxs-lookup"><span data-stu-id="da1a3-104">In a multiuser environment with a secure workgroup, use this declaration with a query to give the user who runs the query the same permissions as the query's owner.</span></span>

## <a name="syntax"></a><span data-ttu-id="da1a3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da1a3-105">Syntax</span></span>

<span data-ttu-id="da1a3-106">*SQLStatement* С ПОМОЩЬЮ ПАРАМЕТРА OWNERACCESS</span><span class="sxs-lookup"><span data-stu-id="da1a3-106">*sqlstatement* WITH OWNERACCESS OPTION</span></span>

## <a name="remarks"></a><span data-ttu-id="da1a3-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="da1a3-107">Remarks</span></span>

<span data-ttu-id="da1a3-108">Объявление OWNERACCESS OPTION не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="da1a3-108">The WITH OWNERACCESS OPTION declaration is optional.</span></span>

<span data-ttu-id="da1a3-109">Следующий пример позволяет пользователям просматривать сведения о зарплате (даже в том случае, если пользователь в противном случае — не имеет разрешения на просмотр в таблице зарплаты), при условии, что владелец запроса имеет данное разрешение:</span><span class="sxs-lookup"><span data-stu-id="da1a3-109">The following example enables the user to view salary information (even if the user does not otherwise have permission to view the Payroll table), provided that the query's owner does have that permission:</span></span>

``` sql
SELECT LastName, 
FirstName, Salary
FROM Employees 
ORDER BY LastName 
WITH OWNERACCESS OPTION;
```

<span data-ttu-id="da1a3-110">Если пользователь в противном случае — не позволяет создание или добавление к таблице, можно использовать WITH OWNERACCESS OPTION дать ему для запуска на создание таблицы или запрос на добавление.</span><span class="sxs-lookup"><span data-stu-id="da1a3-110">If a user is otherwise prevented from creating or adding to a table, you can use WITH OWNERACCESS OPTION to enable the user to run a make-table or append query.</span></span>

<span data-ttu-id="da1a3-111">Если нужно применить параметры рабочей группы безопасности и разрешений пользователей, не включайте объявление OWNERACCESS OPTION.</span><span class="sxs-lookup"><span data-stu-id="da1a3-111">If you want to enforce workgroup security settings and users' permissions, do not include the WITH OWNERACCESS OPTION declaration.</span></span>

<span data-ttu-id="da1a3-112">Этот параметр, необходимо иметь доступ к файлу System.mdw, связанной с базой данных.</span><span class="sxs-lookup"><span data-stu-id="da1a3-112">This option requires you to have access to the System.mdw file associated with the database.</span></span> <span data-ttu-id="da1a3-113">Полезно только в защищенных многопользовательских системах.</span><span class="sxs-lookup"><span data-stu-id="da1a3-113">It is useful only in secured multiuser implementations.</span></span>

