---
title: Метод Workspace.Close (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 63b935fa178eb4c55ce11724ec3fd5f62d056779
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919852"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="1023b-102">Метод Workspace.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="1023b-102">Workspace.Close method (DAO)</span></span>


<span data-ttu-id="1023b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1023b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1023b-104">Закрытие открытых **рабочей области**.</span><span class="sxs-lookup"><span data-stu-id="1023b-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1023b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1023b-105">Syntax</span></span>

<span data-ttu-id="1023b-106">*выражение* . Закрыть</span><span class="sxs-lookup"><span data-stu-id="1023b-106">*expression* .Close</span></span>

<span data-ttu-id="1023b-107">*выражение* Переменная, которая представляет собой объект- **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="1023b-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1023b-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="1023b-108">Remarks</span></span>

<span data-ttu-id="1023b-109">Если объект **рабочей области** уже работает при использовании **Закрыть**, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="1023b-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="1023b-110">Альтернативой метод **Close** — это значение переменной объекта значение **Nothing** (задать dbsTemp = ничего).</span><span class="sxs-lookup"><span data-stu-id="1023b-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

