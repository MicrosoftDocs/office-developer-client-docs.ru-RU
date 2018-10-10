---
title: Workspace.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 87f72a58cd3e24838416ef4d19ec1a2cf91e7c1f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480357"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="bae04-102">Workspace.Close Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="bae04-102">Workspace.Close Method (DAO)</span></span>


<span data-ttu-id="bae04-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bae04-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bae04-104">Закрытие открытых **рабочей области**.</span><span class="sxs-lookup"><span data-stu-id="bae04-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bae04-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bae04-105">Syntax</span></span>

<span data-ttu-id="bae04-106">*выражение* . Закрыть</span><span class="sxs-lookup"><span data-stu-id="bae04-106">*expression* .Close</span></span>

<span data-ttu-id="bae04-107">*выражение* Переменная, которая представляет собой объект- **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="bae04-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bae04-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="bae04-108">Remarks</span></span>

<span data-ttu-id="bae04-109">Если объект **рабочей области** уже работает при использовании **Закрыть**, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="bae04-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="bae04-110">Альтернативой метод **Close** — это значение переменной объекта значение **Nothing** (задать dbsTemp = ничего).</span><span class="sxs-lookup"><span data-stu-id="bae04-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

