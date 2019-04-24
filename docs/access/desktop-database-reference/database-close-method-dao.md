---
title: Метод Database. Close (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 190b47b59bd9781553912f91156c74a3fd09c2d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295025"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="a0134-102">Метод Database. Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="a0134-102">Database.Close method (DAO)</span></span>


<span data-ttu-id="a0134-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a0134-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a0134-104">ЗаКрывает открытую **базу данных**.</span><span class="sxs-lookup"><span data-stu-id="a0134-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0134-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0134-105">Syntax</span></span>

<span data-ttu-id="a0134-106">*выражение*.Close</span><span class="sxs-lookup"><span data-stu-id="a0134-106">*expression* .Close</span></span>

<span data-ttu-id="a0134-107">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="a0134-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0134-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="a0134-108">Remarks</span></span>

<span data-ttu-id="a0134-109">Если объект **Database** уже закрыт при использовании **Close**, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="a0134-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="a0134-110">Альтернатива методу **Close** заключается в присвоении объектной переменной значения **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="a0134-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

