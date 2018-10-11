---
title: Customization File SQL Section
TOCTitle: Customization File SQL Section
ms:assetid: 002c544f-fe1b-6aeb-ba9a-97b1e1159516
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248776(v=office.15)
ms:contentKeyID: 48542901
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09be671ba15727e3612ade78c5b54af12b1d1c57
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480114"
---
# <a name="customization-file-sql-section"></a><span data-ttu-id="d2ec3-102">Customization File SQL Section</span><span class="sxs-lookup"><span data-stu-id="d2ec3-102">Customization File SQL Section</span></span>


<span data-ttu-id="d2ec3-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2ec3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d2ec3-104">В разделе **sql** может содержать строку SQL, которая заменяет строки команды клиента.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-104">The **sql** section can contain a new SQL string that replaces the client command string.</span></span> <span data-ttu-id="d2ec3-105">Если строка не SQL в разделе разделе будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-105">If there is no SQL string in the section, the section will be ignored.</span></span>

<span data-ttu-id="d2ec3-106">Создать строку SQL может быть *параметризованный*.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-106">The new SQL string may be *parameterized*.</span></span> <span data-ttu-id="d2ec3-107">То есть соответствующих аргументы в *идентификатор* в командной строке клиента (обозначенного разделенный запятыми список в скобки) могут быть заменены параметров в строке SQL раздел **sql** (обозначенного символ «?»).</span><span class="sxs-lookup"><span data-stu-id="d2ec3-107">That is, parameters in the **sql** section SQL string (designated by the '?' character) can be replaced by corresponding arguments in an *identifier* in the client command string (designated by a comma-delimited list in parentheses).</span></span> <span data-ttu-id="d2ec3-108">Идентификатор и список аргументов обрабатываются как вызов функции.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-108">The identifier and argument list behave like a function call.</span></span>

<span data-ttu-id="d2ec3-109">Предположим, например, строки команды клиента — «CustomerByID(4)», заголовок раздела SQL — \[SQL CustomerByID\] , и — это новый раздел строки SQL «ВЫБЕРИТЕ \* из клиентов WHERE CustomerID = ?».</span><span class="sxs-lookup"><span data-stu-id="d2ec3-109">For example, assume the client command string is "CustomerByID(4)" , the SQL section header is \[SQL CustomerByID\] , and the new SQL section string is "SELECT \* FROM Customers WHERE CustomerID = ?".</span></span> <span data-ttu-id="d2ec3-110">Будет создан обработчик, заголовок раздела SQL — \[SQL CustomerByID\] , и — это новый раздел строки SQL «ВЫБЕРИТЕ \* из клиентов WHERE CustomerID = ?».</span><span class="sxs-lookup"><span data-stu-id="d2ec3-110">The Handler will generate , the SQL section header is \[SQL CustomerByID\] , and the new SQL section string is "SELECT \* FROM Customers WHERE CustomerID = ?".</span></span> <span data-ttu-id="d2ec3-111">Будет создан обработчик «ВЫБЕРИТЕ \* из клиентов WHERE CustomerID = 4» и использовать эту строку для запроса источника данных.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-111">The Handler will generate "SELECT \* FROM Customers WHERE CustomerID = 4" and use that string to query the data source.</span></span>

<span data-ttu-id="d2ec3-112">Если новые инструкции SQL — это пустая строка ("»), а затем раздел пропускается.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-112">If the new SQL statement is the null string (""), then the section is ignored.</span></span>

<span data-ttu-id="d2ec3-113">Если создать строку инструкции SQL не является допустимым, выполнение инструкции завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-113">If the new SQL statement string is not valid, then the execution of the statement will fail.</span></span> <span data-ttu-id="d2ec3-114">Параметр клиента эффективно игнорируется.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-114">The client parameter is effectively ignored.</span></span> <span data-ttu-id="d2ec3-115">Для этого специально для «отключения» все команды SQL клиента, указав:</span><span class="sxs-lookup"><span data-stu-id="d2ec3-115">You can do this intentionally to "turn off" all client SQL commands by specifying:</span></span>

```sql 
 
[SQL default] 
SQL = " " 
```

## <a name="syntax"></a><span data-ttu-id="d2ec3-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2ec3-116">Syntax</span></span>

<span data-ttu-id="d2ec3-117">Замена запись строки SQL не формы:</span><span class="sxs-lookup"><span data-stu-id="d2ec3-117">A replacement SQL string entry is of the form:</span></span>

<span data-ttu-id="d2ec3-118">**SQL = \* sqlString**\*</span><span class="sxs-lookup"><span data-stu-id="d2ec3-118">**SQL=\*sqlString**\*</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d2ec3-119">Часть</span><span class="sxs-lookup"><span data-stu-id="d2ec3-119">Part</span></span></p></th>
<th><p><span data-ttu-id="d2ec3-120">Описание</span><span class="sxs-lookup"><span data-stu-id="d2ec3-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2ec3-121"><strong>SQL</strong></span><span class="sxs-lookup"><span data-stu-id="d2ec3-121"><strong>SQL</strong></span></span></p></td>
<td><p><span data-ttu-id="d2ec3-122">Строковый литерал, которое указывает, это является записью раздел SQL.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-122">A literal string that indicates this is an SQL section entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2ec3-123"><strong><em>sqlString</em></strong></span><span class="sxs-lookup"><span data-stu-id="d2ec3-123"><strong><em>sqlString</em></strong></span></span></p></td>
<td><p><span data-ttu-id="d2ec3-124">Строка SQL, которая заменяет строку клиента.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-124">An SQL string that replaces the client string.</span></span></p></td>
</tr>
</tbody>
</table>

