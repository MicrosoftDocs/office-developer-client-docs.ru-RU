---
title: Перечисление Дриверпромптенум (DAO)
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
# <a name="driverpromptenum-enumeration-dao"></a><span data-ttu-id="e04c1-102">Перечисление Дриверпромптенум (DAO)</span><span class="sxs-lookup"><span data-stu-id="e04c1-102">DriverPromptEnum enumeration (DAO)</span></span>


<span data-ttu-id="e04c1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e04c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e04c1-104">Указывает, следует ли и когда предлагать пользователю установить подключение.</span><span class="sxs-lookup"><span data-stu-id="e04c1-104">Specifies if and when to prompt the user to establish a connection.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e04c1-105">Имя</span><span class="sxs-lookup"><span data-stu-id="e04c1-105">Name</span></span></p></th>
<th><p><span data-ttu-id="e04c1-106">Значение</span><span class="sxs-lookup"><span data-stu-id="e04c1-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e04c1-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e04c1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e04c1-108">дбдриверкомплете</span><span class="sxs-lookup"><span data-stu-id="e04c1-108">dbDriverComplete</span></span></p></td>
<td><p><span data-ttu-id="e04c1-109">нуль</span><span class="sxs-lookup"><span data-stu-id="e04c1-109">0</span></span></p></td>
<td><p><span data-ttu-id="e04c1-110">Если предоставленная строка подключения включает ключевое слово DSN, диспетчер драйверов использует строку, предоставленную в Connect, в противном случае она ведет себя так, как при указании <strong>дбдриверпромпт</strong> .</span><span class="sxs-lookup"><span data-stu-id="e04c1-110">If the connection string provided includes the DSN keyword, the driver manager uses the string as provided in connect, otherwise it behaves as it does when <strong>dbDriverPrompt</strong> is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e04c1-111">дбдриверкомплетерекуиред</span><span class="sxs-lookup"><span data-stu-id="e04c1-111">dbDriverCompleteRequired</span></span></p></td>
<td><p><span data-ttu-id="e04c1-112">4</span><span class="sxs-lookup"><span data-stu-id="e04c1-112">3</span></span></p></td>
<td><p><span data-ttu-id="e04c1-113">Умолчани Аналогично <strong>дбдриверкомплете</strong> , за исключением того, что для всех элементов управления не требуется никаких сведений для завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="e04c1-113">(Default) Behaves like <strong>dbDriverComplete</strong> except the driver disables the controls for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e04c1-114">дбдривернопромпт</span><span class="sxs-lookup"><span data-stu-id="e04c1-114">dbDriverNoPrompt</span></span></p></td>
<td><p><span data-ttu-id="e04c1-115">1,1</span><span class="sxs-lookup"><span data-stu-id="e04c1-115">1</span></span></p></td>
<td><p><span data-ttu-id="e04c1-116">Диспетчер драйверов использует строку подключения, указанную в разделе Connect.</span><span class="sxs-lookup"><span data-stu-id="e04c1-116">The driver manager uses the connection string provided in connect.</span></span> <span data-ttu-id="e04c1-117">Если не указано достаточное количество сведений, возвращается Перехватываемая ошибка.</span><span class="sxs-lookup"><span data-stu-id="e04c1-117">If sufficient information is not provided, a trappable error is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e04c1-118">дбдриверпромпт</span><span class="sxs-lookup"><span data-stu-id="e04c1-118">dbDriverPrompt</span></span></p></td>
<td><p><span data-ttu-id="e04c1-119">2</span><span class="sxs-lookup"><span data-stu-id="e04c1-119">2</span></span></p></td>
<td><p><span data-ttu-id="e04c1-120">Диспетчер драйверов отображает диалоговое окно " <strong>Источники данных ODBC</strong> ".</span><span class="sxs-lookup"><span data-stu-id="e04c1-120">The driver manager displays the <strong>ODBC Data Sources</strong> dialog box.</span></span> <span data-ttu-id="e04c1-121">Строка подключения, используемая для установки подключения, строится на основе имени источника данных (DSN), выбранного и выполненного пользователем с помощью диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="e04c1-121">The connection string used to establish the connection is constructed from the data source name (DSN) selected and completed by the user via the dialog boxes.</span></span></p></td>
</tr>
</tbody>
</table>

