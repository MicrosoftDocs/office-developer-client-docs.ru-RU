---
title: Раздел SQL в файле настройки
TOCTitle: Customization File SQL section
ms:assetid: 002c544f-fe1b-6aeb-ba9a-97b1e1159516
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248776(v=office.15)
ms:contentKeyID: 48542901
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ae259589cc8d4945068901c59105425599edc64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295137"
---
# <a name="customization-file-sql-section"></a><span data-ttu-id="9ec6e-102">Раздел SQL в файле настройки</span><span class="sxs-lookup"><span data-stu-id="9ec6e-102">Customization File SQL section</span></span>


<span data-ttu-id="9ec6e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ec6e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9ec6e-104">Раздел **sql** может содержать новую строку SQL, которая заменяет строку команды клиента.</span><span class="sxs-lookup"><span data-stu-id="9ec6e-104">The **sql** section can contain a new SQL string that replaces the client command string.</span></span> <span data-ttu-id="9ec6e-105">Если строки SQL в разделе нет, раздел будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="9ec6e-105">If there is no SQL string in the section, the section will be ignored.</span></span>

<span data-ttu-id="9ec6e-106">Новая строка SQL может быть *параметризирована.*</span><span class="sxs-lookup"><span data-stu-id="9ec6e-106">The new SQL string may be *parameterized*.</span></span> <span data-ttu-id="9ec6e-107">То есть параметры в разделе **sql** SQL строки (назначенные по символу '?')  можно заменить соответствующими аргументами в идентификаторе в строке команд клиента (назначенный запятой-делимитированный список в скобки).</span><span class="sxs-lookup"><span data-stu-id="9ec6e-107">That is, parameters in the **sql** section SQL string (designated by the '?' character) can be replaced by corresponding arguments in an *identifier* in the client command string (designated by a comma-delimited list in parentheses).</span></span> <span data-ttu-id="9ec6e-108">Идентификатор и список аргументов ведут себя как вызов функции.</span><span class="sxs-lookup"><span data-stu-id="9ec6e-108">The identifier and argument list behave like a function call.</span></span>

<span data-ttu-id="9ec6e-109">Например, предположим, что строка команды клиента — "CustomerByID(4)", заглавная строка раздела SQL — SQL CustomerByID, а новая строка раздела SQL " \[ SELECT FROM Customers WHERE \] \* CustomerID = ?".</span><span class="sxs-lookup"><span data-stu-id="9ec6e-109">For example, assume the client command string is "CustomerByID(4)" , the SQL section header is \[SQL CustomerByID\] , and the new SQL section string is "SELECT \* FROM Customers WHERE CustomerID = ?".</span></span> <span data-ttu-id="9ec6e-110">Обработщик будет создавать, SQL раздела SQL CustomerByID, а новая строка раздела SQL \[ \] будет "SELECT FROM Customers WHERE \* CustomerID =?".</span><span class="sxs-lookup"><span data-stu-id="9ec6e-110">The Handler will generate , the SQL section header is \[SQL CustomerByID\] , and the new SQL section string is "SELECT \* FROM Customers WHERE CustomerID = ?".</span></span> <span data-ttu-id="9ec6e-111">Обработник будет создавать строку "SELECT FROM Customers WHERE CustomerID = 4" и использовать эту строку для \* запроса источника данных.</span><span class="sxs-lookup"><span data-stu-id="9ec6e-111">The Handler will generate "SELECT \* FROM Customers WHERE CustomerID = 4" and use that string to query the data source.</span></span>

<span data-ttu-id="9ec6e-112">Если новое SQL является строкой null (""), то раздел игнорируется.</span><span class="sxs-lookup"><span data-stu-id="9ec6e-112">If the new SQL statement is the null string (""), then the section is ignored.</span></span>

<span data-ttu-id="9ec6e-113">Если новая строка SQL не является допустимой, то выполнение этого утверждения будет неудачным.</span><span class="sxs-lookup"><span data-stu-id="9ec6e-113">If the new SQL statement string is not valid, then the execution of the statement will fail.</span></span> <span data-ttu-id="9ec6e-114">Параметр клиента фактически игнорируется.</span><span class="sxs-lookup"><span data-stu-id="9ec6e-114">The client parameter is effectively ignored.</span></span> <span data-ttu-id="9ec6e-115">Это можно сделать намеренно, чтобы "отключить" SQL клиентские команды, указав:</span><span class="sxs-lookup"><span data-stu-id="9ec6e-115">You can do this intentionally to "turn off" all client SQL commands by specifying:</span></span>

```sql 
 
[SQL default] 
SQL = " " 
```

## <a name="syntax"></a><span data-ttu-id="9ec6e-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ec6e-116">Syntax</span></span>

<span data-ttu-id="9ec6e-117">Замена SQL строки имеет форму:</span><span class="sxs-lookup"><span data-stu-id="9ec6e-117">A replacement SQL string entry is of the form:</span></span>

<span data-ttu-id="9ec6e-118">**SQL=\*sqlString**\*</span><span class="sxs-lookup"><span data-stu-id="9ec6e-118">**SQL=\*sqlString**\*</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ec6e-119">Part</span><span class="sxs-lookup"><span data-stu-id="9ec6e-119">Part</span></span></p></th>
<th><p><span data-ttu-id="9ec6e-120">Описание</span><span class="sxs-lookup"><span data-stu-id="9ec6e-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ec6e-121"><strong>SQL</strong></span><span class="sxs-lookup"><span data-stu-id="9ec6e-121"><strong>SQL</strong></span></span></p></td>
<td><p><span data-ttu-id="9ec6e-122">Буквальная строка, которая указывает, что это запись SQL раздела.</span><span class="sxs-lookup"><span data-stu-id="9ec6e-122">A literal string that indicates this is an SQL section entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ec6e-123"><strong><em>sqlString</em></strong></span><span class="sxs-lookup"><span data-stu-id="9ec6e-123"><strong><em>sqlString</em></strong></span></span></p></td>
<td><p><span data-ttu-id="9ec6e-124">Строка SQL, которая заменяет клиентскую строку.</span><span class="sxs-lookup"><span data-stu-id="9ec6e-124">An SQL string that replaces the client string.</span></span></p></td>
</tr>
</tbody>
</table>

