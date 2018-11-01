---
title: Workspace.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 38f1a7a525a2cf57a98ee3fa015ce29b368aab9b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884130"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="bafe5-102">Workspace.Close Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="bafe5-102">Workspace.Close Method (DAO)</span></span>


<span data-ttu-id="bafe5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bafe5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bafe5-104">Закрытие открытых **рабочей области**.</span><span class="sxs-lookup"><span data-stu-id="bafe5-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bafe5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bafe5-105">Syntax</span></span>

<span data-ttu-id="bafe5-106">*выражение* . Закрыть</span><span class="sxs-lookup"><span data-stu-id="bafe5-106">*expression* .Close</span></span>

<span data-ttu-id="bafe5-107">*выражение* Переменная, которая представляет собой объект- **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="bafe5-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bafe5-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="bafe5-108">Remarks</span></span>

<span data-ttu-id="bafe5-109">Если объект **рабочей области** уже работает при использовании **Закрыть**, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="bafe5-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="bafe5-110">Альтернативой метод **Close** — это значение переменной объекта значение **Nothing** (задать dbsTemp = ничего).</span><span class="sxs-lookup"><span data-stu-id="bafe5-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

