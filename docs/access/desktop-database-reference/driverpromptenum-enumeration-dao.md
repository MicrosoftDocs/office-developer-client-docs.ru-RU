---
title: DriverPromptEnum enumeration (DAO)
TOCTitle: DriverPromptEnum Enumeration
ms:assetid: 8dda5e9f-a58f-a62d-eb49-5966d4a1e086
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197361(v=office.15)
ms:contentKeyID: 48546266
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9612c0713a86ed6ad34a5eff61e45efcddf6cf24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293667"
---
# <a name="driverpromptenum-enumeration-dao"></a><span data-ttu-id="66ad2-102">DriverPromptEnum enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="66ad2-102">DriverPromptEnum enumeration (DAO)</span></span>


<span data-ttu-id="66ad2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66ad2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66ad2-104">Указывает, нужно ли и когда пользователю предложено установить подключение.</span><span class="sxs-lookup"><span data-stu-id="66ad2-104">Specifies if and when to prompt the user to establish a connection.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66ad2-105">Имя</span><span class="sxs-lookup"><span data-stu-id="66ad2-105">Name</span></span></p></th>
<th><p><span data-ttu-id="66ad2-106">Значение</span><span class="sxs-lookup"><span data-stu-id="66ad2-106">Value</span></span></p></th>
<th><p><span data-ttu-id="66ad2-107">Описание</span><span class="sxs-lookup"><span data-stu-id="66ad2-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66ad2-108">dbDriverComplete</span><span class="sxs-lookup"><span data-stu-id="66ad2-108">dbDriverComplete</span></span></p></td>
<td><p><span data-ttu-id="66ad2-109">0</span><span class="sxs-lookup"><span data-stu-id="66ad2-109">0</span></span></p></td>
<td><p><span data-ttu-id="66ad2-110">Если указанная строка подключения содержит ключевое слово DSN, диспетчер драйверов использует строку, указанную при подключении, в противном случае она ведет себя так же, как при указании <strong>dbDriverPrompt.</strong></span><span class="sxs-lookup"><span data-stu-id="66ad2-110">If the connection string provided includes the DSN keyword, the driver manager uses the string as provided in connect, otherwise it behaves as it does when <strong>dbDriverPrompt</strong> is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66ad2-111">dbDriverCompleteRequired</span><span class="sxs-lookup"><span data-stu-id="66ad2-111">dbDriverCompleteRequired</span></span></p></td>
<td><p><span data-ttu-id="66ad2-112">3 </span><span class="sxs-lookup"><span data-stu-id="66ad2-112">3</span></span></p></td>
<td><p><span data-ttu-id="66ad2-113">(По умолчанию) Ведет себя как <strong>dbDriverComplete,</strong> за исключением того, что драйвер отключает элементы управления для любых сведений, не необходимых для завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="66ad2-113">(Default) Behaves like <strong>dbDriverComplete</strong> except the driver disables the controls for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66ad2-114">dbDriverNoPrompt</span><span class="sxs-lookup"><span data-stu-id="66ad2-114">dbDriverNoPrompt</span></span></p></td>
<td><p><span data-ttu-id="66ad2-115">1 </span><span class="sxs-lookup"><span data-stu-id="66ad2-115">1</span></span></p></td>
<td><p><span data-ttu-id="66ad2-116">Диспетчер драйверов использует строку подключения, предоставленную при подключении.</span><span class="sxs-lookup"><span data-stu-id="66ad2-116">The driver manager uses the connection string provided in connect.</span></span> <span data-ttu-id="66ad2-117">Если достаточные сведения не предоставлены, возвращается захватимая ошибка.</span><span class="sxs-lookup"><span data-stu-id="66ad2-117">If sufficient information is not provided, a trappable error is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66ad2-118">dbDriverPrompt</span><span class="sxs-lookup"><span data-stu-id="66ad2-118">dbDriverPrompt</span></span></p></td>
<td><p><span data-ttu-id="66ad2-119">2 </span><span class="sxs-lookup"><span data-stu-id="66ad2-119">2</span></span></p></td>
<td><p><span data-ttu-id="66ad2-120">Диспетчер драйверов отображает диалоговое окно "Источники данных <strong>ODBC".</strong></span><span class="sxs-lookup"><span data-stu-id="66ad2-120">The driver manager displays the <strong>ODBC Data Sources</strong> dialog box.</span></span> <span data-ttu-id="66ad2-121">Строка подключения, используемая для установления подключения, создается из имени источника данных (DSN), выбранного и заполненного пользователем через диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="66ad2-121">The connection string used to establish the connection is constructed from the data source name (DSN) selected and completed by the user via the dialog boxes.</span></span></p></td>
</tr>
</tbody>
</table>

