---
title: Метод Workspace. Close (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0049fb335c869a050a2c20d5740c487413c76786
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305959"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="4d469-102">Метод Workspace. Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="4d469-102">Workspace.Close method (DAO)</span></span>


<span data-ttu-id="4d469-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d469-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4d469-104">ЗаКрывает открытую **рабочую область**.</span><span class="sxs-lookup"><span data-stu-id="4d469-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d469-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d469-105">Syntax</span></span>

<span data-ttu-id="4d469-106">*выражение*.Close</span><span class="sxs-lookup"><span data-stu-id="4d469-106">*expression* .Close</span></span>

<span data-ttu-id="4d469-107">*expression*: переменная, представляющая объект **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="4d469-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d469-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="4d469-108">Remarks</span></span>

<span data-ttu-id="4d469-109">Если объект **Workspace** уже закрыт при использовании **Close**, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="4d469-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="4d469-110">Альтернатива методу **Close** заключается в присвоении объектной переменной значения **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="4d469-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

