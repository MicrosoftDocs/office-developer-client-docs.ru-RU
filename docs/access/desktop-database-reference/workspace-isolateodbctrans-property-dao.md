---
title: Workspace.IsolateODBCTrans Property (DAO)
TOCTitle: IsolateODBCTrans Property
ms:assetid: f7a48358-870b-cad3-d4ef-e46b50428e12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836924(v=office.15)
ms:contentKeyID: 48548770
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053083
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 197bf35c796fe1e34122b7d4214043e9217fb3d9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878544"
---
# <a name="workspaceisolateodbctrans-property-dao"></a><span data-ttu-id="7a299-102">Workspace.IsolateODBCTrans Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="7a299-102">Workspace.IsolateODBCTrans Property (DAO)</span></span>


<span data-ttu-id="7a299-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7a299-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7a299-104">Задает или возвращает значение, указывающее, включены ли несколько transactiond, связанных с одной Microsoft Access базы данных подключен модуль источник данных ODBC изолированный (Microsoft Access рабочие области только).</span><span class="sxs-lookup"><span data-stu-id="7a299-104">Sets or returns a value that indicates whether multiple transactiond that involve the same Microsoft Access database engine-connected ODBC data source are isolated (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a299-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a299-105">Syntax</span></span>

<span data-ttu-id="7a299-106">*выражение* . IsolateODBCTrans</span><span class="sxs-lookup"><span data-stu-id="7a299-106">*expression* .IsolateODBCTrans</span></span>

<span data-ttu-id="7a299-107">*выражение* Переменная, которая представляет собой объект- **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="7a299-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a299-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="7a299-108">Remarks</span></span>

<span data-ttu-id="7a299-109">В некоторых случаях необходимо иметь несколько одновременных незавершенных транзакций для общего подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="7a299-109">In some situations, you need to have multiple simultaneous transactions pending on the same ODBC connection.</span></span> <span data-ttu-id="7a299-110">Для этого необходимо открыть отдельный **рабочей области** для каждой транзакции.</span><span class="sxs-lookup"><span data-stu-id="7a299-110">To do this, you need to open a separate **Workspace** for each transaction.</span></span> <span data-ttu-id="7a299-111">Хотя для каждой **рабочей области** может иметь собственный подключения ODBC к базе данных, это снижает производительность системы.</span><span class="sxs-lookup"><span data-stu-id="7a299-111">Although each **Workspace** can have its own ODBC connection to the database, this slows system performance.</span></span> <span data-ttu-id="7a299-112">Так как изоляции транзакций не обычно не требуется, подключения ODBC от нескольких объектов **рабочей области** при открытии же являются общими по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7a299-112">Because transaction isolation isn't usually required, ODBC connections from multiple **Workspace** objects opened by the same user are shared by default.</span></span>

<span data-ttu-id="7a299-113">На некоторых серверах ODBC, такие как Microsoft SQL Server не разрешать одновременных транзакций для одного подключения.</span><span class="sxs-lookup"><span data-stu-id="7a299-113">Some ODBC servers, such as Microsoft SQL Server, don't allow simultaneous transactions on a single connection.</span></span> <span data-ttu-id="7a299-114">Если необходимо иметь несколько транзакций во время ожидающие относительно такой базы данных, присвойте свойству **IsolateODBCTrans** значение **True,** на каждой **рабочей области** сразу после его открытия.</span><span class="sxs-lookup"><span data-stu-id="7a299-114">If you need to have more than one transaction at a time pending against such a database, set the **IsolateODBCTrans** property to **True** on each **Workspace** as soon as you open it.</span></span> <span data-ttu-id="7a299-115">Это заставляет отдельное подключение ODBC для каждой **рабочей области**.</span><span class="sxs-lookup"><span data-stu-id="7a299-115">This forces a separate ODBC connection for each **Workspace**.</span></span>

