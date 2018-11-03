---
title: Перечисление DriverPromptEnum (DAO)
TOCTitle: DriverPromptEnum Enumeration
ms:assetid: 8dda5e9f-a58f-a62d-eb49-5966d4a1e086
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197361(v=office.15)
ms:contentKeyID: 48546266
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b6911e325b070a8c6d62b70dfcacf96ae1dc3dc
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943558"
---
# <a name="driverpromptenum-enumeration-dao"></a><span data-ttu-id="1c4df-102">Перечисление DriverPromptEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="1c4df-102">DriverPromptEnum enumeration (DAO)</span></span>


<span data-ttu-id="1c4df-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c4df-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1c4df-104">Указывает, если и при пользователя для установки подключения.</span><span class="sxs-lookup"><span data-stu-id="1c4df-104">Specifies if and when to prompt the user to establish a connection.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c4df-105">Имя</span><span class="sxs-lookup"><span data-stu-id="1c4df-105">Name</span></span></p></th>
<th><p><span data-ttu-id="1c4df-106">Значение</span><span class="sxs-lookup"><span data-stu-id="1c4df-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1c4df-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1c4df-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c4df-108">dbDriverComplete</span><span class="sxs-lookup"><span data-stu-id="1c4df-108">dbDriverComplete</span></span></p></td>
<td><p><span data-ttu-id="1c4df-109">0</span><span class="sxs-lookup"><span data-stu-id="1c4df-109">0</span></span></p></td>
<td><p><span data-ttu-id="1c4df-110">Если строку подключения, предоставленную содержит ключевое слово уведомления о Доставке, диспетчер использует драйвер, строки в подключиться, в противном случае его ведет себя так что происходит, когда он указан <strong>dbDriverPrompt</strong> .</span><span class="sxs-lookup"><span data-stu-id="1c4df-110">If the connection string provided includes the DSN keyword, the driver manager uses the string as provided in connect, otherwise it behaves as it does when <strong>dbDriverPrompt</strong> is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c4df-111">dbDriverCompleteRequired</span><span class="sxs-lookup"><span data-stu-id="1c4df-111">dbDriverCompleteRequired</span></span></p></td>
<td><p><span data-ttu-id="1c4df-112">3</span><span class="sxs-lookup"><span data-stu-id="1c4df-112">3</span></span></p></td>
<td><p><span data-ttu-id="1c4df-113">(По умолчанию) Действует как <strong>dbDriverComplete</strong> , за исключением драйвер отключение элементов управления для какие-либо сведения для выполнения подключения не требуется.</span><span class="sxs-lookup"><span data-stu-id="1c4df-113">(Default) Behaves like <strong>dbDriverComplete</strong> except the driver disables the controls for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c4df-114">dbDriverNoPrompt</span><span class="sxs-lookup"><span data-stu-id="1c4df-114">dbDriverNoPrompt</span></span></p></td>
<td><p><span data-ttu-id="1c4df-115">1</span><span class="sxs-lookup"><span data-stu-id="1c4df-115">1</span></span></p></td>
<td><p><span data-ttu-id="1c4df-116">Подключите диспетчер использует драйвер, предоставленные в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="1c4df-116">The driver manager uses the connection string provided in connect.</span></span> <span data-ttu-id="1c4df-117">Если этот параметр не указан достаточно данных возвращается перехватываемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="1c4df-117">If sufficient information is not provided, a trappable error is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c4df-118">dbDriverPrompt</span><span class="sxs-lookup"><span data-stu-id="1c4df-118">dbDriverPrompt</span></span></p></td>
<td><p><span data-ttu-id="1c4df-119">2</span><span class="sxs-lookup"><span data-stu-id="1c4df-119">2</span></span></p></td>
<td><p><span data-ttu-id="1c4df-120">Диспетчер драйверов отображает диалоговое окно <strong>Источники данных ODBC</strong> .</span><span class="sxs-lookup"><span data-stu-id="1c4df-120">The driver manager displays the <strong>ODBC Data Sources</strong> dialog box.</span></span> <span data-ttu-id="1c4df-121">Строку подключения, используемую для установление соединения состоит из имя источника данных (DSN), а для завершения пользователем с помощью диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="1c4df-121">The connection string used to establish the connection is constructed from the data source name (DSN) selected and completed by the user via the dialog boxes.</span></span></p></td>
</tr>
</tbody>
</table>

