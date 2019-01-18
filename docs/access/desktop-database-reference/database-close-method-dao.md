---
title: Метод Database.Close (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 190b47b59bd9781553912f91156c74a3fd09c2d5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699979"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="1a45f-102">Метод Database.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="1a45f-102">Database.Close method (DAO)</span></span>


<span data-ttu-id="1a45f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a45f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1a45f-104">Закрывает открыть **базу данных**.</span><span class="sxs-lookup"><span data-stu-id="1a45f-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a45f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a45f-105">Syntax</span></span>

<span data-ttu-id="1a45f-106">*выражение* . Закрыть</span><span class="sxs-lookup"><span data-stu-id="1a45f-106">*expression* .Close</span></span>

<span data-ttu-id="1a45f-107">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="1a45f-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a45f-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="1a45f-108">Remarks</span></span>

<span data-ttu-id="1a45f-109">Если объект **базы данных** уже работает при использовании **Закрыть**, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="1a45f-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="1a45f-110">Альтернативой метод **Close** — это значение переменной объекта значение **Nothing** (задать dbsTemp = ничего).</span><span class="sxs-lookup"><span data-stu-id="1a45f-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

