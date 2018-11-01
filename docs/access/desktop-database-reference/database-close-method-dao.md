---
title: Database.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 92b4075f09bb34eca465f49d30a9ba8777b3e583
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869654"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="66082-102">Database.Close Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="66082-102">Database.Close Method (DAO)</span></span>


<span data-ttu-id="66082-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66082-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66082-104">Закрывает открыть **базу данных**.</span><span class="sxs-lookup"><span data-stu-id="66082-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="66082-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66082-105">Syntax</span></span>

<span data-ttu-id="66082-106">*выражение* . Закрыть</span><span class="sxs-lookup"><span data-stu-id="66082-106">*expression* .Close</span></span>

<span data-ttu-id="66082-107">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="66082-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="66082-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="66082-108">Remarks</span></span>

<span data-ttu-id="66082-109">Если объект **базы данных** уже работает при использовании **Закрыть**, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="66082-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="66082-110">Альтернативой метод **Close** — это значение переменной объекта значение **Nothing** (задать dbsTemp = ничего).</span><span class="sxs-lookup"><span data-stu-id="66082-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

