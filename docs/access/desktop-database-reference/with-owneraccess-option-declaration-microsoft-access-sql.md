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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302508"
---
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a><span data-ttu-id="9f9ff-102">ОБЪЯВЛЕНИЕ OWNERACCESS OPTION (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="9f9ff-102">WITH OWNERACCESS OPTION declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="9f9ff-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f9ff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9f9ff-104">В многоуровневой среде с безопасной workgroup используйте это объявление с запросом, чтобы предоставить пользователю, который выполняет запрос, те же разрешения, что и владельцу запроса.</span><span class="sxs-lookup"><span data-stu-id="9f9ff-104">In a multiuser environment with a secure workgroup, use this declaration with a query to give the user who runs the query the same permissions as the query's owner.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f9ff-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f9ff-105">Syntax</span></span>

<span data-ttu-id="9f9ff-106">*sqlstatement* С ПАРАМЕТРОМ OWNERACCESS</span><span class="sxs-lookup"><span data-stu-id="9f9ff-106">*sqlstatement* WITH OWNERACCESS OPTION</span></span>

## <a name="remarks"></a><span data-ttu-id="9f9ff-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="9f9ff-107">Remarks</span></span>

<span data-ttu-id="9f9ff-108">Объявление OPTION WITH OWNERACCESS является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9f9ff-108">The WITH OWNERACCESS OPTION declaration is optional.</span></span>

<span data-ttu-id="9f9ff-109">В следующем примере пользователь может просматривать сведения о зарплате (даже если у пользователя нет разрешения на просмотр таблицы payroll) при условии, что у владельца запроса есть такое разрешение:</span><span class="sxs-lookup"><span data-stu-id="9f9ff-109">The following example enables the user to view salary information (even if the user does not otherwise have permission to view the Payroll table), provided that the query's owner does have that permission:</span></span>

``` sql
SELECT LastName, 
FirstName, Salary
FROM Employees 
ORDER BY LastName 
WITH OWNERACCESS OPTION;
```

<span data-ttu-id="9f9ff-110">Если пользователю в противном случае не позволяют создавать или добавлять в таблицу, можно использовать ПАРАМЕТР OWNERACCESS, чтобы позволить пользователю выполнить запрос make-table или append.</span><span class="sxs-lookup"><span data-stu-id="9f9ff-110">If a user is otherwise prevented from creating or adding to a table, you can use WITH OWNERACCESS OPTION to enable the user to run a make-table or append query.</span></span>

<span data-ttu-id="9f9ff-111">Чтобы обеспечить соблюдение параметров безопасности и разрешений пользователей, не включай в себя объявление WITH OWNERACCESS OPTION.</span><span class="sxs-lookup"><span data-stu-id="9f9ff-111">If you want to enforce workgroup security settings and users' permissions, do not include the WITH OWNERACCESS OPTION declaration.</span></span>

<span data-ttu-id="9f9ff-112">Этот параметр требует доступа к файлу System.mdw, связанному с базой данных.</span><span class="sxs-lookup"><span data-stu-id="9f9ff-112">This option requires you to have access to the System.mdw file associated with the database.</span></span> <span data-ttu-id="9f9ff-113">Он полезен только в защищенных многоуровневой реализации.</span><span class="sxs-lookup"><span data-stu-id="9f9ff-113">It is useful only in secured multiuser implementations.</span></span>

