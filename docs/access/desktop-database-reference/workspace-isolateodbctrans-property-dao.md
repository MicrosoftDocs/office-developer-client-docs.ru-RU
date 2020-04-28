---
title: Свойство Workspace. Исолатеодбктранс (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 781679dfbd4050cfde219802db4cd9e1544d83ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302515"
---
# <a name="workspaceisolateodbctrans-property-dao"></a><span data-ttu-id="06a48-102">Свойство Workspace. Исолатеодбктранс (DAO)</span><span class="sxs-lookup"><span data-stu-id="06a48-102">Workspace.IsolateODBCTrans property (DAO)</span></span>


<span data-ttu-id="06a48-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="06a48-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="06a48-104">Задает или возвращает значение, указывающее, изолированы ли множественные транзакции, использующие один и тот же источник данных ODBC, подключенный к ядру СУБД Microsoft Access (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="06a48-104">Sets or returns a value that indicates whether multiple transactiond that involve the same Microsoft Access database engine-connected ODBC data source are isolated (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="06a48-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06a48-105">Syntax</span></span>

<span data-ttu-id="06a48-106">*Expression* . исолатеодбктранс</span><span class="sxs-lookup"><span data-stu-id="06a48-106">*expression* .IsolateODBCTrans</span></span>

<span data-ttu-id="06a48-107">*expression*: переменная, представляющая объект **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="06a48-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="06a48-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="06a48-108">Remarks</span></span>

<span data-ttu-id="06a48-109">В некоторых случаях требуется несколько одновременных транзакций для одного и того же подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="06a48-109">In some situations, you need to have multiple simultaneous transactions pending on the same ODBC connection.</span></span> <span data-ttu-id="06a48-110">Для этого необходимо открыть отдельную **рабочую область** для каждой транзакции.</span><span class="sxs-lookup"><span data-stu-id="06a48-110">To do this, you need to open a separate **Workspace** for each transaction.</span></span> <span data-ttu-id="06a48-111">Несмотря на то, что каждая **Рабочая область** может иметь собственное подключение ODBC к базе данных, производительность системы снижается.</span><span class="sxs-lookup"><span data-stu-id="06a48-111">Although each **Workspace** can have its own ODBC connection to the database, this slows system performance.</span></span> <span data-ttu-id="06a48-112">Так как изолированная изоляция транзакций обычно не обязательна, подключения ODBC из нескольких объектов **рабочей области** , открытых одним и тем же пользователем, совместно используются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="06a48-112">Because transaction isolation isn't usually required, ODBC connections from multiple **Workspace** objects opened by the same user are shared by default.</span></span>

<span data-ttu-id="06a48-113">Некоторые серверы ODBC, например Microsoft SQL Server, не разрешают одновременные транзакции для одного подключения.</span><span class="sxs-lookup"><span data-stu-id="06a48-113">Some ODBC servers, such as Microsoft SQL Server, don't allow simultaneous transactions on a single connection.</span></span> <span data-ttu-id="06a48-114">Если для такой базы данных требуется более одной транзакции, установите для свойства **исолатеодбктранс** значение **true** для каждой **рабочей области** сразу после ее открытия.</span><span class="sxs-lookup"><span data-stu-id="06a48-114">If you need to have more than one transaction at a time pending against such a database, set the **IsolateODBCTrans** property to **True** on each **Workspace** as soon as you open it.</span></span> <span data-ttu-id="06a48-115">Это приводит к выделению отдельного подключения ODBC для каждой **рабочей области**.</span><span class="sxs-lookup"><span data-stu-id="06a48-115">This forces a separate ODBC connection for each **Workspace**.</span></span>

